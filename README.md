# Software Studio 2023 Spring
## Assignment 01 Web Canvas


### Scoring

| **Basic components**                             | **Score** | **Check** |
| :----------------------------------------------- | :-------: | :-------: |
| Basic control tools                              | 30%       | Y         |
| Text input                                       | 10%       | Y         |
| Cursor icon                                      | 10%       | Y         |
| Refresh button                                   | 5%       | Y         |

| **Advanced tools**                               | **Score** | **Check** |
| :----------------------------------------------- | :-------: | :-------: |
| Different brush shapes                           | 15%       | Y         |
| Un/Re-do button                                  | 10%       | Y         |
| Image tool                                       | 5%        | Y         |
| Download                                         | 5%        | Y         |

| **Other useful widgets**                         | **Score** | **Check** |
| :----------------------------------------------- | :-------: | :-------: |
| Name of widgets                                  | 1~5%     | Y         |


---

### How to use 

    Describe how to use your web and maybe insert images to help you explain.
    
左邊是工具欄，右邊是Canvas主體

### 工具

選擇中的工具背景會變色。

#### Brush

點選之後可以使用畫筆畫畫，我使用moveto 和 lineto 實踐，若拖曳超出Canvas範圍則會停止。

#### Eraser

點選之後可以使用橡皮擦，使用原理和畫筆一樣，但要將globalCompositeOperation 改成 destination-out，而切回其他工具則需換回 source-over。

#### Rectangle

點選之後可以畫長方形，以起點和cursor位置為對角線，用strokeRect這個function將長方形畫在指定位置上。

#### Circle

點選之後可以畫圓形，以起點和cursor位置為直徑，用arc這個function將圓形畫在指定位置上。

#### Triangle

點選之後可以畫三角形，其原理是先畫一條直線從起點畫到cursor，在鏡像畫一條直線，最後將起點和終點連在一起形成三角形。

#### Undo

回復上一步驟，每次點擊canvas會用一個Imgstack儲存canvas的圖像，按下undo則會回復到上個狀態。

#### Redo

回復下一步驟，每次點擊canvas都會用一個Imgstack儲存canvas的圖像，按下redo則會回復到下個狀態。

#### Clear

清空canvas，利用clearRect清除所有圖像。

#### Download

下載圖片，將canvas利用toDataURL轉成圖URL然後下載。

#### Upload

上傳圖片，先用input type = "file"取得檔案之後將圖檔轉成URL並顯示在canvas裡面

### Bonus Function description

    Decribe your bonus function and how to use it.
#### Straight Line

畫直線，利用moveto和lineto畫出連接起點與cursor位置的直線。

#### Ellipse

畫橢圓，利用ellipse這個函式畫出橢圓形。

#### Brush Extra

將畫筆按著一段時間會將原本的軌跡消除變成直線(像goodnote那樣)，做法就是設一個timer計算上次move的時間，若超過則變成直線模式。

#### Marker

按下可使用螢光筆，在切換為螢光筆時會自動切換為黃色且透明度變高，而繪畫原理則類似straight那樣畫直線。

#### Color-picker

按下之後可使用顏色選擇器，可以用此工具來選擇canvas裡面對應像素之顏色，例如在一張照片中的紫色像素上按下便會將當前顏色變成紫色。備註:若在空白背景按下便會變成黑色。

### Web page link

    your web page URL.
    https://hw-canvas-110062236.firebaseapp.com/

### Others (Optional)

    Anything you want to say to TAs.

<style>
table th{
    width: 100%;
}

</style>
