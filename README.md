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
### chapter 8
### chapter 9
### chapter 10
### chapter 11
### chapter 12
### chapter 13
### chapter 14
### chapter 15
### chapter 16
