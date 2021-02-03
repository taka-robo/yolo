# yolo
yoloの学習用リポジトリ

## Yolo v5
https://github.com/ultralytics/yolov5

## google cloabのセッション切れ対策
### 90分対策
F12→Console
```
function ClickConnect(){
  console.log("60sごとに再接続");
  document.querySelector("colab-connect-button").click()
}
setInterval(ClickConnect,1000*60);
```
### 12時間対策
途中経過を保存できればいけそう．
### 参考文献
https://qiita.com/PoodleMaster/items/5f2cc3248c03b03821b8
