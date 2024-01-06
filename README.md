# mypkg
2023年度後期ロボットシステム学で使用したros2のリポジトリです
  
[![test](https://github.com/higumaharuto/ros2_/actions/workflows/test.yml/badge.svg)](https://github.com/higumaharuto/ros2_/actions/workflows/test.yml)  
  
## インストール方法  
  
* ROS2がインストールされてない方は各自インストールお願い致します。 
  
* インストールされている方は以下のコマンドでこのリポジトリを手元にコピーしてください。  
```  
$ git clone https://git@github.com:higumaharuto/ros2_.git  
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
* talker.pyとlistener.pyを一度に立ち上げるものであり、ノードを操作・管理するようなもの。  
     * 複数のノードを一度に立ち上げる  
  
# 実行例  
## talker.pyとlistener.py
* 端末1  
```  
$ ros2 run mypkg talker  
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
```
Ctrl+Cを入力すると終了します。  
## talk_listen.launch.py  
* 端末1  
```  
$ ros2 launch mypkg talk_listen.launch.py  
[INFO] [launch]: All log files can be found below /home/higuma/.ros/log/2023-12-21-04-35-48-332105-HiBear8610-5627  
[INFO] [launch]: Default logging verbosity is set to INFO  
[INFO] [talker-1]: process started with pid [5628]  
[INFO] [listener-2]: process started with pid [5630]  
[listener-2] [INFO] [1703100949.072531815] [listener]: Listen: 0  
[listener-2] [INFO] [1703100949.559222866] [listener]: Listen: 1  
[listener-2] [INFO] [1703100950.060007871] [listener]: Listen: 2  
[listener-2] [INFO] [1703100950.559930322] [listener]: Listen: 3  
[listener-2] [INFO] [1703100951.059893784] [listener]: Listen: 4  
[listener-2] [INFO] [1703100951.558489960] [listener]: Listen: 5  
[listener-2] [INFO] [1703100952.059958933] [listener]: Listen: 6  
[listener-2] [INFO] [1703100952.558618479] [listener]: Listen: 7  
[listener-2] [INFO] [1703100953.058733515] [listener]: Listen: 8  
[listener-2] [INFO] [1703100953.558680607] [listener]: Listen: 9  
[listener-2] [INFO] [1703100954.060043516] [listener]: Listen: 10  
[listener-2] [INFO] [1703100954.559093037] [listener]: Listen: 11  
[listener-2] [INFO] [1703100955.058720087] [listener]: Listen: 12  
[listener-2] [INFO] [1703100955.559313026] [listener]: Listen: 13  
[listener-2] [INFO] [1703100956.058817465] [listener]: Listen: 14  
[listener-2] [INFO] [1703100956.558704345] [listener]: Listen: 15  
[listener-2] [INFO] [1703100957.059597382] [listener]: Listen: 16  
[listener-2] [INFO] [1703100957.560937831] [listener]: Listen: 17  
[listener-2] [INFO] [1703100958.060128164] [listener]: Listen: 18  
[listener-2] [INFO] [1703100958.560019931] [listener]: Listen: 19  
[listener-2] [INFO] [1703100959.059887932] [listener]: Listen: 20  
[listener-2] [INFO] [1703100959.560232976] [listener]: Listen: 21  
[listener-2] [INFO] [1703100960.059045630] [listener]: Listen: 22  
[listener-2] [INFO] [1703100960.560141689] [listener]: Listen: 23  
[listener-2] [INFO] [1703100961.059141876] [listener]: Listen: 24  
[listener-2] [INFO] [1703100961.560028412] [listener]: Listen: 25  
[listener-2] [INFO] [1703100962.059742883] [listener]: Listen: 26  
[listener-2] [INFO] [1703100962.559866807] [listener]: Listen: 27  
[listener-2] [INFO] [1703100963.060181918] [listener]: Listen: 28  
[listener-2] [INFO] [1703100963.559978765] [listener]: Listen: 29  
[listener-2] [INFO] [1703100964.058540950] [listener]: Listen: 30  
[listener-2] [INFO] [1703100964.560075946] [listener]: Listen: 31  
[listener-2] [INFO] [1703100965.060088350] [listener]: Listen: 32  
[listener-2] [INFO] [1703100965.560074777] [listener]: Listen: 33  
```
Ctrl+Cを入力すると終了します。  

# 必要なソフトウェア  
* Ubuntu 22.04  

# テスト環境  
* ROS2 Humble  

## 著作権・ライセンス  
* このソフトウェアパッケージは、3条項BSDライセンスの下、再頒布および使用が許可されます。  
  
* このパッケージのコードは、下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを、本人の許可を得て自身の著作としたものです。  
* スライドは[こちら](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)です。  
  
* © 2023 higumaharuto



