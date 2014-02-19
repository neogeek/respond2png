#respond2png

> A simple bash script for creating multiple screenshots of a responsive design. Requires [webkit2png](https://github.com/paulhammond/webkit2png/).

##Usage

```bash
Usage: respond2png [options] [http://localhost/]

Options:
   -v, --version             show the version number and then exit
   -h, --help                show this help message and then exit

   -i, --ios                 create iOS device sizes
   -a, --android             create Android device sizes

   -l, --landscape           create landscape versions
   -r, --retina              create retina versions

   -o=name, --output=name    change name of saved files
```

##Screen Sizes

| Device | Orientation | Width |
| ------ | ----------- | ---- |
| iPhone | Portrait | 320 |
| iPhone | Landscape | 568 |
| iPad | Portrait | 768 |
| iPad | Landscape | 1024 |
| Nexus5 | Portrait | 360 |
| Nexus5 | Landscape | 600 |
| Nexus7 | Portrait | 600 |
| Nexus7 | Landscape | 960 |
| Nexus10 | Portrait | 800 |
| Nexus10 | Landscape | 1280 |
| Desktop | n/a | 1440 |

##Grunt Setup

```javascript
grunt.loadNpmTasks('grunt-shell');

grunt.initConfig({
    shell: {
        respond2png: {
            command: 'respond2png http://localhost/ --ios --android'
        }
    }
});

grunt.registerTask('default', ['shell:respond2png']);
```