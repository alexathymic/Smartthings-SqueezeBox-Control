# **Smartthings Squeezebox Player/Presets Set Up**

Each player has several optional preferences in settings.  This allows for each player to hopefully function as seamlessly as possible.  My goal in home automation is the least amount of human intervention as possible. For example, in our household, the shuffle option is either a great thing, or the bane of artist integrity, depending on who is listening to what. So options for shuffle on and off were manditory, who wants to hunt down a shuffle button if the music starts by itself.

If none of this matters to you, simply ignore it all, nothing is required for proper operation.

### **Player Options Instructions**

**Voice for Speech** Select a voice to use with the speak command if you don't like the default of Salli

**Volume for Speech** Select a volume that the speak command will use. Volume wil be changed for speech event, and then restored to previous value. This comes in handy if you are using Chromecast devices such as a Google Home.

**Turn off Shuffle/Repeat**  Include a shuffle and/or repeat **off** command with your stop command.  A must have in our home. Options are Suffle, Repeat, both or none.

**SquezeLite**  This is of value if you are going to use speech/announcements.  SqueezeLite implementations have a known issue that they cannot handle very short tracks, which most speech is.  Mark this as yes, if you want to receive a warning that your track is too short.  Track lengths under 5 seconds get flagged.  The solution is to be more verbose, usually getting beyond 11-12 words is sufficient.  Otherwise, the player acts like it is playing, but nothing is heard, and timer continues to go up until something/someone intervenes.  As far as I know this does not impact other players, including Chromecasts, even though they report as SqueezeLite players.

**Button 1-3** The real fun of having Squeezebox in Smarthings is automation, which means play music for me.  These function as player presets, which will send any valid HTTP command to the player, including predefined groups of music, such as, artist, album, playlist, favorite, and if you can figure it out, streaming.

Valid commands can be found in the LMS Server help in Help -> Technical Information -> The Logitech Media Server Remote Control

You only need to supply the parameter info (p0-p4), the device handler will fill in everything else.

Remember these apply only to the one player.  Each player can have its own set of similar or completely different commands.

So for example if you wanted to play genre jazz, enter p0=playlist&p1=loadalbum&p2=Jazz or to play an artist p0=playlist&p1=loadalbum&p2=\*&p3=Nick%20Lowe&p4=\*  Note that spaces must be unicode replaced.  So, to play your playist called Morning Mix, p0=playlist&p1=play&p2=Morning%20Mix, and yes, it is case sensitive.

With some internet searching, you may find syntax for things like Pandora.

**Button 1-3 Extra Commands**

Again, control for shuffle/repeat for each preset.  Here if only one of the Shuffle/Repeat is selected, then the other is turned off.  If turned on, Shuffle is by song, and repeat is by playlist
