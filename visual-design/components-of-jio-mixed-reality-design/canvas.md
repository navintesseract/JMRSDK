# Canvas

Canvas is the background for laying any User Interface element in Tesseract Mixed Reality Design. The canvas defines the layout and arrangement that plays a huge role in defining the user experience from visual design standpoint.

## Best Practices

### Margins

Margins are the space between content and the left and right edges of the screen.

Margin widths are defined as fixed values at each Canvas size. To better adapt to the screen, the margin width can change at different Canvas size. Wider margins are more appropriate for larger screens, as they create more whitespace around the content.

![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/image-20201002-174424.png?version=1\&modificationDate=1601894776200\&cacheVersion=1\&api=v2\&width=680)

### Curved Edges

Curved edges are directly proportional to the Canvas Size. If canvas size increases then curved edges increases proportionately.

{% hint style="info" %}
**Example** If Canvas size is = 1920px X 1080px ( x ) and Curved edges = 30px ( y ), then **x** and **y** scale proportionately.
{% endhint %}

![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/image-20201002-122338.png?version=1\&modificationDate=1601894814777\&cacheVersion=1\&api=v2\&width=680)

### Gutter

Gutters are the spaces between columns. They help separate content.

Gutter spaces are fixed values at each canvas. To better adapt to the screen, gutter width can change at different canvas size. Wider gutters are more appropriate for larger screens, as they create more whitespace between columns.

![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/image-20201002-174712.png?version=1\&modificationDate=1601894836567\&cacheVersion=1\&api=v2\&width=680)

## Designing Layout of Canvas

### Columns

The Designing area of the screen contains columns which can refer to as content area.\
The number of columns displayed in the grid is determined by the Canvas size at which a screen is viewed.\
**Vertical & horizontal Column Grid** is used as a ruler to maintain design proportion.

![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/image-20201002-175016.png?version=1\&modificationDate=1601894889758\&cacheVersion=1\&api=v2\&width=680)

![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/image-20201002-175114.png?version=1\&modificationDate=1601894991757\&cacheVersion=1\&api=v2\&width=680)

![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/image-20201002-152501.png?version=1\&modificationDate=1601895011960\&cacheVersion=1\&api=v2\&width=680)

## **Canvas**

### **States**

![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/Canvas-Toolkit_v2.png?version=1\&modificationDate=1601658140250\&cacheVersion=1\&api=v2\&width=680)

### **Transitions**

| **Transitions** | **Front View**                                                                                                                                                                  | **Isometric View**                                                                                                                                                                  |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Appear**      | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/canvas_appear.gif?version=6\&modificationDate=1602080256159\&cacheVersion=1\&api=v2\&width=204)    | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/canvas_appear_iso.gif?version=1\&modificationDate=1601537195917\&cacheVersion=1\&api=v2\&width=204)    |
| **Disappear**   | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/canvas_disappear.gif?version=1\&modificationDate=1601537616332\&cacheVersion=1\&api=v2\&width=204) | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/canvas_disappear_iso.gif?version=1\&modificationDate=1601537635457\&cacheVersion=1\&api=v2\&width=204) |

As recommended earlier, use of **Curved UI** elements gives it a more sleek and futuristic look

## **Curved Canvas**

### **Transitions**

| **Transitions** | **Front View**                                                                                                                                                                        | **Isometric View**                                                                                                                                                                    |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Appear**      | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/Canvas_Appear_Front.gif?version=1\&modificationDate=1602066353247\&cacheVersion=1\&api=v2\&width=204)    | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/Canvas_Appear_Persp.gif?version=1\&modificationDate=1602066354343\&cacheVersion=1\&api=v2\&width=204)    |
| **Disappear**   | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/Canvas_Disappear_Front.gif?version=1\&modificationDate=1602066358294\&cacheVersion=1\&api=v2\&width=204) | ![](https://tesseractimaging.atlassian.net/wiki/download/thumbnails/78775667/Canvas_Disappear_Persp.gif?version=1\&modificationDate=1602066361228\&cacheVersion=1\&api=v2\&width=204) |
