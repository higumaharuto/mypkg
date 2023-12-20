# ros2_
2023年度後期ロボットシステム学で使用したros2のリポジトリです
  
[![test](https://github.com/higumaharuto/ros2_/actions/workflows/test.yml/badge.svg)](https://github.com/higumaharuto/ros2_/actions/workflows/test.yml)  
  
## ROS2のインストール方法  
* 以下の手順でコマンドの入力をします。  
```  
$ git clone https://github.com/ryuichiueda/ros2_setup_scripts  
$ cd ros2_setup_scripts  
$ ./setup.bash  
$ source ~/.bashrc  
```  
* インストール後、初期状態のパッケージの作成をする。  
```  
$ cd ~/ros2_ws/src/  
$ ros2 pkg create mypkg --build-type ament_python  
```  
  
* 以下のコマンドでこのリポジトリを手元にコピーしてください。  
```  
$ git clone git@github.com:higumaharuto/ros2_.git  
```  
  
* 最後にビルドしてください。  
```  
$ ( cd ~/ros2_ws && colcon build )  
```  
  
# 説明
## talker.py  
* パブリッシャーを持つノード。数字をカウントアップし、トピック/countupを通じて16ビット符号つき整数であるメッセージの型で送信する。  
  
## listener.py  
* サブスクライバーを持つノード。 トピック/countupからメッセージをもらって表示  
  
## talk_listen.launch.py  
* talker.pyとlistener.pyを一度に立ち上げるノード。  
     * 複数のノードを一度に立ち上げる  
  
# 実行例  
## talker.pyとlistener.py
* 端末1  
```  
  
```  
* 端末2
```  
  
```  
  
## talk_listen.launch.py  
* 端末1  
```  
  
```  

# 必要なソフトウェア  
* ubuntu-22.04    
# テスト環境  
* rosdep  
## 著作権・ライセンス  
* このソフトウェアパッケージは、3条項BSDライセンスの下、再頒布および使用が許可されます。  
  
* このパッケージのコードは、下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを、本人の許可を得て自身の著作としたものです。  
* スライドは[こちら](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)です。  
  
* © 2023 higumaharuto



