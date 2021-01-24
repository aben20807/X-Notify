# X:/Notify

The main goal of this library is to provide developers with a good looking notification system with a single ".js" file. All the styling and such would be included in that file.

### Installation

Put "x-notify.js" in a directory such as "assets/js/", and then, in your "<head>" tag:

````
<script src="./assets/js/x-notify.js"></script>
````

### Usage:

````
const Notify = new XNotify();
````
````
Notify.success({ 
	title: "Title", 
	description: "Description", 
	duration: 4000 
});
````

The above would show a notification on the top right of the screen and it'd stay there for 4 seconds before disappearing. There are quite a few options you can change, such as:

````
Notify.error({
	position: "BottomLeft",
	title: "Failed to Upload File",
	description: "The file you submitted couldn't be uploaded.",
	duration: 4000,
	background: "rgb(200,50,0)",
	color: "rgb(255,255,255)"
});
````

There are 4 different notification types: "success", "error", "alert", and "info", all of which can be used like so:

````
Notify.success();
Notify.error();
Notify.alert();
Notify.info();
````

By default, each type has a different and appropriate background and font color, though they can all be changed as shown above.

Here's a list of all the options you can use, and acceptable values:

|Option|Type|Value|Description|
|------|----|-----|-----------|
|position|String|"TopRight", "BottomRight", "BottomLeft", "TopLeft"|Where the notification popup would appear.
|title|String|Usually, some short text.|The title of the notification; something like "Upload Error", or "Form Submitted".|
|description|String|A longer description of the event.|A description of the event the notification was shown for.|
|duration|Integer|Any integer.|The duration, in milliseconds, that the notification would stay on screen for.|
|background|String|"rgb(r,g,b)", "rgba(r,g,b,a)", "#RRGGBB"|The color of the background of the notification. Can be any RGB, RGBA, or hex value.|
|color|String|"rgb(r,g,b)", "rgba(r,g,b,a)", "#RRGGBB"|The color of the font of the notification. Can be any RGB, RGBA, or hex value.|