

How I created my Nuxt App 

*Based on educational material from Vue Mastery*

1. npx create-next-app <projectname> 

   1. Initialize a repo and fetch dependencies

   2. Select with Universal Mode

   3. ![image-20190713080820521](/Users/jsick/Library/Application Support/typora-user-images/image-20190713080820521.png) settings for my nuxt project

   4. continue to follow directions and cd into the directory

      To get started:

      ```
      cd nuxt
      npm run dev
      ```

        To build & start for production:

      ```
      cd nuxt
      npm run build
      npm run start
      ```

   5. preview on port whatever 3000 for now

   6. 

![image-20190713082136602](/Users/jsick/Library/Application Support/typora-user-images/image-20190713082136602.png)

7. Add to GitHub

```
git remote add origin https://github.com/jannaee/nuxt-app.git
git push -u origin master (to get files into master branch)
```

8. The initial layout of directories and the purpose of each

   -Root

   ​	- Layouts (ex, home layout, store layout, etc)

   ​	- Pages (contains our top level views, and the files in this directory creates our routes)

   ​	- Components (contains the reusable vue components)

   ​	-Store (contains the vuex store files)

   ​	-Static (files we want served the way they are directly from the root like the favicon and the robots.txt)

   ​	- Assets(uncompiled assets like images fonts sass)

*Special note: Nuxt uses the vue loader file loader and url loader for effective asset serving like caching imgages and distributing the website's assets only if the files have changed.*

​		- Plugins (js plugins to load before starting vue app)

​		- Middleware (custom functions to run before rendering a layout or page)

​		- nuxt.config.js (used to moifut the default nuxt configuration)

![img](https://d2mxuefqeaa7sj.cloudfront.net/s_4843393BE943192D4CA144BAAA96C727A13C6E324445331C8FAE92B7DB2241FF_1549297156398_Creating+a+Nuxt+App-3.jpg)

9. For my project I have included index.vue file and create.vue file in the pages folder. by default a router.js file will automatically be created.
10. After modifying vue files use npm run dev to spin up a developmental server



**What is Universal Mode?**

In single page application is only fast after it's initial load. Otherwise it's very slow for the first load.

![img](https://d2mxuefqeaa7sj.cloudfront.net/s_7E49D7BF693B737F1E5819C7D8D74A723243CD29B7BABE49C29CF05DB4EACDDB_1550076033286_single-page-app.jpg)

A solution is to create a Universal application or one that is created in Nuxt in universal mode)

![image-20190713174312393](/Users/jsick/Library/Application Support/typora-user-images/image-20190713174312393.png).

in short the request is made to the server and a static html file is served up and immeadiately sent to the browser to be rendered for the user.

in the background the other requests are contiuning to load and once complete it will start up Vue making the website perform like a single page application.

It allows html to be rendered server side before it's displayed. Even without JS not loading you can see in the network panel, under localhost, and response the html is served.

Once Vue starts in the browser  files are loaded based on code splitting. 

What to notice here is that a JavaScript request is made to pull over just the JavaScript needed to render the `/about-us` page component. This is because Nuxt uses code-splitting by default and will split each of our pages into different JavaScript files which are loaded only when needed. 

**What is Smart prefetching**

A feature combined with Universal mode that provides even better experience by automaticall prefetching code split pages linked with nuxt-link once these components are visible on the viewport.

Once the link is clicked the JS file is executed immediately instead of waiting for a network request.

![img](https://d2mxuefqeaa7sj.cloudfront.net/s_7E49D7BF693B737F1E5819C7D8D74A723243CD29B7BABE49C29CF05DB4EACDDB_1550604027102_animation2-opt.gif)





**SEO with vue-meta**

![image-20190713180937332](/Users/jsick/Library/Application Support/typora-user-images/image-20190713180937332.png)

also the Client side js websites don't rank high for SEO 

SEO Basics

- Needs it's own title tag and meta description

Vue meta is a library built into nuxt. I'm skipping this for now but if I want to revisit go here: https://github.com/Code-Pop/real-world-nuxt/releases/tag/lesson-4-seo-finish

 **Files Based routing**

Lessons to cover: 

How to create Nested routes

Dynamic Routing

And replace the default Error Page

![image-20190713181756715](/Users/jsick/Library/Application Support/typora-user-images/image-20190713181756715.png)

Use an underscore as a prefix for dynamic routes

!![image-20190713183919525](/Users/jsick/Library/Application Support/typora-user-images/image-20190713183919525.png)image-20190713183845484](/Users/jsick/Library/Application Support/typora-user-images/image-20190713183845484.png)

**API Calls with Axios**

npm install -g son-server