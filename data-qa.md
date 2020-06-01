# `data-qa` attributes

## Why add data-qa attributes?
Everyone who is familiar with scripting Selenium automation test know that the
biggest pain in the process is to find a stable unique locator on a page without
writing a long xpath or css selector. Once the scripts are written, if for any
reason those locators change on the DOM, your tests will break.

### Solution -  add data-qa attributes to the elements.
HTML 5 allows attributes to start with `data-` prefixes for passing data values. By adding these custom `data-qa` attributes and values that are used just for the
testing purpose, you can make your tests more stable even when DOM changes and
the values of `id` or `class` or any other attributes needs to change.


## Consistency is Key
![Consistency is Key](images/consistency.jpg)
To be consistent through out the app, please follow the recommendations below to add attribute values. This will help with identifying locators consistently and generating automation code much easier through the chrome extension.

```html
| Element Type  	| Value Prefix 	| Example                            	|
|---------------	|--------------	|------------------------------------	|
| label         	| lbl          	| <label data-qa="lblInfoHeading">     	|
| button        	| btn          	| <button data-qa="btnSubmit">         	|
| input         	| input        	| <input data-qa="inputPassword">      	|
| checkbox      	| chk          	| <checkbox data-qa="chkFulltime">     	|
| dropdown      	| drp          	| <dropdown data-qa="drpSelectStatus"> 	|
| textarea      	| txt          	| <textarea data-qa="txtDescription">  	|
| error message 	| err          	| <div data-qa="errNoAccess">          	|
| message       	| msg          	| <div data-qa="msgSubmitted">         	|
```
