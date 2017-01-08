# Using SCSS

- Website: http://sass-lang.com/
- Docs: http://sass-lang.com/guide

## Global Setup

Install on OS X: `sudo gem install sass`

## CLI Usage

Version info: `sass -v`
Compile: `sass styles.scss styles.css`
Auto-Compile for single files: `sass --watch styles.scss:styles.css`
Auto-Compile for folders: `sass --watch .`
Auto-Compile for folders without sourcemap: `sass --sourcemap=none --style compressed --watch [from_folder]:[to_folder]`

## Color Functions

| SCSS Code | Description |
| --- | --- |
| `rgb(100, 120, 140)` | Creates color from given values |
| `rgba(100, 120, 140, .5)` | Creates color from given values |
| `rgba($color, .5)` | Creates color from given values with given opacity |
