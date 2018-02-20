[![APEX JavaScript](https://cdn.rawgit.com/gisprogrammer/apex-github-badges/6ed914a1/badges/apex-javascript-badge.svg)](<LINK>)
[![APEX Education](https://cdn.rawgit.com/gisprogrammer/apex-github-badges/c527f26f/badges/apex-education-badge.svg)](<LINK>)
# APEX-Cards-online-search
Oracle APEX Cards jQuery Live Search
## Preview
![](https://github.com/gisprogrammer/APEX-Cards-online-search/blob/master/emp_example.gif)
## How to ...
### Add text field item to cards region
![](https://github.com/gisprogrammer/APEX-Cards-online-search/blob/master/page_item.png)
### Add dynamic action event
![](https://github.com/gisprogrammer/APEX-Cards-online-search/blob/master/da_event.png)
### Edit dynamic action javascript code
![](https://github.com/gisprogrammer/APEX-Cards-online-search/blob/master/da_javascript.png)

### Key release dynamic action javacript code
```javascript
var searchTerm = this.triggeringElement.value.toLowerCase();
$('.t-Cards li').each(function(){
    $(this).attr('data-search-term', $(this).text().toLowerCase());
});
$('.t-Cards li').each(function(){
    if ($(this).filter('[data-search-term *= ' + searchTerm + ']').length > 0 || searchTerm.length < 1) {
        $(this).show();
    } else {
        $(this).hide();
        }
    });
```
## Demo application
https://apex.oracle.com/pls/apex/f?p=130451:20
credentials: demo\demo
