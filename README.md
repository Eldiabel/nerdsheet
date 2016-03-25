# Nerdsheet CSS

Nerdsheet allows you to simply set expressive styling to elements with just a few shorthand classes

## Code Example

```html
<div class="ta-c fw-600 d-ib m-l-25 f-l"></div>
```
Will apply following CSS to the concrete div element:
```scss
text-align  : center;
font-weight : 600;
display     : inline-block;
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

```bash
git clone git://github.com/Eldiabel/nerdsheet.git
```

## Usage
```html
<element class="classname-type-value-media-state" />
```

#### Where:

Type | Necessity | Description | Example
--- | --- | --- | ---
**classname** | Obligatory | Shortcut name of the class used. | *.m stands for margin*
**type** | Optional in some cases | Type of the property. | *.m-b stands for margin-bottom*
**value** | Obligatory for some classes | Value to be applied | *.m-b-20 stands for margin-bottom: 20px;*
**media** | Optional | Media to be used. | *.m-b-20-min-md will be emitted inside "@media screen and (min-width: 992px)" by default*
**state** | Optional | State to be styling applied to only. | *fw-bold-hover will emit .fw-bold-hover:hover {font-weight: bold;}*

## API Reference

### Default classes & Variables:

##### Medias:

Type | Size
--- | --- | --- | --- 
min screen size | 480px
min screen size | 768px
min screen size | 992px
min screen size | 1200px

##### Directions:

Type | Class | Value
--- | --- | --- | --- 
{padding, margin, border-radius} | *{p, m, bo}-direction*-**t** | top
{padding, margin, border-radius} | *{p, m, bo}-direction*-**r** | right
{padding, margin, border-radius} | *{p, m, bo}-direction*-**b** | bottom
{padding, margin, border-radius} | *{p, m, bo}-direction*-**l** | left

***

### Colors:

Type | Class | Value
--- | --- | --- | --- 
{color, background-color, border-color} | {c, b, bo}-**white** | #FFF
{color, background-color, border-color} | {c, b, bo}-**black** | #000

***

### Positioning & Blocks

##### Display

Type | Class | Value
--- | --- | --- | --- 
display | d-**b** | block
display | d-**i** | inline
display | d-**ib** | inline-block
display | d-**t** | table
display | d-**tr** | table-row
display | d-**tc** | table-cell

##### Float

Type | Class | Value
--- | --- | --- | --- 
float | f-**l** | left
float | f-**r** | right
float | f-**n** | none

##### Padding, Margin:

Type | Class | Size
--- | --- | --- | --- 
{padding, margin} | {p, m}-*{direction}*-**auto** | auto
{padding, margin} | {p, m}-*{direction}*-**0** | 0
{padding, margin} | {p, m}-*{direction}*-**5** | 5px
{padding, margin} | {p, m}-*{direction}*-**8** | 8px
{padding, margin} | {p, m}-*{direction}*-**10** | 10px
{padding, margin} | {p, m}-*{direction}*-**15** | 15px
{padding, margin} | {p, m}-*{direction}*-**25** | 25px
{padding, margin} | {p, m}-*{direction}*-**50** | 50px

###### Horizontal & Vertical

{p, m}-**v**-*size* => {p, m}-**t**-*size* + {p, m}-**b**-*size*

{p, m}-**h**-*size* => {p, m}-**r**-*size* + {p, m}-**l**-*size*

##### Overflow:

Type | Class | Value
--- | --- | --- | --- 
overflow | o-**h** | hidden
overflow | o-**v** | visible
overflow | o-**a** | auto
overflow | o-**s** | scroll

##### Vertical align

Type | Class | Value
--- | --- | --- | --- 
vertical-align | va-**t** | top
vertical-align | va-**b** | bottom
vertical-align | va-**m** | middle
vertical-align | va-**ba** | baseline

***

### Texts:

##### Font size:

Type | Class | Size
--- | --- | --- | --- 
font-size | fs-**1** | 30px
font-size | fs-**2** | 24px
font-size | fs-**3** | 18px
font-size | fs-**4** | 16px
font-size | fs-**5** | 14px
font-size | fs-**6** | 12px

##### Font weight:

Type | Class | Value
--- | --- | --- | --- 
font-weight | fw-**200** | 200
font-weight | fw-**300** | 300
font-weight | fw-**400** | 400
font-weight | fw-**500** | 500
font-weight | fw-**600** | 600

##### Font style:

Type | Class | Value
--- | --- | --- | --- 
font-style | fs-**n** | normal
font-style | fs-**i** | italic

##### Text align:

Type | Class | Value
--- | --- | --- | --- 
text-align | ta-**l** | left
text-align | ta-**r** | right
text-align | ta-**c** | center
text-align | ta-**j** | justify

##### Text decoration:

Type | Class | Value
--- | --- | --- | --- 
text-decoration | td-**n** | none
text-decoration | td-**u** | underline
text-decoration | td-**lt** | line-through

***

### Borders:

##### Border width

Type | Class | Size
--- | --- | --- | --- 
border-width | bo-**0** | 0
border-width | bo-**1** | 1px
border-width | bo-**2** | 2px

##### Border radius:

Type | Class | Value
--- | --- | --- | --- 
border-radius | circle | 50%
border-radius | square | 0
border-radius | rounded | 4px
border-radius | rounded-**t** | 4px 4px 0 0
border-radius | rounded-**r** | 0 4px 4px 0
border-radius | rounded-**b** | 0 0 4px 4px
border-radius | rounded-**l** | 4px 0 0 4px
border-top-left-radius | rounded-**tl** | 4px
border-top-right-radius | rounded-**tr** | 4px
border-bottom-left-radius | rounded-**bl** | 4px
border-bottom-right-radius | rounded-**br** | 4px

### States

These classes support hover state:

* font-size -> **fs**-*options*-**hover**
* font-weight -> **fw**-*options*-**hover**
* font-style -> **fs**-*options*-**hover**
* text-decoration -> **td**-*options*-**hover**
* color -> **c**-*options*-**hover**
* background-color -> **b**-*options*-**hover**
* border-color -> **bo**-*options*-**hover**
* border-width -> **bo**-*options*-**hover**

## License

MIT
