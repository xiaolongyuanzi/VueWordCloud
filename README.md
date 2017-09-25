# VueWordCloud

A word cloud generator.

## demo

[Try it out!](https://seregpie.github.io/VueWordCloud/)

## dependencies

- [Vue](https://github.com/vuejs/vue)

## setup

Install the [package](https://www.npmjs.com/package/vuewordcloud) via npm.

```sh

npm install vuewordcloud

```

---

Include the code in your page via a CDN.

```html

<script src="https://unpkg.com/vue"></script>
<script src="https://unpkg.com/vuewordcloud"></script>

```

## usage

```html

<vue-word-cloud
  :words="[['romance', 19], ['horror', 3], ['fantasy', 7], ['adventure', 3]]"
  :color="([, weight]) => weight > 10 ? 'DeepPink' : weight > 5 ? 'RoyalBlue' : 'Indigo'"
  font-family="Roboto"
></vue-word-cloud>

```

## properties

`words = []`

An array of words. A value of the array is either an object, a string or an array.

If the value is an object: `{text, weight, color, rotation, fontFamily, fontStyle, fontVariant, fontWeight}`.

If the value is an array: `[text, weight, color, rotation, fontFamily, fontStyle, fontVariant, fontWeight]`.

If the value is a string: `text`;

---

`text = ''`

A string or a function for the text of each word.

---

`weight = 1`

A number or a function for the weight of each word.

---

`color = 'Black'`

A string or a function for the color of each word.

---

`rotation`

A number or a function for the rotation of each word. The units for the rotation are turns (1 turn is 360 degrees).

---

`fontFamily = 'serif'`

A string or a function for the font family.

---

`fontStyle = 'normal'`

A string or a function for the font style of each word. Possible values are `'normal'`, `'italic'` and `'oblique'`.

---

`fontVariant = 'normal'`

A string or a function for the font variant of each word. Possible values are `'normal'` and `'small-caps'`.

---

`fontWeight = 'normal'`

A string or a function for the font weight of each word. Possible values are `'normal'`, `'bold'`, `'bolder'`, `'lighter'` and `'100'` to `'900'`.

---

`text`<br/>
`weight`<br/>
`color`<br/>
`rotation`<br/>
`fontFamily`<br/>
`fontStyle`<br/>
`fontVariant`<br/>
`fontWeight`<br/>

If the property is a function, it will be called with a given word as the first paramater, awaiting the corresponding attribute in return. The attribute is assigned to each word, where the attribute is not already present.

---

`animationDuration = 5000`

---

`containerSizeUpdateInterval = 1000`

A number for the update interval in milliseconds.
