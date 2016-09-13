# postForm
postForm is an open-source JQuery plugin that helps you post your form including files without (re)loading pages using Ajax.

### Getting Started
```html
<script src="gapostform.js"></script>
```
### How to use
```javascript
$("form").postForm({
  url: 'file.php'
  dataType: 'json',
  success: function(result){
    if(typeof result.done != 'undefined' && result.done == true) console.info('Done');
  },
  error: function(xhr, status){
    console.error('Error!\n' + status);
  },
  beforeSend: function(){
    console.log('Sending your form');
  },
  complete: function(){
    console.log('Form is completed');
  }
});
```
## Who I am
[Follow me on Twitter](https://twitter.com/abewichner) or [Find me on Facebook](https://www.facebook.com/abe.wichner)
