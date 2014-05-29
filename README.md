# jQuery Validate

jQuery Validate is a live input validation plugin.

### Supported Validation Types:
- Phone
- Numeric
- ABA Bank Routing
- Email Addresses
- Matching Other Inputs
- Passwords
- Required
- Date

## Basic Usage

```html
    <input type="text" id="first-name" />
```
```javascript
// Required Field
$('#first-name').validate( { required: true } );
```
By default, the plugin will add CSS classes to the validated input. You can
style these with CSS.

```css
.validate-success {
    border: 1px solid green;
}

.validate-error {
    border: 1px solid red;
}
```

## Callback

###onDone
```javascript
// JavaScript anonymous callback function after validation check.
$('first-name').validate( {
    required: true,
    onDone: function( result ){
        if( !result ){
            console.log("Cannot leave input blank.");
        } else {
            console.log("You typed:"+$(this).val()+" .");
        }
    }
});
``` 