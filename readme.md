Ad4Game SDK For Desktop And Mobile HTML5 Content
=
[Preview](http://ad4game.com/adspec/html5sdk/)
=
Ad4Game created this Javascript library to help HTML5 content publishers integrate Ads into their games or video players.
Usage
-
Easily set the banner id and initialize to display Ad4Game Ads. The script will automatically identify the largest target canvas to overlay.
```javascript
<script type="text/javascript" src="ad4game_html5_sdk.js"></script>
<script type="text/javascript">
	// Add other options here
	ad4game_html5_sdk.setAdBanner("10249");
	ad4game_html5_sdk.init();
</script>
```
Contact your Ad4Game account manager to get your banner id (zoneid)
You can use *10249* to test.


----------


Options
-
> **Note:**
The following options and customizations should be added **before** the *init()* method.

Manually define the target canvas you want to overlay, by introducing its DOM id
```javascript
ad4game_html5_sdk.setTargetCanvas("canvas_DOM_id");
```
Set the Ad banner to one of the available sizes: 1, 2 or 3 (**1** = *300x250*, **2** = *728x90*, **3** = *468x60*)
```javascript
ad4game_html5_sdk.setAdBanner("10249", "2");
```
Set the Ad count-down to 15 seconds (default value is 10 s)
```javascript
ad4game_html5_sdk.setCountDownTime(15);
```
The overlay size is automatically detected to match the canvas area, but you can manually set its width and height by using this method: setOverlaySize("**width**", "**height**")
```javascript
ad4game_html5_sdk.setOverlaySize("500px", "350px");
```
The branding box is hidden by default. Use this method to display a clickable box, showing your brand with a caption: setBrand("**logo_url**", "**official website link**", "**caption**")
```javascript
ad4game_html5_sdk.setBrand("http://games.a4g.com/fog.png", "http://fog.com", "Find more games on FOG.com");
```
Set the "Wait" message. Default value: "**Ad will skip in**", change it to your own audience language (e.g.: "Chargement en cours" in French)
```javascript
ad4game_html5_sdk.setWaitText("Chargement en cours")
```
Set the background color of the overlay area to Red in hexadecimal code. Default value is Black (#000000)
```javascript
ad4game_html5_sdk.setBGColor("#FF0000");
```
Set this method to "false" to display the call-to-action button after the count-down.
```javascript
ad4game_html5_sdk.autoSkip(false);
```
Change the call-to-action text, Default value: "**Play Now**", change it to your own audience language (e.g.: "Kostenlos Spielen" in German)
```javascript
ad4game_html5_sdk.setCTA("Kostenlos Spielen");
```
Use this method to show the Ad in between levels of your games or in-straem for videos (autoSkip = true, count-down = 5 seconds)
```javascript
ad4game_html5_sdk.interLevelShowAd();
```
Change the interLevel count-down to 10 seconds and enable the background transparency:
```javascript
ad4game_html5_sdk.interLevelShowAd(10, true);
```
Frequency capping (in hours) is disabled by default.
Set a number of hours this Ad Unit should not appear again when the ad gets closed.
The following example sets the Ad to show once per 12 hours.
```javascript
ad4game_html5_sdk.setCapping(12);
```
Use this method if you are using the SDK on mobile content. Default value is "false".
```javascript
ad4game_html5_sdk.isMobile(true);
```
