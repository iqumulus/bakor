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

Build it using `bakor` in the project directory.

Less files are of course optional. If you do use less, each less file supplied in the array will result in *a separate css file*. The idea is to include a single less file which uses `import` to fetch the rest of them. This way it's easy to several different color schemes etc. 
