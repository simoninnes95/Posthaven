# The Posthaven Classic Theme

## Theme Building Resources

* [Posthaven theme documentation](http://theme-docs.posthaven.com/)
* See the [posthaven_theme](https://github.com/posthaven/posthaven_theme) gem for theme file upload via the API.


## Building Stylesheets

### Install Gems

Install [bundler](http://bundler.io) and run:
```
bundle install
```

### Building SCSS

Build `assets/blog.css`:
```
rake compile
```

Watch `src/blog.scss` and build on update:
```
rake watch
```

## Uploading to Posthaven

Theme files are uploaded using the `phtheme` CLI from the [`posthaven_theme`](https://github.com/posthaven/posthaven_theme) gem.

### One-time setup

Get your API key from [posthaven.com/account/theme_api_key](https://posthaven.com/account/theme_api_key), then run:
```
phtheme configure <your-api-key>
```
This generates a `config.yml` file in the project root. **Do not commit this file to version control.**

### Upload all files
```
phtheme upload
```

### Upload a single file
```
phtheme upload assets/blog.css
```

### Replace all remote theme files with local versions
```
phtheme replace
```

### Watch and auto-upload on change
```
phtheme watch
```

> If `phtheme` is not on your PATH, use the local binary at `vendor/posthaven_theme/bin/phtheme`.

## Screenshot

![Screenshot](/assets/screenshot.png?raw=true)
