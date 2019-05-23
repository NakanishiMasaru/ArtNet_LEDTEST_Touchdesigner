 # 説明
全体
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/fcd39b26-d767-7bd9-3d08-1d34d5999344.png)

流れ、
複数のButtonをreNameでChanNameをOSCのRouteNameに割り当て。
ChanNameごとにOSCを送信するようChopExcute。

Button
Momentaryに変更して押下時に変化するように
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/f4ec278a-b281-a128-3814-3a17587aa45e.png)

constant_OSC_routeName
ここのChanNameを変更することで複数のroute分けかできるようになっています。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/debdeed4-301d-fef7-6f3d-471caa319334.png)


chopExcute
上記の流れになるようPythonで書いてます。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/f3efd912-8195-9267-7c39-063e512c178a.png)

oscout DAT
ここで送信先ip(C4-ExtendのIP)とport(8000)を設定します。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/b54a0248-0fd0-d936-89dd-8b03c75b3570.png)

