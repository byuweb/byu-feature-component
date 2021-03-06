# BYU Feature Card

This component is meant to be used to feature a single piece of content (i.e. news story, calendar event, etc.).
## To Use:

A. Drupal: Likely Coming Soon - a submodule in the module Views Card D7 - You will be able to enable the module, and create a view. The style is defined within the view.

B. Not Drupal:

Reference the js and css file for byu-feature-card:
js: https://cdn.byu.edu/byu-feature-card/1.x.x/byu-feature-card.min.js: 
css: https://cdn.byu.edu/byu-feature-card/1.x.x/byu-feature-card.min.css

Place your content inside <byu-feature-card> tags. Your content should be a direct child to the <byu-card> tag. See the demo at https://github.com/byuweb/byu-feature-card/blob/master/my-component/demo.html
## How It Works



```html
<byu-feature-card class="cardClass navy-title" without-logo>
  <h2 slot="title">Feature</h2>
  <img slot="feature-left" src="#">
  <ul slot="feature-right">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
  <p slot="feature-center">This is where body content goes</p>
</byu-feature-card>
```
The card is divided into three rows: the title row, feature row, and body row. To put elements in the title or body row, set the slot attribute of an element to be `title` or `body`. The feature row can be divided into two sections. To place an element, either add `slot="feature-left"` or `slot="feature-right"` to the element. After forking this repo, you can see a live demo of the component by running the appropriate command from below.

## Styling

_Logo_: By default, the BYU monogram will be on the right of the card title. If you don't want it, just add the `without-logo` attribute (see the example above).

_Title Background Color_: This component comes packaged with predefined, accessible packages for styling the title. Add one of these classes to your byu-feature-card element to change the title background:

- `navy-title`
- `royal-blue-title`
- `dark-gray-title`
- `gray-title`
- `wordpress-gray-title`
- `drupal-blue-title`

In addition, if you'd like to use your own colors, you can use this CSS:

```css
byu-feature-card.cardClass {
  --byu-feature-card-title-background: #002e5d;
  --byu-feature-card-title-color: white;
}
```
The default colors will be a navy blue background with white text.

# Development

To contribute to this repository, fork it, make your changes, then submit a pull request. More information about contributing to web components can be found on the [byu-theme-components wiki](https://github.com/byuweb/byu-theme-components/wiki/Contributing-to-this-Repository).

After forking this repository, you'll need to run the following command in the project folder:

```
npm install
```

To run a local development server with a file watch, run

```
npm start
```

_You should do this before you submit a pull request._ To assemble the final distribution bundle, run

```
npm run build
```

To run automatic unit tests, run

```
npm test
```

## To Be Developed

- Full width feature slot
