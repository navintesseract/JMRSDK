# Voice

Voice is one of the key forms of input. It allows you to directly command without having to use hand gestures. Voice input can be a natural way to communicate your intent. Voice is especially good at traversing complex interfaces, because it lets users cut through nested menus with one command.

## Best practices <a href="#voice-bestpractices" id="voice-bestpractices"></a>

Below are some practices that will aid in smooth speech recognition.

* **Use concise commands** - When possible, choose keywords of two or more syllables. One-syllable words tend to use different vowel sounds when spoken by persons of different accents. Example: "Play video" is better than "Play the currently selected video"
* **Use simple vocabulary** - Example: "Show note" is better than "Show placard"
* **Make sure commands are non destructive** - Make sure any action that can be taken by a speech command is non destructive and can easily be undone in case another person speaking near the user accidentally triggers a command.
* **Avoid similar sounding commands** - Avoid registering multiple speech commands that sound very similar. Example: "Show more" and "Show store" can be very similar sounding.
* **Unregister your app when not it use** - When your app is not in a state in which a particular speech command is valid, consider unregistering it so that other commands are not confused for that one.
* **Test with different accents** - Test your app with users of different accents.
* **Maintain voice command consistency** - If "Go back" goes to the previous page, maintain this behavior in your applications.
* **Avoid using system commands** - The following voice commands are reserved for the system. These should not be used by applications.
  * "Hey Cortana"
  * "Select"
  * "Go to start"

## Top things users should know about "speech" in mixed reality <a href="#voice-topthingsusersshouldknowabout-speech-inmixedreality" id="voice-topthingsusersshouldknowabout-speech-inmixedreality"></a>

* Say **"Select"** while targeting a button (you can use this anywhere to click a button).
* You can say the **label name of an app bar button** in some apps to take an action. For example, while looking at an app, a user can say the command "Remove" to remove the app from the world (this saves time from having to click it with your hand).

## Voice feedback states

When Voice is applied properly, the user understands **what they can say and get clear feedback** the system **heard them correctly**. These two signals make the user feel confident in using Voice as a primary input. Below is a diagram showing what happens to the cursor when voice input is recognized and how it communicates that to the user.

![](../.gitbook/assets/91325028.png)

## **Jio Mixed Reality Voice Interaction Guidelines**

| **Dos**                                                                          | **Don’ts**                                                                                |
| -------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| <ul><li>Concise commands</li><li>Simple Vocabulary</li><li>Consistency</li></ul> | <ul><li>Single syllable commands</li><li>System commands</li><li>Similar sounds</li></ul> |

| **Pros**                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | **Cons**                                                                                                                                                                                                                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <ul><li>Reduces time and effort- Imagine just telling the computer what to do instead of having to do tasks manually. Hella time-saving.</li><li>Socially acceptable- People around us all talk on their smartphones, so it is not something that would be seen as weird. (Unless of course, you do it in a public setting with a high tone).</li><li>Routine- Done well, this form of interaction can become routine quickly, as it is intuitive and feels natural.</li></ul> | <ul><li>Accent- What if the MR does not understand your accent? If it does understand, what about the context?</li><li>Quantify- Supposedly you tell the MR computer to reduce the volume, or increase it, what is it supposed to do? How much louder do you want it? Think about checking your e-mail and you say “zoom in”; well, how much?</li></ul> |
