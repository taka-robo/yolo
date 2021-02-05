# yolo
yoloの学習用リポジトリ

## Yolo v5
https://github.com/ultralytics/yolov5

## google colabのセッション切れ対策
### 90分対策
F12→Console
```
function ClickConnect(){
  console.log("600sごとに再接続");
  document.querySelector("colab-connect-button").click()
}
setInterval(ClickConnect,1000*600);
```
### 12時間対策
途中経過を保存できればいけそう．

## ローカルで実行する場合
GTX1060のメモリサイズがgogle colabのGPUより小さいのでbatchサイズに注意  
[簡易的なメモリ量の見積もり方](https://nori-life-log.com/nn%E3%81%AE%E5%AD%A6%E7%BF%92%E3%81%A7%E5%BF%85%E8%A6%81%E3%81%AAgpu%E3%83%A1%E3%83%A2%E3%83%AA%E3%82%92%E7%AE%97%E5%87%BA%E3%81%99%E3%82%8B)
###CUDA
https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exenetwork
### 実行コード
```bash
cd D:\yolo\yolov5
 .\.yolo\Scripts\Activate.ps1
cd yolov5
python .\train.py --batch 4 --epochs 100 --data 'D:\yolo\robomaster2.yaml' --name robomaster
```

## 参考文献
https://qiita.com/PoodleMaster/items/5f2cc3248c03b03821b8
