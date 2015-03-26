# bakor
Simple JavaScript, CSS, and LESS baker.

## Usage

`npm install -g bakor`

Create a `bakor.json` file in your project:

    
    {
      "name": "<name of app>",
      "outputDir": "./build",  

      "js": [
        "path/to/jsfile1",
        "path/to/jsfile2"
      ],
      "css": [
        "path/to/cssfile1",
        "path/to/cssfile2"
      ],
      "less": [
        "path/to/lessfile"
      ]
    }

Build it using `bakor` in the project directory. This will result in the following files in `outputDir`:
  * [app name].js - Baked JavaScript (if JavaScript files are supplied)
  * [app name].min.js - Baked + minified JavaScript (if JavaScript files are supplied)
  * [app name].css - Baked CSS (if CSS files are supplied)
  * [app name].min.css - Baked + minified CSS (if CSS files are supplied)
  * [app name + less filename].css - Baked less CSS (if less files are supplied)
  * [app name + less filename].min.css - Baked + minified less CSS (if less files are supplied)

If less files are used, each less file supplied in the array will result in **a separate css file**. The idea is to include a single less file which uses `import` to fetch the rest of them. This way it's easy to bake several different color schemes etc. 

## License

MIT. See LICENSE file.