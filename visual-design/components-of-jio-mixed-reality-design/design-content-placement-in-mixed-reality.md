# Input Field

Input fields give people a way to enter and edit text. They’re used in forms, modal dialog, tables, and other surfaces where text input is required.

## Types of Text field

* TextFields (without placeholder)
* TextFields (with placeholder)

## Best Practices

### Layout

* Use a multi-line text field when long entries are expected.
* Don't place a text field in the middle of a sentence, because the sentence structure might not make sense in all languages. For example, "Remind me in \[textfield] weeks" should instead read, "Remind me in this many weeks: \[textfield]".
* Format the text field for the expected entry. For example, when someone needs to enter a phone number, use an input mask to indicate that three sets of digits should be entered.

### Content

* Include a short label above the text field to communicate what information should be entered. Don't use placeholder text instead of a label. Placeholder text poses a variety of accessibility issues (including possible problems with color/contrast, and people thinking the form input is already filled out).
* When part of a form, make it clear which fields are required vs. optional. If the input is required, add an asterisk "\*" to the label.
* Use sentence-style capitalization (only capitalize the first word).

## Text Field

### States

![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/Input-Field-Toolkit-States.png?version=2\&modificationDate=1600947016543\&cacheVersion=1\&api=v2\&width=680)

### Transitions

| Transitions   | **Front View**                                                                                                                                                                            | **Isometric View**                                                                                                                                                                        |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Appear**    | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/InputField_Appear_Front.gif?version=1\&modificationDate=1600931646678\&cacheVersion=1\&api=v2\&width=204)    | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/InputField_Appear_Persp.gif?version=1\&modificationDate=1600931650225\&cacheVersion=1\&api=v2\&width=204)    |
| **Enter**     | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/InputField_Enter_Front.gif?version=2\&modificationDate=1600931393520\&cacheVersion=1\&api=v2\&width=204)     | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/InputField_Enter_Persp.gif?version=1\&modificationDate=1600931407125\&cacheVersion=1\&api=v2\&width=204)     |
| **Exit**      | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/InputField_Exit_Front.gif?version=1\&modificationDate=1600931425810\&cacheVersion=1\&api=v2\&width=204)      | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/InputField_Exit_Persp.gif?version=1\&modificationDate=1600931432020\&cacheVersion=1\&api=v2\&width=204)      |
| **Interact**  | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/InputField_Interact_Front.gif?version=1\&modificationDate=1600931438769\&cacheVersion=1\&api=v2\&width=204)  | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/InputField_Interact_Persp.gif?version=1\&modificationDate=1600931442524\&cacheVersion=1\&api=v2\&width=204)  |
| **Disappear** | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/InputField_Disappear_Front.gif?version=1\&modificationDate=1600931806884\&cacheVersion=1\&api=v2\&width=204) | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/InputField_Disappear_Persp.gif?version=1\&modificationDate=1600931812063\&cacheVersion=1\&api=v2\&width=204) |

## Multiline Text Field

### States

![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809561/Input-Field-Multiline-Toolkit-States.png?version=1\&modificationDate=1601620471525\&cacheVersion=1\&api=v2\&width=680)
