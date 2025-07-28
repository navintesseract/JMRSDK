# Pointer

Pointers are used to interact with UI or game objects.\
This section describes how pointers are created, how they get updated, and how they determine the object(s) that are in focus.

Pointers receive, process, and manage input data from pointing devices (such as touch, mouse, pen/stylus, and touchpad) in your applications.

## Best practices

### Layout

* It should be clearly visible.
* It should be always center aligned with the pointer
* Direction of ray should be indicative of the actual pointer direction
* Indicative animations should be used to grab the user's attention
* It should give feedback with context for user relevance.

### Content

Interactive experiences typically involve the user identifying the object they want to interact with by pointing at it through input devices such as touch, mouse, pen/stylus, and touchpad. Since, the raw Human Interface Device (HID) data provided by these input devices includes many common properties, the data is promoted and consolidated into a unified input stack and exposed as device-agnostic pointer data. Your applications can then consume the data without worrying about the input device being used.

## Pointer

### States

![](https://tesseractimaging.atlassian.net/wiki/download/attachments/78809441/pointer-states.png?version=1\&modificationDate=1600864293308\&cacheVersion=1\&api=v2)

### Transitions

| **Transitions** | **Front View**                                                                                                                                                                        | **Isometric View**                                                                                                                                                                    |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Enter**       | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809441/Pointer_Enter_Front.gif?version=1\&modificationDate=1600864203702\&cacheVersion=1\&api=v2\&width=224)    | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809441/Pointer_Enter_Persp.gif?version=1\&modificationDate=1600864203831\&cacheVersion=1\&api=v2\&width=224)    |
| **Exit**        | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809441/Pointer_Exit_Front.gif?version=1\&modificationDate=1600864214013\&cacheVersion=1\&api=v2\&width=224)     | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809441/Pointer_Exit_Persp.gif?version=1\&modificationDate=1600864216863\&cacheVersion=1\&api=v2\&width=224)     |
| **Interact**    | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809441/Pointer_Interact_Front.gif?version=1\&modificationDate=1600864220656\&cacheVersion=1\&api=v2\&width=224) | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78809441/Pointer_Interact_Persp.gif?version=1\&modificationDate=1600864223003\&cacheVersion=1\&api=v2\&width=224) |
