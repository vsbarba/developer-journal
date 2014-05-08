```javascript
/*global module:false*/
module.exports = function (grunt) {

  /** 
   * Load required Grunt tasks. These are installed based on the versions listed
   * in `package.json` when you do `npm install` in this directory.
   */
   
  grunt.loadNpmTasks('grunt-contrib-watch');
  grunt.loadNpmTasks('grunt-contrib-less');

  // Project configuration.
  grunt.initConfig({

    /**
     * We read in our `package.json` file so we can access the package name and
     * version. It's already there, so we don't repeat ourselves here.
     */
    pkg: grunt.file.readJSON("package.json"),

    // Configuration Directory


    // Metadata
    // =====================================
    meta: {
      version: '0.1.0'
    },
    
    // Watch Less stylesheets
    // =====================================
    watch: {
      less: {
        files: ['_source/less/**/*.less'],
        tasks: ['less:development']
      }
    },

    // Compile Less stylesheets
    // =====================================
    less: {
      development: {
        options: {
          strictMath: true,
          sourceMap: false
        },
        files: {
          "application/assets/css/bootstrap.css": "_source/less/bootstrap.less",
        }
      }
    }

  });


  // Watch CSS Development
  grunt.registerTask('watchless', ['watch']);

};
```
