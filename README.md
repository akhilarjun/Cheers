# Cheers
An AngularJs plugin that will help you create small notifications on desktop, and at the same time the same would appear as a toast on Mobile devices, i.e. irrespective of the OS

###[Demo Here](http://akhilarjun.github.io/Cheers/demo.html)

##How To:
First you have to include the _cheers.js_ file to your page
```html
<script type="text/javascript" src='js/cheers.js'></script>
```
And then initialise it in your angular application as follows,
```js
/*Edited For Brewity*/

var app = angular.module("app",['cheers']);

/*Edited For Brewity*/
```
Then include the tag in your HTML file
```html
/*Edited For Brewity*/

<cheers></cheers>

/*Edited For Brewity*/
```
Now include the _toast_ service to your controller and Voila! you get your Toast/Notification on your screen
```js
/*Edited For Brewity*/

app.controller("demoController",["$scope","toast",function($scope,toast){
toast.setMsg("Cheers");
}]);

/*Edited For Brewity*/
```

###API  :
**setMsg** : This function accepts 4 parameters of which first one is mandatory , the message itself; and rest three are optional which can be used to controll the duration of the notification, the fading in speed and fading out speed respectively.
```js
/*Edited For Brewity*/

toast.setMsg("Cheers",2000); /*This message stays on screen for 2 seconds*/

/*Edited For Brewity*/
```
If multiple _.setMsg()_ functions are called one after the other. All the notifications would be queued automatically, and woudl be called in their triggering order.

**hide** : This function hides the active toast explicitly.
```js
/*Edited For Brewity*/

toast.hide();

/*Edited For Brewity*/
```
