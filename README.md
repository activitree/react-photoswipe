# React PhotoSwipe

PhotoSwipe, PhotoSwipeGallery component for ReactJS base on [PhotoSwipe](http://photoswipe.com/).

## Installation

### NPM

```bash
npm install --save react-photoswipe
```

### Bower
```bash
bower install --save react-photoswipe
```

## Usage

### Styles

#### With webpack:

```js
import 'react-photoswipe/lib/photoswipe.css';
```

#### Without webpack:

```html
<link rel="stylesheet" type="text/css" href="path/to/react-photoswipe/lib/photoswipe.css">
```

### JS

#### PhotoSwipe

```js
import {PhotoSwipe} from 'react-photoswipe';

let isOpen = true;

let items = [
  {
    src: 'http://lorempixel.com/1200/900/sports/1',
    w: 1200,
    h: 900,
    title: 'Image 1'
  },
  {
    src: 'http://lorempixel.com/1200/900/sports/2',
    w: 1200,
    h: 900,
    title: 'Image 2'
  }
];

let options = {
  //http://photoswipe.com/documentation/options.html
};

handleClose = () => {
  isOpen: false
};

<PhotoSwipe isOpen={isOpen} items={items} options={options} onClose={handleClose}/>

```

#### PhotoSwipeGallery

```js
import {PhotoSwipeGallery} from 'react-photoswipe';

let items = [
  {
    src: 'http://lorempixel.com/1200/900/sports/1',
    thumbnail: 'http://lorempixel.com/120/90/sports/1',
    w: 1200,
    h: 900,
    title: 'Image 1'
  },
  {
    src: 'http://lorempixel.com/1200/900/sports/2',
    thumbnail: 'http://lorempixel.com/120/90/sports/2',
    w: 1200,
    h: 900,
    title: 'Image 2'
  }
];

let options = {
  //http://photoswipe.com/documentation/options.html
};

getThumbnailContent = (item) => {
  return (
    <img src={item.thumbnail} width={120} height={90}/>
  );
}

<PhotoSwipeGallery items={items} options={options} thumbnailContent={getThumbnailContent}/>
```

### UMD

```html
<link rel="stylesheet" type="text/css" href="path/to/react-photoswipe/dist/photoswipe.css">
<script src="path/to/react-photoswipe/dist/react-photoswipe.js"></script>
```

```js
var PhotoSwipe = window.ReactPhotoswipe.PhotoSwipe;
var PhotoSwipeGallery = window.ReactPhotoswipe.PhotoSwipeGallery;
```

Example [here](http://codepen.io/vn38minhtran/pen/XmVdvW/)

## Props

**Note:**  The first argument of every listener is a Photoswipe instance.

EX:
```js
beforeChange(instance, change);
imageLoadComplete(instance, index, item);
```

### PhotoSwipe

| Name | Type | Default | Required | Description |
|------|------|---------|----------|-------------|
| isOpen | bool | false | true |  |
| items | array | [] | true | http://photoswipe.com/documentation/getting-started.html |
| options | object | {} | false | http://photoswipe.com/documentation/options.html |
| onClose | function |  | false | Callback after PhotoSwipe close |
| beforeChange | func |  | false | Photoswipe event listener |
| afterChange | func |  | false | Photoswipe event listener |
| imageLoadComplete | func |  | false | Photoswipe event listener |
| resize | func |  | false | Photoswipe event listener |
| gettingData | func |  | false | Photoswipe event listener |
| mouseUsed | func |  | false | Photoswipe event listener |
| initialZoomIn | func |  | false | Photoswipe event listener |
| initialZoomInEnd | func |  | false | Photoswipe event listener |
| initialZoomOut | func |  | false | Photoswipe event listener |
| initialZoomOutEnd | func |  | false | Photoswipe event listener |
| parseVerticalMargin | func |  | false | Photoswipe event listener |
| close | func |  | false | Photoswipe event listener |
| unbindEvents | func |  | false | Photoswipe event listener |
| destroy | func |  | false | Photoswipe event listener |
| updateScrollOffset | func |  | false | Photoswipe event listener |
| preventDragEvent | func |  | false | Photoswipe event listener |
| shareLinkClick | func |  | false | Photoswipe event listener |

### PhotoSwipeGallery

| Name | Type | Default | Required | Description |
|------|------|---------|----------|-------------|
| items | array | [] | true | http://photoswipe.com/documentation/getting-started.html |
| options | object | {} | false | http://photoswipe.com/documentation/options.html |
| thumbnailContent | function | `<img src={item.src} width='100' height='100'/>` | false | Thumbnail content |
| beforeChange | func |  | false | Photoswipe event listener |
| afterChange | func |  | false | Photoswipe event listener |
| imageLoadComplete | func |  | false | Photoswipe event listener |
| resize | func |  | false | Photoswipe event listener |
| gettingData | func |  | false | Photoswipe event listener |
| mouseUsed | func |  | false | Photoswipe event listener |
| initialZoomIn | func |  | false | Photoswipe event listener |
| initialZoomInEnd | func |  | false | Photoswipe event listener |
| initialZoomOut | func |  | false | Photoswipe event listener |
| initialZoomOutEnd | func |  | false | Photoswipe event listener |
| parseVerticalMargin | func |  | false | Photoswipe event listener |
| close | func |  | false | Photoswipe event listener |
| unbindEvents | func |  | false | Photoswipe event listener |
| destroy | func |  | false | Photoswipe event listener |
| updateScrollOffset | func |  | false | Photoswipe event listener |
| preventDragEvent | func |  | false | Photoswipe event listener |
| shareLinkClick | func |  | false | Photoswipe event listener |

## Demo

View [demo](http://vn38minhtran.github.io/react-photoswipe) or example folder.
