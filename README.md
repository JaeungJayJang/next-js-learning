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
### chapter 10
### chapter 11
### chapter 12
### chapter 13
### chapter 14
### chapter 15
### chapter 16
