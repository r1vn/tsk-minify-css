minifies all css files in the specified directory

uses [clean-css](https://github.com/jakubpawlowicz/clean-css) as the minifier

## setup

- download [tsk-minify-css.tar.xz](https://github.com/r1vn/tsk-minify-css/raw/master/tsk-minify-css.tar.xz) and unpack as `your-project/lib/tsk-minify-css`
- add a config entry to the manifest

example config: minifying all .css files in `build` directory

```
{
    module: 'lib/tsk-minify-css',
    config:
    {
        // path of the directory to look for files to minify in
        dir: 'build',
        // filter function applied to files in the dir
        filter: path => path.endsWith('.css'),
        // https://github.com/jakubpawlowicz/clean-css#constructor-options
        // lib/tsk-minify-css/node_modules/clean-css/README.md
        opts: 
        {

        }
    }
}
```