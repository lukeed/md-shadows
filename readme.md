# md-shadows

> Material Design shadows as SASS mixins, classes, and extensions.


## Install

```
$ bower install --save md-shadows
```


## Usage

```sass
@import 'md-shadows'

.element1
  +md-shadow(2, #1A237E)

.element2
  @extend %md-shadow--3

.element3
  @extend %md-shadow--3
```

Output:

```css
.element1 {
  box-shadow: 0 3px 6px rgba(26,35,126, 0.16), 0 3px 6px rgba(26,35,126, 0.23)
}

.md-shadow--3,
.element1,
.element3 {
  box-shadow: 0 10px 20px rgba(0,0,0, 0.19), 0 6px 6px rgba(0,0,0, 0.23)
}
```


## API

### +md-color(depth, [color])

Add a shadow to an element, using the mixin.

#### depth

Type: `integer`

The depth of the shadow. Smaller numbers represent "shorter", denser shadows. 

Range:
* `0` is no shadow
* `5` is the largest, most obscure shadow

#### color

Type: `Color`<br>
Default: `black`

An optional color to use as the shadow's color. May use either a HEX or RGB value.

> **Note:** Only mixins can accept an alternate color. If you use the extensions (`%md-shadow--X`) or classes (`.md-shadow--X`) your shadow will always be pure black.

## License

MIT © [Luke Edwards](https://github.com/lukeed)
