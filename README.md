# Normform 2.0

Normform: A tiny CSS plugin to make your web forms beautiful again
Form plugin (6KB)

### [Check out the demos](http://normform.surge.sh/)

## How to use

1. Download `normform.min.css` (or `normform.css` if you wish to customize)
2. Add the following to your project
```
<link rel="stylesheet" href="path-to-norform-folder/normform.min.css">
```
3. Add the `normform` class to your form element
4. Enjoy your forms!

## Documentation

Most structuring questions can be answered by simply taking a look at the included `index.html` file for the proper way to build your form(s) for the best results.

### Fieldsets & Legends

It is completely optional to use `fieldset` and/or `legend`, but to do so is very simple:

```
<fieldset>
    <legend>This is a legend</legend>
    {inner form content goes here}
</fieldset>
```

### Inputs

The text, email, password, and number inputs all follow the structure of `label` > `input`.

Example:
```
<label for="text-input">Text Input:</label>
<input type="text" id="text-input" value="" placeholder="Text input content...">
```

### Select Dropdowns

Default browser select styling is reset and Normform uses a custom `div` to represent the dropdown contents:

```
<label for="select-choice-2">Dropdown Select Choice:</label>
<div class="select-dropdown">
    <select name="select-choice-2" id="select-choice">
        <option value="Choice 1">Choice 1</option>
        <option value="Choice 2">Choice 2</option>
        <option value="Choice 3">Choice 3</option>
    </select>
</div>
```

### Radios & Checkboxes

Radio and checkbox elements follow the structure of `input` > `label`. The default browser radios and checkboxes are hidden and replaced with custom elements.

```
<input type="radio" name="radio-choice" id="radio-choice-1" tabindex="6" value="choice-1" checked>
<label for="radio-choice-1">Choice 1</label>
```

```
<input type="checkbox" name="checkbox-1" id="checkbox-1">
<label for="checkbox-1">Checkbox 1</label>
```

### Textareas

Straightforward:

```
<label for="textarea">Textarea:</label>
<textarea rows="8" name="textarea" id="textarea"></textarea>
```

### Submit & Reset 'Buttons'

Inputs set with a default type of `submit` or `reset` will be automatically styled. If you wish to have both buttons inline with each other, simply group them inside an `inline-buttons` parent element:

```
<div class="inline-buttons">
    <input type="reset" value="Cancel">
    <input type="submit" value="Sign up">
</div>
```

### Error Descriptors

Adding input validation is as simple as including the `required` attribute but if you wish to include additonal error descriptor you need to also include the `requirements` element and place all values inside a parent `div`:

```
<div>
    <label for="password-input">Password Input:</label>
    <input type="password" id="password-input" required  value="" tabindex="3" pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{6,}" placeholder="Secure password">
    <div class="requirements">Your password must be at least 6 characters as well as contain at least one uppercase, one lowercase, and one number.</div>
</div>
```

---

That's it! Enjoy, and if you have any feature request or notice any bugs - please open a ticket!
