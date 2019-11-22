# amdefine

Images in the CSS file path can be converted into an absolute path, and add the CDN prefix

## Install

```javascript
npm install gulp-css-path --save-dev
```

## Usage

```javascript
const cssUrlToAbsolute = require('gulp-css-path');
gulp.task('CSS_build', function() {
    return gulp.src(['./src/**/*.css'])
        .pipe(cssUrlToAbsolute({
            //relative path
            root: './src',
            //cdn prefix
            cdnpath: '//img.xxx.com/dist/img/'
        }))
        .pipe(gulp.dest(DIST_PATH))
});
```
## example
**1)** css
```css
.label {
    width: 57px;
    height: 69px;
    background: url(../../common/img/label.png) center center no-repeat;
}
```
**2)** convert after

```css
.label {
    width: 57px;
    height: 69px;
    background: url(//img.xxx.com/dist/img/help/label/common/img/label.png) center center no-repeat;
}
```

## License

New BSD and MIT. Check the LICENSE file for all the details.
