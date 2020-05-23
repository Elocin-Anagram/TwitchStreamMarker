A HTML/Javascript that will place a marker on a streamers timeline on web page load or refresh if the streamer is live at the time. Requires you to create an app thru https://dev.twitch.tv/login to generate a Client-ID and Generate a Oath token. I recommend this token generator https://twitchapps.com/tokengen/ as it is easier than setting up your own local host server and code to generate one with twitch. You will also need your twitch User id which is a number, and is different from your User name. Once you have Client-ID, Oath token, and user_id number. Fill them into the javascript in the appropriate places. The code has notes that tells you where. 

OBS SETUP FOR HOTKEYS
This will funtion much like a NOT Gate. I will assume you do not know the function of a NOT Gate, also known as an inverter. When the input of a Not gate is in a high state/ on state the output is in a Low / off state. 

In OBS Create a scene and call it Marker_

In Marker_, Create a browser source called Marker0
	Check "Local file" Select "Marker.HTML" 
	Set the file path to the script
	Check "Shutdown source when not visiable"
	Cech "Refresh browser when scene becomes active"
Click ok

In Marker_, Create a browser source called Marker1
	Check "Local file" Select "Marker.HTML" 
	Set the file path to the script
	Check "Shutdown source when not visiable"
	Cech "Refresh browser when scene becomes active"
Click ok

In Marker_, Create a Color Source.
	Click "Select color"
	Select Black or put HTML: #000000
	Select ok
	Set the width and height to cover the entire screen.
	Select ok

Arrange the order of sources as to be like this:

			Color Source
			Marker0
			Marker1

Mute or unsee Marker0
Click on Contols go to settings
Click on Hotkeys
Scoll to Marker0 and Marker1 in the list
Set the hotkey for Marker0 and Marker1 (show and hide) to be the same hotkey.
Click apply
Click ok
I recommend the Page Down/Page up key, as I do not know of any conflicts with any game that would cause problems. It is also the same buttons found on the DinoFire Presentation Clicker ring. Usefull for VR applications and will not interfere with contollers. I.E. Index/Knuckles controlers.

Now when you push your chosen hotkey Marker0 will go visable and Marker1 will go invisable just like the function of a Not Gate/inverter, and sending your marker requests to twitch every time you press your chosen hot key. Add Scene Marker_ to any scene that you will be live with.

As a side note the black color source on top is a security feature. I don't know what will happen when the oath token expires, or if the code breaks. To keep your credentials safe and hidden... I recommend keeping the black color source on top and all three sources, and locked.

Special thanks to the Twitch dev discord esp @Dist @BarryCarlyon @Marenthyu @foodz who helped me learn how to do this. A special special thanks to @BarryCarlyon who helped me set up the code, and was very patient with me.

Have fun, and be creative.
-Elocin Anagram
