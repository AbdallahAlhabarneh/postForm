# postform.js
postForm is an open-source JQuery plugin that helps you post your form including files without (re)loading pages using Ajax.

### Getting Started
You can either copy the following html script tag:
```html
<script src="https://raw.githubusercontent.com/AbdallahAlhabarneh/postForm/master/gapostform.js"></script>
```
or download the script file from [here](https://github.com/AbdallahAlhabarneh/postForm/archive/master.zip).
### How to use
```javascript
$("#myform").on("submit",function(e){
  $(this).postForm({
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
});
```
## Follow me on social media
[Follow me on Questific](https://www.questific.com/user/alhabarneh) or [Find me on Facebook](https://www.facebook.com/aalhabarneh)

## Author and License
Created and maintained by [Abdallah Alhabarneh](https://github.com/AbdallahAlhabarneh) under the MIT license.
