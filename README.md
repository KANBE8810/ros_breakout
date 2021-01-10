# mitsu_checker/密チェッカー
## 説明
ロボットシステム学の課題2でROSを用いて作成した密チェッカーです｡<br>
OpenCVを用いて人の顔を検出し､人が複数人いた場合やPCに顔が近い場合に｢密です｣という警告の音声を出したり､視覚による警告を行います｡
## デモ動画
準備中
## 動作確認
以下の環境にて動作確認をしています｡
* ROS Melodic
  * OS : Ubuntu 18.04.5 LTS
  * ROS Distribution : Melodoc Morenia 1.14.3
* usb-cam
* OpenCV : version 3.4.3
* Python 2.7.17
また､カメラに関してはdynabookのノートパソコンの内蔵カメラを用いて動作確認いたしました
## 環境構築
1. 本パッケージをインストールします｡
```sh
$cd ~/catkin_ws/src  
$git clone https://github.com/KANBE8810/mitsu_checker.git  
$cd ~/catkin_ws
$catkin_make
```
2. pygameで音を再生するため､pygameをインストールします｡
```sh
$pip install pygame
```
3. usb-camをインストールします｡
```sh
$sudo apt-get update
$sudo apt-get install ros-melodic-usb-cam
```

# 使用方法
1. usb-canを起動します｡
```sh
$roslaunch mitsu_checker usb_cam.launch 
```
2. 本パッケージの人の顔を検知するプログラムを起動します
```sh
$rosrun mitsu_checker mitsu_checker.py
```
3. 警告文を読み上げるプログラムを起動します｡
```sh
$rosrun mitsu_checker mitsu.py
```
尚､1,2,3,の動作はそれぞれ別の端末でコマンドを実行してください

# ライセンス
ROS [BSD 3-Clause License](https://github.com/KANBE8810/mitsu_checker/blob/master/LICENSE)<br>
密の画像は[いらすとやさん](https://www.irasutoya.com/)から用いています([詳しくはこちら](https://www.irasutoya.com/p/terms.html))<br>
警告文の読み上げ音声は[ゆくも!](https://www.yukumo.net/#/)さんで作成いたしました([詳しくはこちら](https://www.yukumo.net/#/about))
