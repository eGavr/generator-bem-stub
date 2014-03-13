# generator-bemgen

A generator for [Yeoman](http://yeoman.io).

## Install

```
$ npm install -g yo

$ git clone https://github.com/eGavr/generator-bemgen.git

$ cd generator-bemgen

$ npm link
```

## Usage

Run from any directory you want:

```
$ yo bemgen
```

or use ```JSON-file``` with answers as the parameter:

```
$ yo bemgen FULL_PATH_TO_JSON-FILE
```

For example, we have the file with answers ```example.json``` which lies in the directory where we want to create the project:

```
{
  "projectName": "example",
  "author": "Ivan Ivanov",
  "email": "ivan@yandex.ru",
  "collector": "bem",
  "baseLibrary": { "name": "bem-bl", "version": "support/1.x" },
  "addLibraries": [],
  "platforms": [ "common", "desktop" ],
  "localization": false,
  "techs": []
}
```

Run:

```
$ yo bemgen example.json
```

```generator-bemgen``` will take the content of ```example.json``` as answers.

Go to the ```test/basic``` and see more examples of ```JSON-files```.

## Assembly

As soon as you answer all questions you will have to assembly the created project:

```
$ cd THE_NAME_OF_YOUR_PROJECT

$ npm i

$ ./node_modules/.bin/bem make
```

You can use the parameter ```+a``` to automate the assembly:

```
$ yo bemgen +a

$ yo bemgen FULL_PATH_TO_JSON-FILE +a
```

## Tests

Run from the root folder of ```generator-bemgen```:

```$ cd test```

Then run:

```$ ./run.sh +a``` or ```$ ./run.sh -basic +a``` - to check the created files and the assembly of the projects (higher quality testing, but slower)

```$ ./run.sh``` or ```$ ./run.sh -basic``` - to check only the created files of the projects (lower quality testing, but faster)

## License

[MIT License](http://en.wikipedia.org/wiki/MIT_License)
