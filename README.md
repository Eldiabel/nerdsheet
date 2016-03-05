# Nerdsheet Framework

Nerdsheet allows you to set simple styling to elements with just a few shorthand classes

## Code Example

```html
<div class="ta-c fw-bold d-i m-l-25 f-l"></div>
```
Will apply following CSS to the concrete div element:
```scss
text-align  : center;
font-weight : bold;
display     : inline;
margin-left : 25px;
float       : left
```

***

Simulating tables and centering elements horizontally and vertically too.

```html
<div class="d-t">
  <div class="d-tr">
    <div class="d-tc va-m ta-c">
      <span>Vertically and Horizontally centered text!</span>
    </div>
  </div>
</div>
```
The most inner div element will be applied:
```scss
display        : table-cell;
vertical-align : middle;
text-align     : center;
```

## Motivation

As a hardcore [Twitter Bootstrap](http://getbootstrap.com) user you can often run into situation that bootstrap didn't keep in mind, like **text-align**ing, **vertical-align**ing, **padding**s and **margin**s or **display**s and you really really want to style that element with just a single shorthand class.

## Installation
```bash
bower install nerdsheet --save
```

## API Reference



## License

MIT
