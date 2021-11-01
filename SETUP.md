# Setup instructions

## deployment project
run command
``` bash
# install dependencies
$ npm install
```

## add .nuxt folder to .gitignore 
after installing npm, nuxt.js generated service files that are located in the .nuxt folder. There is no need to track changes in this folder. This folder has been added to .gitignore.

## set home-start-up template
to select the template home-start-up template, you need to transfer all code from the /pages/home-start-up.vue file to the index.vue file

## github pages
changed nuxt.config. to work with github
added a prefix (path) for all pictures. So that pictures can be displayed on github pages

to deploy the project need to change the value in the field - router.base: '/demo-brook-vue-theme'
for local development or if the project will be moved to a live server, 
then you need to change the value to - router.base: '/'
then you need to create (or change if it already exists) a branch to gh-pages
and run command
``` bash
$ npm run generate
```
It will create a dist folder with everything inside ready to be deployed on GitHub Pages hosting

then need add and commit the dist folder
``` bash
git add dist && git commit -m "Initial dist subtree commit demo-brook-vue-theme"
```
then need to push the dist folder to the root of the gh-pages branch
``` bash
git subtree push --prefix dist https://github.com/mlmedia/demo-brook-vue-theme.git gh-pages
```
then need to activate the gh-pages branch on the github
1) Go to Settings - https://prnt.sc/1w8uh2k
2) Click on Pages - https://prnt.sc/1w8um2o
3) Click on Source > gh-pages - https://prnt.sc/1w8vekx
and click save

## add content for Home, About Us, Services, Portfolio, Contact
### create files and upload images:
create pages:
/pages/about-us.vue
/pages/contact-us.vue
/pages/portfolio.vue
/pages/services.vue
create components:
/components/custom/ContactModern.vue
/components/custom/ContactUsBreadcrumb.vue
/components/custom/EffectiveSolution.vue
/components/custom/HeaderBlack.vue
/components/custom/HeroEssential.vue
/components/custom/Navigation.vue
/components/custom/ServiceModern.vue
/components/custom/ServiceModernBreadcrumb.vue
/components/custom/WhatNext.vue
upload images in /static/images

### create commit for demo-stratup branch and push on github:
``` bash
git add .
git commit -m "add content: home, about, services, portfolio, contact"
git push orign
```

### generate static files and push on github pages:
switch branch on gh-pages
change root path in nuxt.config.js
router.base: '/' to router.base: '/demo-brook-vue-theme'

run command: 
``` bash
npm run generate
```

add commit 
``` bash
git add dist && git commit -m "add content: home, about, services, portfolio, contact"
```

push new static files on GitHub
``` bash
git push origin `git subtree split --prefix dist gh-pages`:gh-pages --force
```

## Created pages and css edits
created a global style file - assets/scss/main.scss in layouts/default.vue 
added menu items for header navigation - components/custom/Navigation.vue 

### added brands for "About Us" page and added content
created component - components/custom/Brands.vue
added team members in file - pages/about-us.vue 
uploaded images to team members to folder - static/images/about-us/
uploaded brand images to folder - static/images/brands/

### Mobile navigation
updated header mobile files - components/HeaderForOffCanvas.vue
                            - components/HeaderForOffCanvasBlack.vue 
                            - components/OffCanvasMobileMenu.vue 
created component for menu list - components/custom/MobileNavigation.vue 

### Blog page, Blog details page
created blog page - pages/blog/index.vue
created component for list item - components/custom/BlogPostFour.vue 
updated detail blog page - pages/blog/_id.vue 
uploaded images - static/images/blog/blog-1.jpeg 

### Press page
created press page - pages/press.vue 

### Add logos
uploaded logo images to folder - static/images/app/
changed logo images in files - components/custom/HeaderElement.vue 
                             - components/custom/HeaderBlack.vue 
                             - components/custom/HeaderAbout.vue 

