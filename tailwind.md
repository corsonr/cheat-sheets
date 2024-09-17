# Adding Tailwind CSS to WordPress Plugins

This guide explains how to add Tailwind CSS support to WordPress plugins with a common file structure.

## Prerequisites

- Node.js and npm installed on your system
- A WordPress plugin with a structure similar to:
  ```
  plugin-name/
  ├── includes/
  │   └── class-plugin-name.php
  ├── assets/
  │   ├── css/
  │   └── js/
  └── plugin-name.php
  ```

## Steps

1. **Initialize npm and install dependencies**

   In your plugin's root directory, run:
   ```bash
   npm init -y
   npm install tailwindcss postcss autoprefixer
   ```

2. **Create Tailwind configuration file**

   Run:
   ```bash
   npx tailwindcss init
   ```

3. **Update `tailwind.config.js`**

   ```javascript:tailwind.config.js
   module.exports = {
     content: [
       './includes/**/*.php',
       './assets/**/*.js',
     ],
     theme: {
       extend: {
         colors: {
           primary: {
             50: '#faf8fc',
             100: '#f2eef9',
             200: '#e9e0f4',
             300: '#d7c8ea',
             400: '#bca4dc',
             500: '#a280cc',
             600: '#7f54b3',
             700: '#754fa1',
             800: '#634584',
             900: '#51386b',
             950: '#35204b',
           },
         },
       },
     },
     plugins: [],
   }
   ```

4. **Create PostCSS configuration**

   Create `postcss.config.js` in the plugin root:
   ```javascript:postcss.config.js
   module.exports = {
     plugins: {
       tailwindcss: {},
       autoprefixer: {},
     }
   }
   ```

5. **Create Tailwind CSS file**

   Create `assets/css/tailwind.css`:
   ```css:assets/css/tailwind.css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

6. **Add build script**

   In `package.json`, add:
   ```json:package.json
   {
     "scripts": {
       "build": "tailwindcss -i ./assets/css/tailwind.css -o ./assets/css/style.css --minify",
   	   "start": "tailwindcss -i ./assets/css/tailwind.css -o ./assets/css/style.css --watch"
     }
   }
   ```

7. **Build CSS**

   Run:
   ```bash
   npm run build
   ```

8. **Update enqueue method**

   In your main plugin class (e.g., `includes/class-plugin-name.php`), update the `enqueue_scripts` method:
   ```php:includes/class-plugin-name.php
   public function enqueue_scripts() {
       wp_enqueue_style( 'plugin-name-style', plugin_dir_url( __DIR__ ) . 'assets/css/style.css', array(), filemtime( plugin_dir_path( __DIR__ ) . 'assets/css/style.css' ) );
       wp_enqueue_script( 'plugin-name-script', plugin_dir_url( __DIR__ ) . 'assets/js/scripts.js', array( 'jquery' ), filemtime( plugin_dir_path( __DIR__ ) . 'assets/js/scripts.js' ), true );
   }
   ```

9. **Ensure enqueue action is added**

   In the constructor of your main plugin class:
   ```php:includes/class-plugin-name.php
   public function __construct() {
       add_action( 'wp_enqueue_scripts', array( $this, 'enqueue_scripts' ) );
       // Other actions...
   }
   ```

## Usage

- Use Tailwind classes in your PHP files.
- Run `npm run build` after making changes to Tailwind classes or configuration.
- The generated CSS will be in `assets/css/style.css`.

## Notes

- Adjust file paths if your plugin structure differs.
- Consider using a watch script for development to automatically rebuild CSS.
