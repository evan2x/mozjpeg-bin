# mozjpeg-bin

> [mozjpeg](https://github.com/mozilla/mozjpeg) is a production-quality JPEG encoder that improves compression while maintaining compatibility with the vast majority of deployed decoders

You probably want [`@evan2x/imagemin-mozjpeg`](https://github.com/evan2x/imagemin-mozjpeg) instead.


## Install

```
$ npm install @evan2x/mozjpeg-bin
```

Compared with the official package, this package supports setting the mirror URL. You can set the download URLs of its binary files in the following two ways:

1. Set the npm config property `imagemin_cdnurl`.

```sh
npm install @evan2x/mozjpeg-bin --imagemin_cdnurl=https://npmmirror.com/mirrors
```

2. Set the environment variables.

```sh
IMAGEMIN_CDNURL=https://npmmirror.com/mirrors npm install @evan2x/mozjpeg-bin
```

## Usage

```js
import {execFile} from 'node:child_process';
import mozjpeg from '@evan2x/mozjpeg-bin';

execFile(mozjpeg, ['-outfile', 'output.jpg', 'input.jpg'], err => {
	console.log('Image minified!');
});
```


## CLI

```
$ npm install --global @evan2x/mozjpeg-bin
```

```
$ mozjpeg --help
```


## License

MIT © [Imagemin](https://github.com/imagemin)
