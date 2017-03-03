# gulp-practice

##Setup Guide
###-npm install gulp-g
###-npm init
###-npm install gulp --save-dev
###-create gulpfile.js (Preferably root level)
###-(in gulpfile.js)
###-You can create 'tasks', and run them using 'gulp "task-name"'

```javascript
var gulp = require('gulp');
var sass = require('gulp-sass');

//Pre-processing structure
// gulp.task('sass', function(){
//   return gulp.src('source-files')
//     .pipe(sass()) // Using gulp-sass
//     .pipe(gulp.dest('destination'))
// });

gulp.task('sass', function(){
  return gulp.src('app/scss/*.scss')
    .pipe(sass()) // Converts Sass to CSS with gulp-sass
    .pipe(gulp.dest('app/css'))
});

// Gulp watch syntax
// gulp.watch('files-to-watch', ['tasks', 'to', 'run']);

gulp.task('watch', function(){
  gulp.watch('app/scss/*.scss', ['sass']);
  // Other watchers
});
```
