# Software Studio 2023 Spring  
## Assignment 01 Web Canvas

### Scoring

| **Basic Components**                             | **Score** | **Check** |
| :----------------------------------------------- | :-------: | :-------: |
| Basic control tools                              | 30%       | Y         |
| Text input                                       | 10%       | Y         |
| Cursor icon                                      | 10%       | Y         |
| Refresh button                                   | 5%        | Y         |

| **Advanced Tools**                               | **Score** | **Check** |
| :----------------------------------------------- | :-------: | :-------: |
| Different brush shapes                           | 15%       | Y         |
| Undo/Redo buttons                                | 10%       | Y         |
| Image tool                                       | 5%        | Y         |
| Download                                         | 5%        | Y         |

| **Other Useful Widgets**                         | **Score** | **Check** |
| :----------------------------------------------- | :-------: | :-------: |
| Name of widgets                                  | 1~5%      | Y         |

---

### How to Use

Describe how to use your web app and optionally include images to illustrate.

The toolbar is on the left side, and the main canvas area is on the right.

### Tools

The background of the selected tool will change color.

#### Brush

Click to use the brush tool for drawing. This is implemented using `moveTo` and `lineTo`. Drawing stops if the cursor is dragged outside the canvas area.

#### Eraser

Click to use the eraser tool. It works the same way as the brush but changes `globalCompositeOperation` to `destination-out`. It switches back to `source-over` when using other tools.

#### Rectangle

Click to draw rectangles. The starting point and current cursor location define the diagonal. It uses `strokeRect` to draw.

#### Circle

Click to draw circles. The starting point and current cursor location define the diameter. It uses `arc` to draw.

#### Triangle

Click to draw triangles. It first draws a line from the starting point to the cursor, mirrors that line, then connects back to form a triangle.

#### Undo

Undo the last action. Each canvas click saves an image to an `ImgStack`. Clicking Undo reverts to the previous state.

#### Redo

Redo the next action. Like Undo, but restores the next state in the stack.

#### Clear

Clears the canvas using `clearRect`.

#### Download

Downloads the image by converting the canvas to a data URL using `toDataURL`.

#### Upload

Uploads an image. Uses an input of type `file` to get the file, converts it to a URL, and displays it on the canvas.

### Bonus Function Description

Describe your bonus functions and how to use them.

#### Straight Line

Draws a straight line from the starting point to the cursor using `moveTo` and `lineTo`.

#### Ellipse

Draws an ellipse using the `ellipse` function.

#### Brush Extra

Holding the brush for a while will convert the stroke into a straight line (similar to GoodNotes). This is done by setting a timer to check the time since the last `move` event.

#### Marker

Uses a highlighter-like tool. Automatically sets the color to yellow and increases transparency. Drawing is similar to the straight line tool.

#### Color-picker

Allows you to pick a color from the canvas. Clicking on a pixel sets the current drawing color to that pixel’s color. Note: Clicking on a blank background will set it to black.

### Web Page Link

Your web page URL:  
https://hw-canvas-110062236.firebaseapp.com/

### Others (Optional)

Anything you want to say to the TAs.
