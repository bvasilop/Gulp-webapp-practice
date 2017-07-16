# Gulp-webapp-practice
practice installing gulp yeoman workflow

**Steps for installing Gulp, Webapp and Yeoman**
1) Create repo in Github.

2) Clone repo to local machine in terminal:   **git clone "git@github.com:{github user name}/{project name}.git"**

3) Enter proper project directory:   **cd Gulp-webapp-practice**

4) Install Webapp:   **npm install -g generator-webapp**

5) Install Yeoman scaffolding Webapp:  **yo webapp**

6)  Which additional features would you like to include?   **Sass, Bootstrap, Modernizr**

7) Which version of Bootstrap would you like to include?   **Bootstrap 4**

8) Choose your style of DSL:   **TDD**

9) Install Gulp:   **gulp serve**

10) Test Gulp:   **gulp serve:test**

11) Run Gulp:   **gulp**

12) Run gulp on server:   **gulp serve:dist**

13) Run gulp tasks:   **gulp --tasks**

14) Setup to publish on Github Pages:  **npm install --save-dev gulp-gh-pages**

15) Enter Gulpfile.js and add the following:  **const ghPages = require('gulp-gh-pages');

gulp.task('deploy', function() {
return gulp.src('./dist/**/*')*
  **.pipe(ghPages());
});**

16) Final Changes in Gulpfile.js should look like this in text editor:   
**const gulp = require('gulp');
const gulpLoadPlugins = require('gulp-load-plugins');
const browserSync = require('browser-sync').create();
const del = require('del');
const wiredep = require('wiredep').stream;
const runSequence = require('run-sequence');
const ghPages = require('gulp-gh-pages');
const $ = gulpLoadPlugins();
const reload = browserSync.reload;
gulp.task('deploy', function() {
return gulp.src('./dist/**/*')*
  **.pipe(ghPages());
});**

17) Add changes to gh-pages:  **git add -A**

18) Commit changes to gh-pages:   **git commit -m "added gulp yeoman"**

19) Push changes to gh-pages:    **git push origin**

20) Completed and should be able to be viewed in gh-pages.
