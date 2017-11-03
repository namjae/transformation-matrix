<!-- THIS IS AN AUTOGENERATED FILE. DO NOT EDIT THIS FILE DIRECTLY. -->
<!-- for your changes use misc/README.hbs file -->


# transformation-matrix
Isomorphic 2d transformation matrix functions written in ES6 syntax. Tree shaking ready!

[![Build Status](https://travis-ci.org/chrvadala/transformation-matrix.svg?branch=master)](https://travis-ci.org/chrvadala/transformation-matrix)
[![Coverage Status](https://coveralls.io/repos/github/chrvadala/transformation-matrix/badge.svg?branch=master)](https://coveralls.io/github/chrvadala/transformation-matrix?branch=master)
[![npm](https://img.shields.io/npm/v/transformation-matrix.svg?maxAge=2592000?style=plastic)](https://www.npmjs.com/package/transformation-matrix)
[![Downloads](https://img.shields.io/npm/dm/transformation-matrix.svg)](https://www.npmjs.com/package/transformation-matrix)
[![Beerpay](https://beerpay.io/chrvadala/transformation-matrix/badge.svg?style=beer)](https://beerpay.io/chrvadala/transformation-matrix)

## Setup
### NPM
```sh
  npm install transformation-matrix
```
### YARN
```sh
yarn add transformation-matrix
```
### UMD
```html
<script src="https://unpkg.com/transformation-matrix@1"></script>
```


## Usage example (ES6)
```js

import {scale, rotate, translate, transform, applyToPoint} from 'transformation-matrix';
//or
let {scale, rotate, translate, transform, applyToPoint} = window.TransformationMatrix;

let matrix = transform(
  translate(40,40),
  rotate(Math.PI/2),
  scale(2, 4)
);
let point = applyToPoint(matrix, {x: 42, y: 42});
```

## Live Demo
available at [http://chrvadala.github.io/transformation-matrix/](http://chrvadala.github.io/transformation-matrix/)

# Reference
## Functions

<dl>
<dt><a href="#applyToPoint">applyToPoint(matrix, point)</a> ⇒ <code>Object</code></dt>
<dd><p>Calculate a point transformed with an affine matrix</p>
</dd>
<dt><a href="#applyToPoints">applyToPoints(matrix, points)</a> ⇒ <code>array</code></dt>
<dd><p>Calculate an array of points transformed with an affine matrix</p>
</dd>
<dt><a href="#fromObject">fromObject(object)</a> ⇒ <code>Object</code></dt>
<dd><p>Extract an affine matrix from an object that contains a,b,c,d,e,f keys
Each value could be a float or a string that contains a float</p>
</dd>
<dt><a href="#fromString">fromString(string)</a> ⇒ <code>Object</code></dt>
<dd><p>Parse a string matrix formatted as matrix(a,b,c,d,e,f)</p>
</dd>
<dt><a href="#identity">identity()</a> ⇒ <code>Object</code></dt>
<dd><p>Identity matrix</p>
</dd>
<dt><a href="#inverse">inverse(matrix)</a> ⇒ <code>Object</code></dt>
<dd><p>Calculate a matrix that is the inverse of the provided matrix</p>
</dd>
<dt><a href="#isAffineMatrix">isAffineMatrix(object)</a> ⇒ <code>boolean</code></dt>
<dd><p>Check if the object contain an affine matrix</p>
</dd>
<dt><a href="#rotate">rotate(angle, [cx], [cy])</a> ⇒ <code>Object</code></dt>
<dd><p>Calculate a rotation matrix</p>
</dd>
<dt><a href="#rotateDEG">rotateDEG(angle, [cx], [cy])</a> ⇒ <code>Object</code></dt>
<dd><p>Calculate a rotation matrix with a DEG angle</p>
</dd>
<dt><a href="#scale">scale(sx, [sy])</a> ⇒ <code>Object</code></dt>
<dd><p>Calculate a scaling matrix</p>
</dd>
<dt><a href="#shear">shear(shx, shy)</a> ⇒ <code>Object</code></dt>
<dd><p>Calculate a shear matrix</p>
</dd>
<dt><a href="#toCSS">toCSS(matrix)</a> ⇒ <code>string</code></dt>
<dd><p>Serialize the matrix to a string that can be used with CSS or SVG</p>
</dd>
<dt><a href="#toSVG">toSVG(matrix)</a> ⇒ <code>string</code></dt>
<dd><p>Serialize the matrix to a string that can be used with CSS or SVG</p>
</dd>
<dt><a href="#toString">toString(matrix)</a> ⇒ <code>string</code></dt>
<dd><p>Serialize the matrix to a string that can be used with CSS or SVG</p>
</dd>
<dt><a href="#transform">transform(...matrices)</a> ⇒ <code>Object</code></dt>
<dd><p>Merge multiple matrices into one</p>
</dd>
<dt><a href="#translate">translate(tx, [ty])</a> ⇒ <code>Object</code></dt>
<dd><p>Calculate a translate matrix</p>
</dd>
</dl>

## Changelog
- **0.0** - Preview version
- **1.0** - First public version
- **1.1** - Split lib into different files
- **1.2** - Adds shear operation
- **1.3** - Adds umd support
- **1.4** - Adds typescript definitions
- **1.5** - Upgrade deps
- **1.6** - Adds optional parameter support on translate(tx), scale(sx), rotate(angle, cx, cy)

## Some projects using transformation-matrix
- [**React Planner**](https://github.com/cvdlab/react-planner)
- [**React SVG Pan Zoom**](https://github.com/chrvadala/react-svg-pan-zoom)
- [**Others...**](https://libraries.io/npm/transformation-matrix/dependent-repositories)
- Pull request your project!

## Contributors
- [chrvadala](https://github.com/chrvadala) (author)
- [forabi](https://github.com/forabi) (TypeScript definitions)

# API
<a name="applyToPoint"></a>

## applyToPoint(matrix, point) ⇒ <code>Object</code>
Calculate a point transformed with an affine matrix

**Kind**: global function  
**Returns**: <code>Object</code> - Point  

| Param | Description |
| --- | --- |
| matrix | Affine matrix |
| point | Point |

<a name="applyToPoints"></a>

## applyToPoints(matrix, points) ⇒ <code>array</code>
Calculate an array of points transformed with an affine matrix

**Kind**: global function  
**Returns**: <code>array</code> - Array of points  

| Param | Description |
| --- | --- |
| matrix | Affine matrix |
| points | Array of points |

<a name="fromObject"></a>

## fromObject(object) ⇒ <code>Object</code>
Extract an affine matrix from an object that contains a,b,c,d,e,f keys
Each value could be a float or a string that contains a float

**Kind**: global function  
**Returns**: <code>Object</code> - }  

| Param |
| --- |
| object | 

<a name="fromString"></a>

## fromString(string) ⇒ <code>Object</code>
Parse a string matrix formatted as matrix(a,b,c,d,e,f)

**Kind**: global function  
**Returns**: <code>Object</code> - Affine matrix  

| Param | Description |
| --- | --- |
| string | String with a matrix |

<a name="identity"></a>

## identity() ⇒ <code>Object</code>
Identity matrix

**Kind**: global function  
**Returns**: <code>Object</code> - Affine matrix  
<a name="inverse"></a>

## inverse(matrix) ⇒ <code>Object</code>
Calculate a matrix that is the inverse of the provided matrix

**Kind**: global function  
**Returns**: <code>Object</code> - Affine matrix  

| Param | Description |
| --- | --- |
| matrix | Affine matrix |

<a name="isAffineMatrix"></a>

## isAffineMatrix(object) ⇒ <code>boolean</code>
Check if the object contain an affine matrix

**Kind**: global function  

| Param |
| --- |
| object | 

<a name="rotate"></a>

## rotate(angle, [cx], [cy]) ⇒ <code>Object</code>
Calculate a rotation matrix

**Kind**: global function  
**Returns**: <code>Object</code> - Affine matrix *  

| Param | Description |
| --- | --- |
| angle | Angle in radians |
| [cx] | If (cx,cy) are supplied the rotate is about this point |
| [cy] | If (cx,cy) are supplied the rotate is about this point |

<a name="rotateDEG"></a>

## rotateDEG(angle, [cx], [cy]) ⇒ <code>Object</code>
Calculate a rotation matrix with a DEG angle

**Kind**: global function  
**Returns**: <code>Object</code> - Affine matrix  

| Param | Description |
| --- | --- |
| angle | Angle in degree |
| [cx] | If (cx,cy) are supplied the rotate is about this point |
| [cy] | If (cx,cy) are supplied the rotate is about this point |

<a name="scale"></a>

## scale(sx, [sy]) ⇒ <code>Object</code>
Calculate a scaling matrix

**Kind**: global function  
**Returns**: <code>Object</code> - Affine matrix  

| Param | Default | Description |
| --- | --- | --- |
| sx |  | Scaling on axis x |
| [sy] | <code>sx</code> | Scaling on axis y (default sx) |

<a name="shear"></a>

## shear(shx, shy) ⇒ <code>Object</code>
Calculate a shear matrix

**Kind**: global function  
**Returns**: <code>Object</code> - Affine matrix  

| Param | Description |
| --- | --- |
| shx | Shear on axis x |
| shy | Shear on axis y |

<a name="toCSS"></a>

## toCSS(matrix) ⇒ <code>string</code>
Serialize the matrix to a string that can be used with CSS or SVG

**Kind**: global function  
**Returns**: <code>string</code> - String that contains a matrix formatted as matrix(a,b,c,d,e,f)  

| Param | Description |
| --- | --- |
| matrix | Affine matrix |

<a name="toSVG"></a>

## toSVG(matrix) ⇒ <code>string</code>
Serialize the matrix to a string that can be used with CSS or SVG

**Kind**: global function  
**Returns**: <code>string</code> - String that contains a matrix formatted as matrix(a,b,c,d,e,f)  

| Param | Description |
| --- | --- |
| matrix | Affine matrix |

<a name="toString"></a>

## toString(matrix) ⇒ <code>string</code>
Serialize the matrix to a string that can be used with CSS or SVG

**Kind**: global function  
**Returns**: <code>string</code> - String that contains a matrix formatted as matrix(a,b,c,d,e,f)  

| Param | Description |
| --- | --- |
| matrix | Affine matrix |

<a name="transform"></a>

## transform(...matrices) ⇒ <code>Object</code>
Merge multiple matrices into one

**Kind**: global function  
**Returns**: <code>Object</code> - Affine matrix  

| Param | Type | Description |
| --- | --- | --- |
| ...matrices | <code>object</code> | list of matrices |

<a name="translate"></a>

## translate(tx, [ty]) ⇒ <code>Object</code>
Calculate a translate matrix

**Kind**: global function  
**Returns**: <code>Object</code> - Affine matrix  

| Param | Default | Description |
| --- | --- | --- |
| tx |  | Translation on axis x |
| [ty] | <code>0</code> | Translation on axis y (default 0) |

