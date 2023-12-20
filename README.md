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
$ ros2 run mypkg talker  
(何も表示されません。)
``` 
何も表示されません。  

* 端末2  
```  
$ ros2 run mypkg listener  
[INFO] [1703099610.832156329] [listener]: Listen: 3  
[INFO] [1703099611.319894370] [listener]: Listen: 4  
[INFO] [1703099611.820156251] [listener]: Listen: 5  
[INFO] [1703099612.320027709] [listener]: Listen: 6  
[INFO] [1703099612.819988524] [listener]: Listen: 7  
[INFO] [1703099613.320026807] [listener]: Listen: 8  
[INFO] [1703099613.820155645] [listener]: Listen: 9  
[INFO] [1703099614.320112295] [listener]: Listen: 10  
[INFO] [1703099614.820145741] [listener]: Listen: 11  
[INFO] [1703099615.320095485] [listener]: Listen: 12  
[INFO] [1703099615.819568145] [listener]: Listen: 13  
[INFO] [1703099616.320050188] [listener]: Listen: 14  
[INFO] [1703099616.819190437] [listener]: Listen: 15  
[INFO] [1703099617.320147676] [listener]: Listen: 16  
[INFO] [1703099617.819915364] [listener]: Listen: 17  
[INFO] [1703099618.319878921] [listener]: Listen: 18  
[INFO] [1703099618.818747612] [listener]: Listen: 19  
[INFO] [1703099619.320038921] [listener]: Listen: 20  
[INFO] [1703099619.820249276] [listener]: Listen: 21  
[INFO] [1703099620.319452949] [listener]: Listen: 22  
[INFO] [1703099620.819270659] [listener]: Listen: 23  
[INFO] [1703099621.319354878] [listener]: Listen: 24  
[INFO] [1703099621.818630933] [listener]: Listen: 25  
[INFO] [1703099622.320069510] [listener]: Listen: 26  
[INFO] [1703099622.819877789] [listener]: Listen: 27  
[INFO] [1703099623.319865548] [listener]: Listen: 28  
[INFO] [1703099623.819956602] [listener]: Listen: 29  
[INFO] [1703099624.320236731] [listener]: Listen: 30  
[INFO] [1703099624.819895413] [listener]: Listen: 31  
[INFO] [1703099625.319678311] [listener]: Listen: 32  
[INFO] [1703099625.819574864] [listener]: Listen: 33  
(Ctrl+Cを入力すると終了します。)
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



