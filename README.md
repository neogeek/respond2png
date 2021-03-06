# respond2png

> A simple bash script for creating multiple screenshots of a responsive design. Requires [webkit2png](https://github.com/paulhammond/webkit2png/).

## Install

```bash
$ curl https://raw.githubusercontent.com/neogeek/respond2png/master/respond2png -o /usr/local/bin/respond2png && chmod +x /usr/local/bin/respond2png
```

## Usage

```bash
Usage: respond2png [options] [http://localhost/]

OPTIONS:
   -v, --version             show the version number and then exit
   -h, --help                show this help message and then exit

   -i, --ios                 create iOS device sizes
   -a, --android             create Android device sizes

   -l, --landscape           create landscape versions
   -r, --retina              create retina versions

   -o=name, --output=name    change name of saved files
```

## Screen Sizes

| Device | Orientation | Width |
| ------ | ----------- | ---- |
| iPhone 6 | Portrait | 375 |
| iPhone 6 | Landscape | 667 |
| iPhone 6 Plus | Portrait | 414 |
| iPhone 6 Plus | Landscape | 736 |
| iPhone 5 | Portrait | 320 |
| iPhone 5 | Landscape | 568 |
| iPad | Portrait | 768 |
| iPad | Landscape | 1024 |
| Nexus5 | Portrait | 360 |
| Nexus5 | Landscape | 600 |
| Nexus7 | Portrait | 600 |
| Nexus7 | Landscape | 960 |
| Nexus10 | Portrait | 800 |
| Nexus10 | Landscape | 1280 |
| Desktop | n/a | 1440 |

## Grunt Setup

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
