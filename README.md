React Flickity Component
=======================

[![Greenkeeper badge](https://badges.greenkeeper.io/theolampert/react-flickity-component.svg)](https://greenkeeper.io/)
[![build status](https://travis-ci.org/theolampert/react-flickity-component.svg?branch=master)](https://travis-ci.org/theolampert/react-flickity-component/)
[![dependencies](https://david-dm.org/theolampert/react-flickity-component.svg)](https://david-dm.org/theolampert/react-flickity-component)
[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

#### Introduction:
A React.js Flickity component.

#### Install:

```shell
npm install react-flickity-component --save
// Or
yarn add react-flickity-component
```

#### Usage:

```javascript
// Commonjs
const Flickity = require('flickity');
// Or for ES2015 module
import Flickity from 'react-flickity-component/src/index'

const flickityOptions = {
    initialIndex: 2
}

function Carousel() {
  this.flickityInstance = null
  
  this.handleInitialize = function (flickityInstance) {
    this.flickityInstance = flickityInstance
  }

  this.handleInitialize = this.handleInitialize.bind(this)

  return (
    <Flickity
      className={'carousel'} // default ''
      initialize={this.handleInitialize}
      elementType={'div'} // default 'div'
      options={flickityOptions} // takes flickity options {}
      disableImagesLoaded={false} // default false
      reloadOnUpdate // default false
    >
      <img src="/images/placeholder.png"/>
      <img src="/images/placeholder.png"/>
      <img src="/images/placeholder.png"/>
    </Flickity>
  )
}

```
#### Example usage:
The examples folder contains an example use with create-react-app.

```
cd examples/react-flickity
yarn
yarn start
```

#### Props:

##### className={String}
`className` applied to top level component.

##### initialize={Func}
Runs after the Flickity instance is ready, passes the Flickity instance as an argument

##### elementType={String}
What kind of DOM element to render, defaults to 'div'

##### options={Object}
Any options you would normally initialise flickity with

##### disableImagesLoaded={Boolean}
If you want to disable images loaded

##### reloadOnUpdate
Runs flickity's `reloadCells()` on `componentDidUpdate` lifecycle method

export default Carousel


#### License Information:
Flickity may be used in commercial projects and applications with the one-time purchase of a commercial license.
http://flickity.metafizzy.co/license.html
