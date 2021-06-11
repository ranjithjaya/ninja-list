# Next.js Tutorial from Ninja
## Installing
- cd C:\Users\Ranjithj\OneDrive\Documents\ReactProjects\React-Next\Ninja-List
cd ninja-list
- npx create-next-app ninja-list
## Run 
- npm run dev
---------------------------------------------------------
## #1 - Introduction & Setup
[https://www.youtube.com/watch?v=A63UxsQsEbU]

In this Next.js tutorial series you'll learn how to create a website with Next (& React) - including pages, routes, layouts, fetching data & deployment.

---------------------------------------------------------

## #2 - Pages & Routes
[https://www.youtube.com/watch?v=zktJ8-k0JDc]

In this Next.js tutorial we'll take a look at how pages & routes are created using React components.

### Automatically created routes:
If you add a new file or folder under pages folder routes for those elements will be automaticaly created and cn be access typing following options after http://localhost:3000 in ther browser
- /               index.js            Home page
- /ninja          /ninja/index.js     All ninjas page
- /ninja/test     /ninja/test.js      Test page

---------------------------------------------------------

## #3 - Adding Other Components
[https://www.youtube.com/watch?v=MJT_WXdSPjE]

Hear we create 2 compnents not inside the pages folder but in outside in the new folder comps 
- /comps
- /comps/Navbar.js
- /comps/Footer.js

Add components to /pages/index.js
- < Navbar />
- < Footer />

## #4 - Linking Between Pages
[https://www.youtube.com/watch?v=u8vaAc3ivcY]

In this Next js tutorial we'll see how we can link between pages using the Link component.

In

| index.js | import Link from 'next/link' |

| FILE| ELEMENT |
| ------ | ------ |
| /pages/index.js | import Link from 'next/link' |
|  | < Link href="/ninjas/" > < a>See Ninja Listing< /a > < /Link> |
| /comps/Navbar.js | import Link from 'next/link'; < Link href="/">< a>Home< /a>< /Link> |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |


## #5 - Creating a Layout Component
[https://www.youtube.com/watch?v=DGn25s42NvQ]


In this Next.js tutorial we'll see how to reate a layout component (navbar and footer) which can wrap our page content. 
On each page we want to add Nabar as header and Copyright as foter
In order to do this we create layout.js file and include those Navbar and Footer and include this layout in _app.js file.
Now you could see header and footer in each and every page.

## #6 - Adding Styles
[https://www.youtube.com/watch?v=qKwnlTVAGnA]

in this Next.js tutorial we'll see how to add global styles & also CSS modules to our Next project.
- globals.css styls are common for all pages in the project
- those styles can be owerritten through page specific stayles in Home.modules.css styles

## #7 - Custom 404 Page
[https://www.youtube.com/watch?v=dlee0ESZvlc]

When the route unknown 
- built-in 404 will be displayed
- to diplay own customized 404, create new 404.js page in pages folder, for stiling global.css should be updated as well

## #8 - Redirecting Users
[https://www.youtube.com/watch?v=O3yKwz4wRHc]

In this Next.js tutorial we'll learn how to use the useRoutr hook to redirect users from one page to another.
- In 404 page we included go back tohome page button
- to do that in automatically after 3 second we use custom hooks, useEffects in 404 page

## #9 - Images & Metadata
[https://www.youtube.com/watch?v=rHncMH1CfCU]

In this Next.js tutorial I'll show you how to use the Image component in Next & also how to use the Head component to add titles and metadata to your pages.
To customize heading of the app (Ninja List)
- what ever objects in public folder will be aplicable to all pages in the project
- Copy logo.png image to public folder
```html
- in Navbar.js  
    - replace <h1>Ninja List</h1> with <img src="/logo.png" />
    - Now big image will be dispayed instead of Ninja List
    - In version 10 image component has been introduced insted <img> tag
    - include import Image from 'next/image'
    - replace <img src="/logo.png" /> with <Image src="/logo.png" alt="site logo" width={128} height={77} /> and see the difference
```
- Introducing Head tag with meta data: The name appear on  browser tab of  'localhost:3000' can be customize like 'NinjaList Home'
```html
    - open pages/index.js and add empty tag <> just after return( and add folowings:
    - <Head>
        <title>Ninja List | Home</title>
      </Head>
    - Now you can do it every page if needed
```

## #10 - Fetching Data (getStaticProps)
[https://www.youtube.com/watch?v=zueyEdRZQlk]

 in this Next.js tutorial we'll use the getStaticProps function to reach out and fetch some data which we can then inject into our page components.
- To get data into components we use fake data from {JSON} Placeholder https://jsonplaceholder.typicode.com/ 
- we will fech data in All Ninja in /pages/ninjas/index.js

## #11 - Dynamic Routes (part 1)
[https://www.youtube.com/watch?v=WPdJaBFquNc]

in this Next.js tutorial we'll see how to use route parameters.
- on clicking on the name detal page should be apeared

## #12 - Dynamic Routes (part 2 - getStaticPaths)
[https://www.youtube.com/watch?v=mAHqpdVzJmA]

in this Next.js tutorial we'll see how to use the getStaticPaths function to generate pages for each of our dynamic routes.
- Create new file [id].js in /pages/ninjas folder

## #13 - Fetching a Single Item
[https://www.youtube.com/watch?v=2zRHlqc0_yw]

In previous tutorial, we use getStaticProps function to retrieve remote api and render ninjas list. But if we want to fetch a single ninja item, we have to apply both getStaticProps and getStaticPaths function inside dynamic route componet ([id].js/detail page component)
Q: Why do we need getStaticPaths function ? A: Because we need to tell Nextjs how many html page needed to be made base on 


---------------------------------------------------------
---------------------------------------------------------
This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
