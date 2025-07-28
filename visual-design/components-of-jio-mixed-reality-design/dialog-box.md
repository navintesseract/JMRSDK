# Dialog Box

A dialog box is a temporary pop-up that takes focus from the page or app and requires people to interact with it. It’s primarily used for confirming actions, such as deleting a file, or asking people to make a choice.

## Best practices

### Layout

* Don't use more than three buttons.
* Dialog boxes consist of a header, body, and footer.
* Validate that people’s entries are acceptable before closing the dialog box. Show an inline validation error near the field they must correct.
* Blocking dialogs should be used very sparingly, only when it is critical that people make a choice or provide information before they can proceed. Blocking dialogs are generally used for irreversible or potentially destructive tasks. They’re typically paired with an overlay without a light dismiss.

**Header**

* Locks to the top of the dialog.
* May include an icon to the left of the title.
* Includes a Close button in the top-right corner.

**Footer**

* Lock buttons to the bottom of the dialog.
* Includes one primary button. A secondary button is optional.

**Width**

* Maximum is 2/3rd the background width
* Minimum is 1/2 the background width

**Height**

* Maximum is 1/2 the background height
* Minimum is 1/3 the background height.

### Content

**Title**

* Keep the title as concise as possible.
* Don’t use periods at the end of titles.
* This mandatory content should explain the main information in a clear, concise, and specific statement or question. For example, “Delete this file?” instead of “Are you sure?”
* The title shouldn’t be description of the body content. For example, don’t use “Error” as a title. Instead, use an informative statement like “Your session ended.”
* Use sentence-style capitalization (only capitalize the first word).

**Body copy (Optional)**

* Don't restate the title in the body.
* Use ending punctuation on sentences.
* Use actionable language, with the most important information at the beginning.
* Use the optional body content area for additional info or instructions, if needed. Only include information needed to help people make a decision.

**Button labels**

* Write button labels that are specific responses to the main information in the title. The title “Delete this file?” could have buttons labeled “Delete” and “Cancel”.
* Be concise. Limit labels to one or two words. Usually a single verb is best. Include a noun if there is any room for interpretation about what the verb means. For example, “Delete” or “Delete file”.

## Dialog Box

### States

![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775860/Dialogue-Box_v2-default.png?version=2\&modificationDate=1601359691653\&cacheVersion=1\&api=v2\&width=442)

### Transitions

| **Transitions** | **Front View**                                                                                                                                                                           | **Isometric View**                                                                                                                                                                       |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Appear**      | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775860/DialogBox_Appear_Front.gif?version=5\&modificationDate=1601303093871\&cacheVersion=1\&api=v2\&width=210)    | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775860/DialogBox_Appear_Persp.gif?version=1\&modificationDate=1600950288739\&cacheVersion=1\&api=v2\&width=210)    |
| **Disappear**   | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775860/DialogBox_Disappear_Front.gif?version=4\&modificationDate=1601302787795\&cacheVersion=1\&api=v2\&width=210) | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775860/DialogBox_Disappear_Persp.gif?version=1\&modificationDate=1600950894295\&cacheVersion=1\&api=v2\&width=210) |

## Error Dialog Box

In case of an error the surface color changes to error color as shown below. The error colors are chosen to be bright to fetch user’s attention for immediate action.

### States

![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775860/Dialogue-Box_v2-error.png?version=2\&modificationDate=1601359718255\&cacheVersion=1\&api=v2\&width=442)

### Transitions

| **Transitions** | **Front View**                                                                                                                                                                                | **Isometric View**                                                                                                                                                                            |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Appear**      | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775860/ErrorDialogBox_Appear_Front.gif?version=3\&modificationDate=1601302732311\&cacheVersion=1\&api=v2\&width=210)    | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775860/ErrorDialogBox_Appear_Persp.gif?version=3\&modificationDate=1601302734205\&cacheVersion=1\&api=v2\&width=210)    |
| **Disappear**   | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775860/ErrorDialogBox_Disappear_Front.gif?version=3\&modificationDate=1601302743396\&cacheVersion=1\&api=v2\&width=210) | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775860/ErrorDialogBox_Disappear_Persp.gif?version=3\&modificationDate=1601302745436\&cacheVersion=1\&api=v2\&width=210) |
