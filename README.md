# postForm
postForm is an open-sourse JQuery plugin that helps you post your form including files without (re)loading pages using Ajax.

# Usage
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
