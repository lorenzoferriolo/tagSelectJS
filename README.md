# tagSelectJS

A lightweight and customizable JavaScript component that transforms any `<select multiple>` into a tag-style input with full keyboard and mouse support.

## Features

- Keyboard accessibility (A11y)
- Customizable tag and wrapper styles
- Internationalization (i18n) support
- Placeholder management
- Tag removal customization
- Easy integration into existing forms
- Plugin-ready architecture (WIP)

## Installation

Download the `tagSelectJS.js` and `tagSelectJS.css` files and include them in your HTML:

```html
<link rel="stylesheet" href="tagSelectJS.css">
<script src="tagSelectJS.js"></script>
```

## Usage

```html
<select multiple class="select2">
  <option value="1">Tag One</option>
  <option value="2">Tag Two</option>
</select>

<script>
  createTagSelect(".select2", {
    keepOpen: true,
    tagClassExtra: "my-custom-tag",
    wrapperClassExtra: "my-wrapper",
    maxTags: 3,
    placeholder: "Add or select tags...",
    onChange: (values) => {
      console.log("Selected values:", values);
    },
    remove: "✖",
    i18n: {
      remove: "✖",
      added: "Tag added",
      removed: "Tag removed"
    }
  });
</script>
```

## API Options

| Option             | Type     | Description                                             |
|--------------------|----------|---------------------------------------------------------|
| `keepOpen`         | Boolean  | Keep dropdown open after each selection                |
| `tagClassExtra`    | String   | Extra class added to each tag                          |
| `wrapperClassExtra`| String   | Extra class added to the wrapper                       |
| `maxTags`          | Number   | Maximum number of tags allowed                         |
| `placeholder`      | String   | Placeholder text when no tags are selected             |
| `onChange`         | Function | Callback triggered with selected values array          |
| `remove`           | String   | Character or icon used to remove a tag                 |
| `i18n`             | Object   | Object with `added`, `removed`, `remove` messages      |

## License

This project is licensed under the MIT License.