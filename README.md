# api documentation for  [svg2ttf (v4.0.2)](https://github.com/fontello/svg2ttf#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-svg2ttf.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-svg2ttf) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-svg2ttf.svg)](https://travis-ci.org/npmdoc/node-npmdoc-svg2ttf)
#### Converts SVG font to TTF font

[![NPM](https://nodei.co/npm/svg2ttf.png?downloads=true)](https://www.npmjs.com/package/svg2ttf)

[![apidoc](https://npmdoc.github.io/node-npmdoc-svg2ttf/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-svg2ttf_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-svg2ttf/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-svg2ttf/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-svg2ttf/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Sergey Batishchev",
        "email": "sergej.batishchev@gmail.com"
    },
    "bin": {
        "svg2ttf": "./svg2ttf.js"
    },
    "bugs": {
        "url": "https://github.com/fontello/svg2ttf/issues"
    },
    "dependencies": {
        "argparse": "^1.0.6",
        "cubic2quad": "^1.0.0",
        "lodash": "^4.6.1",
        "microbuffer": "^1.0.0",
        "svgpath": "^2.1.5",
        "xmldom": "~0.1.22"
    },
    "description": "Converts SVG font to TTF font",
    "devDependencies": {
        "eslint": "~3.2.2",
        "mocha": "^3.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "5e37123c7e9bf3dc6c7f26b141392a19fcec7a57",
        "tarball": "https://registry.npmjs.org/svg2ttf/-/svg2ttf-4.0.2.tgz"
    },
    "files": [
        "index.js",
        "svg2ttf.js",
        "lib/"
    ],
    "gitHead": "e9d53557ae63fce96cc34cd23117bf1de593afcc",
    "homepage": "https://github.com/fontello/svg2ttf#readme",
    "keywords": [
        "font",
        "ttf",
        "svg",
        "convertor"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "vitaly",
            "email": "vitaly@rcdesign.ru"
        }
    ],
    "name": "svg2ttf",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/fontello/svg2ttf.git"
    },
    "scripts": {
        "lint": "eslint .",
        "test": "npm run lint && ./node_modules/.bin/mocha"
    },
    "version": "4.0.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module svg2ttf](#apidoc.module.svg2ttf)
1.  object <span class="apidocSignatureSpan">svg2ttf.</span>math
1.  object <span class="apidocSignatureSpan">svg2ttf.</span>sfnt
1.  object <span class="apidocSignatureSpan">svg2ttf.</span>svg
1.  object <span class="apidocSignatureSpan">svg2ttf.</span>ucs2

#### [module svg2ttf.math](#apidoc.module.svg2ttf.math)
1.  [function <span class="apidocSignatureSpan">svg2ttf.math.</span>Point (x, y)](#apidoc.element.svg2ttf.math.Point)
1.  [function <span class="apidocSignatureSpan">svg2ttf.math.</span>isInLine (p1, m, p2, accuracy)](#apidoc.element.svg2ttf.math.isInLine)

#### [module svg2ttf.sfnt](#apidoc.module.svg2ttf.sfnt)
1.  [function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>Contour ()](#apidoc.element.svg2ttf.sfnt.Contour)
1.  [function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>Font ()](#apidoc.element.svg2ttf.sfnt.Font)
1.  [function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>Glyph ()](#apidoc.element.svg2ttf.sfnt.Glyph)
1.  [function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>Point ()](#apidoc.element.svg2ttf.sfnt.Point)
1.  [function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>SfntName ()](#apidoc.element.svg2ttf.sfnt.SfntName)
1.  [function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>toTTF (font)](#apidoc.element.svg2ttf.sfnt.toTTF)

#### [module svg2ttf.svg](#apidoc.module.svg2ttf.svg)
1.  [function <span class="apidocSignatureSpan">svg2ttf.svg.</span>cubicToQuad (segment, index, x, y, accuracy)](#apidoc.element.svg2ttf.svg.cubicToQuad)
1.  [function <span class="apidocSignatureSpan">svg2ttf.svg.</span>load (str)](#apidoc.element.svg2ttf.svg.load)
1.  [function <span class="apidocSignatureSpan">svg2ttf.svg.</span>toSfntCoutours (svgPath)](#apidoc.element.svg2ttf.svg.toSfntCoutours)

#### [module svg2ttf.ucs2](#apidoc.module.svg2ttf.ucs2)
1.  [function <span class="apidocSignatureSpan">svg2ttf.ucs2.</span>decode (string)](#apidoc.element.svg2ttf.ucs2.decode)
1.  [function <span class="apidocSignatureSpan">svg2ttf.ucs2.</span>encode (array)](#apidoc.element.svg2ttf.ucs2.encode)



# <a name="apidoc.module.svg2ttf"></a>[module svg2ttf](#apidoc.module.svg2ttf)



# <a name="apidoc.module.svg2ttf.math"></a>[module svg2ttf.math](#apidoc.module.svg2ttf.math)

#### <a name="apidoc.element.svg2ttf.math.Point"></a>[function <span class="apidocSignatureSpan">svg2ttf.math.</span>Point (x, y)](#apidoc.element.svg2ttf.math.Point)
- description and source-code
```javascript
function Point(x, y) {
  this.x = x;
  this.y = y;
}
```
- example usage
```shell
...
    var sfntContours = svg.toSfntCoutours(svgPath);

    // Add contours to SFNT font
    glyph.contours = _.map(sfntContours, function (sfntContour) {
var contour = new sfnt.Contour();

contour.points = _.map(sfntContour, function (sfntPoint) {
  var point = new sfnt.Point();

  point.x = sfntPoint.x;
  point.y = sfntPoint.y;
  point.onCurve = sfntPoint.onCurve;
  return point;
});
...
```

#### <a name="apidoc.element.svg2ttf.math.isInLine"></a>[function <span class="apidocSignatureSpan">svg2ttf.math.</span>isInLine (p1, m, p2, accuracy)](#apidoc.element.svg2ttf.math.isInLine)
- description and source-code
```javascript
function isInLine(p1, m, p2, accuracy) {
  var a = p1.sub(m).sqr();
  var b = p2.sub(m).sqr();
  var c = p1.sub(p2).sqr();

  // control point not between anchors
  if ((a > (b + c)) || (b > (a + c))) {
    return false;
  }

  // count distance via scalar multiplication
  var distance = Math.sqrt(Math.pow((p1.x - m.x) * (p2.y - m.y) - (p2.x - m.x) * (p1.y - m.y), 2) / c);

  return distance < accuracy ? true : false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.svg2ttf.sfnt"></a>[module svg2ttf.sfnt](#apidoc.module.svg2ttf.sfnt)

#### <a name="apidoc.element.svg2ttf.sfnt.Contour"></a>[function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>Contour ()](#apidoc.element.svg2ttf.sfnt.Contour)
- description and source-code
```javascript
function Contour() {
  this.points = [];
}
```
- example usage
```shell
...
      .iterate(function (segment, index, x, y) {
return svg.cubicToQuad(segment, index, x, y, accuracy);
      });
    var sfntContours = svg.toSfntCoutours(svgPath);

    // Add contours to SFNT font
    glyph.contours = _.map(sfntContours, function (sfntContour) {
      var contour = new sfnt.Contour();

      contour.points = _.map(sfntContour, function (sfntPoint) {
var point = new sfnt.Point();

point.x = sfntPoint.x;
point.y = sfntPoint.y;
point.onCurve = sfntPoint.onCurve;
...
```

#### <a name="apidoc.element.svg2ttf.sfnt.Font"></a>[function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>Font ()](#apidoc.element.svg2ttf.sfnt.Font)
- description and source-code
```javascript
function Font() {
  this.ascent = 850;
  this.copyright = '';
  this.createdDate = new Date();
  this.glyphs = [];
  this.ligatures = [];
  // Maping of code points to glyphs.
  // Keys are actually numeric, thus should be 'parseInt'ed.
  this.codePoints = {};
  this.isFixedPitch = 0;
  this.italicAngle = 0;
  this.familyClass = 0; // No Classification
  this.familyName = '';
  this.fsSelection = 0x40; // Characters are in the standard weight/style for the font.
  // Non zero value can cause issues in IE, https://github.com/fontello/svg2ttf/issues/45
  this.fsType = 0;
  this.lowestRecPPEM = 8;
  this.macStyle = 0;
  this.modifiedDate = new Date();
  this.panose = {
    familyType: 2, // Latin Text
    serifStyle: 0, // any
    weight: 5, // book
    proportion: 3, //modern
    contrast: 0, //any
    strokeVariation: 0, //any,
    armStyle: 0, //any,
    letterform: 0, //any,
    midline: 0, //any,
    xHeight: 0 //any,
  };
  this.revision = 1;
  this.sfntNames = [];
  this.underlineThickness = 0;
  this.unitsPerEm = 1000;
  this.weightClass = 400; // normal
  this.width = 1000;
  this.widthClass = 5; // Medium (normal)
  this.ySubscriptXOffset = 0;
  this.ySuperscriptXOffset = 0;
  this.int_descent = -150;

//getters and setters

  Object.defineProperty(this, 'descent', {
    get: function () {
      return this.int_descent;
    },
    set: function (value) {
      this.int_descent = parseInt(Math.round(-Math.abs(value)), 10);
    }
  });

  this.__defineGetter__('avgCharWidth', function () {
    if (this.glyphs.length === 0) {
      return 0;
    }
    var widths = _.map(this.glyphs, 'width');

    return parseInt(widths.reduce(function (prev, cur) {
      return prev + cur;
    }) / widths.length, 10);
  });

  Object.defineProperty(this, 'ySubscriptXSize', {
    get: function () {
      return parseInt(!_.isUndefined(this.int_ySubscriptXSize) ? this.int_ySubscriptXSize : (this.width * 0.6347), 10);
    },
    set: function (value) {
      this.int_ySubscriptXSize = value;
    }
  });

  Object.defineProperty(this, 'ySubscriptYSize', {
    get: function () {
      return parseInt(!_.isUndefined(this.int_ySubscriptYSize) ? this.int_ySubscriptYSize : ((this.ascent - this.descent) * 0.7),
10);
    },
    set: function (value) {
      this.int_ySubscriptYSize = value;
    }
  });

  Object.defineProperty(this, 'ySubscriptYOffset', {
    get: function () {
      return parseInt(!_.isUndefined(this.int_ySubscriptYOffset) ? this.int_ySubscriptYOffset : ((this.ascent - this.descent) *
0.14), 10);
    },
    set: function (value) {
      this.int_ySubscriptYOffset = value;
    }
  });

  Object.defineProperty(this, 'ySuperscriptXSize', {
    get: function () {
      return parseInt(!_.isUndefined(this.int_ySuperscriptXSize) ? this.int_ySuperscriptXSize : (this.width * 0.6347), 10);
    },
    set: function (value) {
      this.int_ySuperscriptXSize = value;
    }
  });

  Object.defineProperty(this, 'ySuperscriptYSize', {
    get: function () {
      return parseInt(!_.isUndefined(this.int_ySuperscriptYSize) ? this.int_ySuperscriptYSize : ((this.ascent - this.descent) *
0.7), 10);
    },
    set: function (value) {
      this.int_ySuperscriptYSize = value;
    }
  });

  Object.defineProperty(this, 'ySuperscriptYOffset', {
    get: function () {
      return parseInt(!_.isUndefined(this.int_ySuperscriptYOffset) ? this.int_ySuperscriptYOffset : ((this.ascent - this.descent
) * 0.48), 10);
    },
    set: function (value) {
      this.int_ySuperscriptYOffset = value;
    }
  });

  Object.defineProperty(this, 'yStrikeoutSize', {
    get: function () {
      return parseInt(!_.isUndefined(this.int_yStrikeoutSize) ? this.int_yStrikeoutSize : ((this.ascent - this.descent) * 0.049),
10);
    },
    set: function (value) {
      this.int_yStrikeoutSize = value;
    }
  });

  Object.defineProperty(this, 'yStrikeoutPosition', {
    get: function () {
      return parseInt(!_.isUndefined(this.int_yStrikeoutPosition) ? this.int_yStrikeoutPosition : ((this.ascent - this.descent) *
0.258), 10);
    },
    set: function (value) { ...
```
- example usage
```shell
...
var sfnt    = require('./lib/sfnt');


var VERSION_RE = /^(Version )?(\d+[.]\d+)$/i;


function svg2ttf(svgString, options) {
var font = new sfnt.Font();
var svgFont = svg.load(svgString);

options = options || {};

font.id = options.id || svgFont.id;
font.familyName = options.familyname || svgFont.familyName || svgFont.id;
font.copyright = options.copyright || svgFont.metadata;
...
```

#### <a name="apidoc.element.svg2ttf.sfnt.Glyph"></a>[function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>Glyph ()](#apidoc.element.svg2ttf.sfnt.Glyph)
- description and source-code
```javascript
function Glyph() {
  this.contours = [];
  this.d = '';
  this.id = '';
  this.height = 0;
  this.name = '';
  this.width = 0;
}
```
- example usage
```shell
...
}
codePoints[codePoint] = glyph;
return true;
  }

  // add SVG glyphs to SFNT font
  _.forEach(svgFont.glyphs, function (svgGlyph) {
var glyph = new sfnt.Glyph();

glyph.name = svgGlyph.name;
glyph.d = svgGlyph.d;
glyph.height = !isNaN(svgGlyph.height) ? svgGlyph.height : font.height;
glyph.width = !isNaN(svgGlyph.width) ? svgGlyph.width : font.width;
glyphs.push(glyph);
...
```

#### <a name="apidoc.element.svg2ttf.sfnt.Point"></a>[function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>Point ()](#apidoc.element.svg2ttf.sfnt.Point)
- description and source-code
```javascript
function Point() {
  this.onCurve = true;
  this.x = 0;
  this.y = 0;
}
```
- example usage
```shell
...
    var sfntContours = svg.toSfntCoutours(svgPath);

    // Add contours to SFNT font
    glyph.contours = _.map(sfntContours, function (sfntContour) {
var contour = new sfnt.Contour();

contour.points = _.map(sfntContour, function (sfntPoint) {
  var point = new sfnt.Point();

  point.x = sfntPoint.x;
  point.y = sfntPoint.y;
  point.onCurve = sfntPoint.onCurve;
  return point;
});
...
```

#### <a name="apidoc.element.svg2ttf.sfnt.SfntName"></a>[function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>SfntName ()](#apidoc.element.svg2ttf.sfnt.SfntName)
- description and source-code
```javascript
function SfntName() {
  this.id = 0;
  this.value = '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.svg2ttf.sfnt.toTTF"></a>[function <span class="apidocSignatureSpan">svg2ttf.sfnt.</span>toTTF (font)](#apidoc.element.svg2ttf.sfnt.toTTF)
- description and source-code
```javascript
function generateTTF(font) {

  // Prepare TTF contours objects. Note, that while sfnt countours are classes,
  // ttf contours are just plain arrays of points
  _.forEach(font.glyphs, function (glyph) {
    glyph.ttfContours = _.map(glyph.contours, function (contour) {
      return contour.points;
    });
  });

  // Process ttf contours data
  _.forEach(font.glyphs, function (glyph) {

    // 0.3px accuracy is ok. fo 1000x1000.
    glyph.ttfContours = utils.simplify(glyph.ttfContours, 0.3);
    glyph.ttfContours = utils.simplify(glyph.ttfContours, 0.3); // one pass is not enougth

    // Interpolated points can be removed. 1.1px is acceptable
    // measure - it will give us 1px error after coordinates rounding.
    glyph.ttfContours = utils.interpolate(glyph.ttfContours, 1.1);

    glyph.ttfContours = utils.roundPoints(glyph.ttfContours);
    glyph.ttfContours = utils.removeClosingReturnPoints(glyph.ttfContours);
    glyph.ttfContours = utils.toRelative(glyph.ttfContours);
  });

  // Add tables
  var headerSize = 12 + 16 * TABLES.length; // TTF header plus table headers
  var bufSize = headerSize;

  _.forEach(TABLES, function (table) {
    //store each table in its own buffer
    table.buffer = table.create(font);
    table.length = table.buffer.length;
    table.corLength = table.length + (4 - table.length % 4) % 4; // table size should be divisible to 4
    table.checkSum = calc_checksum(table.buffer);
    bufSize += table.corLength;
  });

  //calculate offsets
  var offset = headerSize;

  _.forEach(_.sortBy(TABLES, 'order'), function (table) {
    table.offset = offset;
    offset += table.corLength;
  });

  //create TTF buffer

  var buf = new ByteBuffer(bufSize);

  //special constants
  var entrySelector = Math.floor(Math.log(TABLES.length) / Math.LN2);
  var searchRange = Math.pow(2, entrySelector) * 16;
  var rangeShift = TABLES.length * 16 - searchRange;

  // Add TTF header
  buf.writeUint32(CONST.VERSION);
  buf.writeUint16(TABLES.length);
  buf.writeUint16(searchRange);
  buf.writeUint16(entrySelector);
  buf.writeUint16(rangeShift);

  _.forEach(TABLES, function (table) {
    buf.writeUint32(utils.identifier(table.innerName)); //inner name
    buf.writeUint32(table.checkSum); //checksum
    buf.writeUint32(table.offset); //offset
    buf.writeUint32(table.length); //length
  });

  var headOffset = 0;

  _.forEach(_.sortBy(TABLES, 'order'), function (table) {
    if (table.innerName === 'head') { //we must store head offset to write font checksum
      headOffset = buf.tell();
    }
    buf.writeBytes(table.buffer.buffer);
    for (var i = table.length; i < table.corLength; i++) { //align table to be divisible to 4
      buf.writeUint8(0);
    }
  });

  // Write font checksum (corrected by magic value) into HEAD table
  buf.setUint32(headOffset + 8, ulong(CONST.CHECKSUM_ADJUSTMENT - calc_checksum(buf)));

  return buf;
}
```
- example usage
```shell
...
        return point;
      });

      return contour;
    });
  });

  var ttf = sfnt.toTTF(font);

  return ttf;
}

module.exports = svg2ttf;
...
```



# <a name="apidoc.module.svg2ttf.svg"></a>[module svg2ttf.svg](#apidoc.module.svg2ttf.svg)

#### <a name="apidoc.element.svg2ttf.svg.cubicToQuad"></a>[function <span class="apidocSignatureSpan">svg2ttf.svg.</span>cubicToQuad (segment, index, x, y, accuracy)](#apidoc.element.svg2ttf.svg.cubicToQuad)
- description and source-code
```javascript
function cubicToQuad(segment, index, x, y, accuracy) {
  if (segment[0] === 'C') {
    var quadCurves = cubic2quad(
      x, y,
      segment[1], segment[2],
      segment[3], segment[4],
      segment[5], segment[6],
      accuracy
    );

    var res = [];

    for (var i = 2; i < quadCurves.length; i += 4) {
      res.push([ 'Q', quadCurves[i], quadCurves[i + 1], quadCurves[i + 2], quadCurves[i + 3] ]);
    }
    return res;
  }
}
```
- example usage
```shell
...

//SVG transformations
var svgPath = new SvgPath(glyph.d)
  .abs()
  .unshort()
  .unarc()
  .iterate(function (segment, index, x, y) {
    return svg.cubicToQuad(segment, index, x, y, accuracy);
  });
var sfntContours = svg.toSfntCoutours(svgPath);

// Add contours to SFNT font
glyph.contours = _.map(sfntContours, function (sfntContour) {
  var contour = new sfnt.Contour();
...
```

#### <a name="apidoc.element.svg2ttf.svg.load"></a>[function <span class="apidocSignatureSpan">svg2ttf.svg.</span>load (str)](#apidoc.element.svg2ttf.svg.load)
- description and source-code
```javascript
function load(str) {
  var attrs;

  var doc = (new DOMParser()).parseFromString(str, 'application/xml');

  var metadata, fontElem, fontFaceElem;

  metadata = doc.getElementsByTagName('metadata')[0];
  fontElem = doc.getElementsByTagName('font')[0];

  if (!fontElem) {
    throw new Error("Can't find <font> tag. Make sure you SVG file is font, not image.");
  }

  fontFaceElem = fontElem.getElementsByTagName('font-face')[0];

  var font = {
    id: fontElem.getAttribute('id') || 'fontello',
    familyName: fontFaceElem.getAttribute('font-family') || 'fontello',
    stretch: fontFaceElem.getAttribute('font-stretch') || 'normal'
  };

  // Doesn't work with complex content like <strong>Copyright:></strong><em>Fontello</em>
  if (metadata && metadata.textContent) {
    font.metadata = metadata.textContent;
  }

  // Get <font> numeric attributes
  attrs = {
    width:        'horiz-adv-x',
    //height:       'vert-adv-y',
    horizOriginX: 'horiz-origin-x',
    horizOriginY: 'horiz-origin-y',
    vertOriginX:  'vert-origin-x',
    vertOriginY:  'vert-origin-y'
  };
  _.forEach(attrs, function (val, key) {
    if (fontElem.hasAttribute(val)) { font[key] = parseInt(fontElem.getAttribute(val), 10); }
  });

  // Get <font-face> numeric attributes
  attrs = {
    ascent:     'ascent',
    descent:    'descent',
    unitsPerEm: 'units-per-em'
  };
  _.forEach(attrs, function (val, key) {
    if (fontFaceElem.hasAttribute(val)) { font[key] = parseInt(fontFaceElem.getAttribute(val), 10); }
  });

  if (fontFaceElem.hasAttribute('font-weight')) {
    font.weightClass = fontFaceElem.getAttribute('font-weight');
  }

  var missingGlyphElem = fontElem.getElementsByTagName('missing-glyph')[0];

  if (missingGlyphElem) {

    font.missingGlyph = {};
    font.missingGlyph.d = missingGlyphElem.getAttribute('d') || '';

    if (missingGlyphElem.getAttribute('horiz-adv-x')) {
      font.missingGlyph.width = parseInt(missingGlyphElem.getAttribute('horiz-adv-x'), 10);
    }
  }

  var glyphs = [];
  var ligatures = [];

  _.forEach(fontElem.getElementsByTagName('glyph'), function (glyphElem) {
    var glyph = getGlyph(glyphElem);

    if (_.has(glyph, 'ligature')) {
      ligatures.push({
        ligature: glyph.ligature,
        unicode: glyph.ligatureCodes,
        glyph: glyph
      });
    }

    glyphs.push(glyph);
  });

  glyphs = deduplicateGlyps(glyphs, ligatures);

  font.glyphs = glyphs;
  font.ligatures = ligatures;

  return font;
}
```
- example usage
```shell
...


var VERSION_RE = /^(Version )?(\d+[.]\d+)$/i;


function svg2ttf(svgString, options) {
var font = new sfnt.Font();
var svgFont = svg.load(svgString);

options = options || {};

font.id = options.id || svgFont.id;
font.familyName = options.familyname || svgFont.familyName || svgFont.id;
font.copyright = options.copyright || svgFont.metadata;
font.sfntNames.push({ id: 2, value: options.subfamilyname || 'Regular' }); // subfamily name
...
```

#### <a name="apidoc.element.svg2ttf.svg.toSfntCoutours"></a>[function <span class="apidocSignatureSpan">svg2ttf.svg.</span>toSfntCoutours (svgPath)](#apidoc.element.svg2ttf.svg.toSfntCoutours)
- description and source-code
```javascript
function toSfntCoutours(svgPath) {
  var resContours = [];
  var resContour = [];

  svgPath.iterate(function (segment, index, x, y) {

    //start new contour
    if (index === 0 || segment[0] === 'M') {
      resContour = [];
      resContours.push(resContour);
    }

    var name = segment[0];

    if (name === 'Q') {
      //add control point of quad spline, it is not on curve
      resContour.push({ x: segment[1], y: segment[2], onCurve: false });
    }

    // add on-curve point
    if (name === 'H') {
      // vertical line has Y coordinate only, X remains the same
      resContour.push({ x: segment[1], y: y, onCurve: true });
    } else if (name === 'V') {
      // horizontal line has X coordinate only, Y remains the same
      resContour.push({ x: x, y: segment[1], onCurve: true });
    } else if (name !== 'Z') {
      // for all commands (except H and V) X and Y are placed in the end of the segment
      resContour.push({ x: segment[segment.length - 2], y: segment[segment.length - 1], onCurve: true });
    }

  });
  return resContours;
}
```
- example usage
```shell
...
    var svgPath = new SvgPath(glyph.d)
.abs()
.unshort()
.unarc()
.iterate(function (segment, index, x, y) {
  return svg.cubicToQuad(segment, index, x, y, accuracy);
});
    var sfntContours = svg.toSfntCoutours(svgPath);

    // Add contours to SFNT font
    glyph.contours = _.map(sfntContours, function (sfntContour) {
var contour = new sfnt.Contour();

contour.points = _.map(sfntContour, function (sfntPoint) {
  var point = new sfnt.Point();
...
```



# <a name="apidoc.module.svg2ttf.ucs2"></a>[module svg2ttf.ucs2](#apidoc.module.svg2ttf.ucs2)

#### <a name="apidoc.element.svg2ttf.ucs2.decode"></a>[function <span class="apidocSignatureSpan">svg2ttf.ucs2.</span>decode (string)](#apidoc.element.svg2ttf.ucs2.decode)
- description and source-code
```javascript
function ucs2decode(string) {
  var output = [],
      counter = 0,
      length = string.length,
      value,
      extra;

  while (counter < length) {
    value = string.charCodeAt(counter++);
    if (value >= 0xD800 && value <= 0xDBFF && counter < length) {
      // high surrogate, and there is a next character
      extra = string.charCodeAt(counter++);
      if ((extra & 0xFC00) === 0xDC00) { // low surrogate
        output.push(((value & 0x3FF) << 10) + (extra & 0x3FF) + 0x10000);
      } else {
        // unmatched surrogate; only append this code unit, in case the next
        // code unit is the high surrogate of a surrogate pair
        output.push(value);
        counter--;
      }
    } else {
      output.push(value);
    }
  }
  return output;
}
```
- example usage
```shell
...
  var glyph = {};

  glyph.d = glyphElem.getAttribute('d').trim();
  glyph.unicode = [];

  if (glyphElem.getAttribute('unicode')) {
glyph.character = glyphElem.getAttribute('unicode');
var unicode = ucs2.decode(glyph.character);

// If more than one code point is involved, the glyph is a ligature glyph
if (unicode.length > 1) {
  glyph.ligature = glyph.character;
  glyph.ligatureCodes = unicode;
} else {
  glyph.unicode.push(unicode[0]);
...
```

#### <a name="apidoc.element.svg2ttf.ucs2.encode"></a>[function <span class="apidocSignatureSpan">svg2ttf.ucs2.</span>encode (array)](#apidoc.element.svg2ttf.ucs2.encode)
- description and source-code
```javascript
function ucs2encode(array) {
  return _.map(array, function (value) {
    var output = '';

    if (value > 0xFFFF) {
      value -= 0x10000;
      output += String.fromCharCode(value >>> 10 & 0x3FF | 0xD800);
      value = 0xDC00 | value & 0x3FF;
    }
    output += String.fromCharCode(value);
    return output;
  }).join('');
}
```
- example usage
```shell
...

  _.forEach(ligature.unicode, function (charPoint) {
    // We need to have a distinct glyph for each code point so we can reference it in GSUB
    var glyph = new sfnt.Glyph();
    var added = addCodePoint(charPoint, glyph);

    if (added) {
      glyph.name = ucs2.encode([ charPoint ]);
      glyphs.push(glyph);
    }
  });
  ligatures.push(ligature);
});

// Missing Glyph needs to have index 0
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
