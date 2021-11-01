# Setup instructions

## deployment project
run command
``` bash
# install dependencies
$ npm install
```

## added .nuxt folder to .gitignore 
after installing npm, nuxt.js generated service files that are located in the .nuxt folder. There is no need to track changes in this folder. This folder has been added to .gitignore.

## set home-start-up template
to select the template home-start-up template, you need to transfer all code from the /pages/home-start-up.vue file to the index.vue file

## github pages
changed nuxt.config. to work with github<br />
added a prefix (path) for all pictures. So that pictures can be displayed on github pages

to deploy the project need to change the value in the field - router.base: '/demo-brook-vue-theme'<br />
for local development or if the project will be moved to a live server, <br />
then you need to change the value to - router.base: '/'<br />
then you need to create (or change if it already exists) a branch to gh-pages<br />
and run command
``` bash
$ npm run generate
```
It will create a dist folder with everything inside ready to be deployed on GitHub Pages hosting<br />

then need add and commit the dist folder
``` bash
git add dist && git commit -m "Initial dist subtree commit demo-brook-vue-theme"
```
then need to push the dist folder to the root of the gh-pages branch
``` bash
git subtree push --prefix dist https://github.com/mlmedia/demo-brook-vue-theme.git gh-pages
```
then need to activate the gh-pages branch on the github<br />
1) Go to Settings - https://prnt.sc/1w8uh2k<br />
2) Click on Pages - https://prnt.sc/1w8um2o<br />
3) Click on Source > gh-pages - https://prnt.sc/1w8vekx<br />
and click save

## Added content for Home, About Us, Services, Portfolio, Contact
### create files and upload images:
create pages:<br />
/pages/about-us.vue<br />
/pages/contact-us.vue<br />
/pages/portfolio.vue<br />
/pages/services.vue<br />
create components:<br />
/components/custom/ContactModern.vue<br />
/components/custom/ContactUsBreadcrumb.vue<br />
/components/custom/EffectiveSolution.vue<br />
/components/custom/HeaderBlack.vue<br />
/components/custom/HeroEssential.vue<br />
/components/custom/Navigation.vue<br />
/components/custom/ServiceModern.vue<br />
/components/custom/ServiceModernBreadcrumb.vue<br />
/components/custom/WhatNext.vue<br />
upload images in /static/images

### create commit for demo-stratup branch and push on github:
``` bash
git add .
git commit -m "add content: home, about, services, portfolio, contact"
git push orign
```

### generate static files and push on github pages:
switch branch on gh-pages<br />
change root path in nuxt.config.js<br />
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
created a global style file - assets/scss/main.scss in layouts/default.vue <br />
added menu items for header navigation - components/custom/Navigation.vue 

### added brands for "About Us" page and added content
created component - components/custom/Brands.vue<br />
added team members in file - pages/about-us.vue <br />
uploaded images to team members to folder - static/images/about-us/<br />
uploaded brand images to folder - static/images/brands/

### Mobile navigation
updated header mobile files:<br />
            - components/HeaderForOffCanvas.vue<br />
            - components/HeaderForOffCanvasBlack.vue <br />
            - components/OffCanvasMobileMenu.vue <br />
created component for menu list - components/custom/MobileNavigation.vue 

### Blog page, Blog details page
created blog page - pages/blog/index.vue<br />
created component for list item - components/custom/BlogPostFour.vue<br />
updated detail blog page - pages/blog/_id.vue<br />
uploaded images - static/images/blog/blog-1.jpeg

### Press page
created press page - pages/press.vue 

### Added logos
uploaded logo images to folder - static/images/app/<br />
changed logo images in files<br />
    - components/custom/HeaderElement.vue <br />
    - components/custom/HeaderBlack.vue <br />
    - components/custom/HeaderAbout.vue 

### Added images for the press page
uploaded images to folder - static/images/press/