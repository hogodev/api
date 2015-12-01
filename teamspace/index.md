## HoGo REST API

![hogo](http://simplifiedbox.com/nitcms/images/HoGoIntroduction/Slide7.PNG)


Following is the design philosophy applied to HoGo API.
* API protocol must be HTTP or HTTPS
* API request parameters must be passed using query string for APIs that require GET
* API request parameters must be “application/x-www-form-urlencoded” for APIs that require POST
* API response body format must be JSON except when binary data returned
* All API response object has following properties
### General error status

|Status|Description|
|:----|:----|
|UserAlreadyExist|There is a user who has same e-mail value|
|SessionIDNotFound|Not found user Session ID or Session ID request not valid|
|SessionExpired|Session was expired|
|InputParameterError|Parameter request is not valid|

For more infomation about HoGo please reference at http://www.hogodoc.com <br/>
If any question regarding to APIs usage and customization support, please get in touch with us at http://www.hogodoc.com/contact-us
