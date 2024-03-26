## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

## Notes
This is a place where I am making a notes about things that I newly learned by following each chapter... or just anything that I wanted to write here.
### chapter 1
  it says that Next.js team recommend the usage of **Prisma**. My stance was not using it as it's encapsulating whole data fetching process and can cause problem.. I need to look more into it and see how it can be beneficial to my usecase.
### chapter 2
  learned usage of global.css and styled css module. styled css is what I encountered while using MUI library and it's great that they can translate the classname to unique classname. this will be definitely be a good as project gets big.
  First time heard of clsx library. I already faced issue of applying conditional classname while building personal project and it's great that this solution already exist. I don't have to manage separate components with different props with this.
### chapter 3
  learned about cumulative layout shift (CLS) and it is a metric to measure the performance of the website. vaguely knew about it but I did not think about the **font layout shift**.
  Glad to know that next wrapper for fonts and image prevent this issue by pre-downloading during build time and host with other static assets to reduce network latency.
### chapter 4
  This covered about layouts in Next.js app route. it helped to review my understanding.
### chapter 5
  This chapter introduced link component and how to use it.
  Learned that the Link allows partial refreshing instead of full refresh and I was able to see this behavior through console, network tab.
  also learned that Next.js performs prefetching of the linked page if **Link** component exist so that when user clicks the component the page is ready to be served already.i
  This is also a chapter that shows active link on the nav bar using **clsx** library.
### chapter 6
  This chapter went over how to setup github and host database and the app through vercel.
### chapter 7
  This chapter covered data fetching.
  This mentions that one of the pro about server side component is that the props are not necessary and data can be fetched directly, but as I've been using CSC so far that this felt like serving static pages and no dynamics at all, and requiring additional lines to define that the file is associated with **client** at the top. I need more experience on clearly identifying what components are beneficial to be server side vs client side before I do anything to reduce design time.
  The nitty gritty portions for retrieving data from SQL is given that I feel like I am not getting this yet.. I need to dig more into it and actually write this myself to get experience.
  This also covers the usage of **Promise.all** to send request in parallel. Good example.
### chapter 8
  This chapter covered about how to make the request dynamic. The problem is that the components are server side components and they are cached into CDN and this is not a great behavior for applications like dashboard that relies on up-to-date data. So this chapter introduced a way to make next.js API dynamic by using **unstable_noStore** function as **noStore** and use this function at the top of each functions.
  my go to backend so far is based on python and I wonder how this can be helpful for me unless I go with node based API... I will just keep this in mind that this exist.
### chapter 9
  This chapter is one of the best chapter to look for so far: it covered about how to show skeletons when data is being loaded.
  I was able to achieve this with HTTP request and states before but indeed this was too much to write, and probably not direct to understand.
  As this chapter covered, **Suspense** function from React library would be a better alternative approach to handle the loading state.
  This chapter also covered three different ways to handle the loading state, where usage of the **loading.tsx** is the most astonishing feature so far;
  I did not know that next.js implemented this feature until now.
  whatever approach I take from here, I still need to make the skeleton components myself, so that is a bit disappointment, but it's not like I found one library that can do this... so this is good anyway.
  This chapter also introduced **Route Group** that allows files such as loading.tsx does not apply to the child component by excluding the groups from URL path.
  This route group can be used to group files together and make as sections to easily identify which files are associated with which teams in larger projects. this is a good feature indeed to manage tasks.
### chapter 10
  Skipping this chapter as this is an experimental feature as of right now.
### chapter 11
  This was a long chapter that covered about search and pagination feature and I thing it is one of the best chapter covered here alogn with chapter 9.
  This uses useSearchParams hook to get query parameters, usePathname hook to get current pathname, and useRouter hook to change page on client side. It covers how to make the search dynamic using these 3 hooks and also how this request can be sent to the server side components and triggers it to work. This is a great concept to know that the server side can be affected by the changes on the client side. This still feels it's a bit magic to me but my assumption is that the changes on the client affects the changes DOM, and that's why server side is also rerendered? I need to look more into DOM manipulation part to fully capture the behind logic of this.
  It is also great that searchParams are supported from **page.tsx** so I can use directly inside page.tsx. (although I need to specify the type..)
  Another great thing covered: **debouncing**. This tutorial introduce public library called `use-debounce` and it can help to implement debounce logic out of box so I don't need to make the logic myself.
  It was conversome to implement all this with state and would be a great option in future projects. Logic is simple; I can change the function that are passed to the onChange with the useDebouncedCallback wrapper function and define the debouncing rate at the end.
  
  Pagination is cool, but it seems to be that this is a more complex usage of the hooks covered above and using **page** query param instead of **query** query param.
### chapter 12
  As the chapter goes toward the end, more valuable contents are covered in the chapter.
  This chapter introduced something called server actions and this is indeed cool that Vercel introduced this feature into Next.js, I am a bit unsure if this will be useful for my case where I will likely to build my own API route with Python that I am more familiar with. I could use API route and the server route seems to make it easier than making API route logic, but would need to see how Vercel wants to move with this in the later version.
  One thing that makes me wonder is that the entire example relies on the form to make the API call, which is fine but I thought that forms are all POST request and it makes me think that the logic is a bit unorganized..
  another potentially useful library used here is **ZOD**. I created a separate file that keeps schema of the database and then used it to validate if the data is correct. At first I was unsure why this is needed as typescript itself can check if the variable types are correct until I see a comment comparing **ZOD with YUP...** I used YUP before when I needed to implement logic to check if user input for form is correct and this experience makes me think backward that ZOD is a similar tool as YUP but more friendly with typescript and I could define the variables, strings however I want with ZOD.<br/>
  [Another thing I found is that the type safety for typescript is only during compile time and ZOD can validate during runtime to provide increase security and reliability.](https://www.turing.com/blog/data-integrity-through-zod-validation/#:~:text=Some%20developers%20might%20reason%2C%20Why,Zod%20library%20solves%20this%20problem.)
### chapter 13
  This  chapter covers uasge of try and catch, with the intro to error.tsx and not-found.tsx pages that can be shown when errors arise and handling it on client side.<br/>
  This uses not-found function from `next/navigation` that basically reroute the user to not-found.tsx page. One I was worried at first is that the function handles automatically based on the type as well, such as like showing notfound only when the request is of GET request, but it seems to be **NOT**, and I can implement logics however I want and show the page at the line it needs to be, so this is better for the most of my usual cases.
### chapter 14
  accessibility:
  uses [eslint-plugin-jsx-a11y](https://www.npmjs.com/package/eslint-plugin-jsx-a11y) to check accessibility beforehand. things include `alt`, `aria-*`, and `role`.<br/>

  - Use semantic HTML; use proper html tags instead of div.
  - Use labelling: use `label` or `htmlFor` for each field.
  - focus outline when a field is selected.

  It was a hand-on practice section to implement the components with high accessibility. Learned usage of aria tags that are useful to show text in error and those are `aria-describedby` and `aria-live`.
  also used `useFormState` hook to keep the previous states of the variables and use them to show error messages to the end user or not.
  I did not bother to learn about aria tags before and I learned the importance of them from this chapter.
### chapter 15
### chapter 16
