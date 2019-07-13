

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
11. 