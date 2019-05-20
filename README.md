# ArtNet_LEDTEST_Touchdesigner
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/c689177b-9df3-fcea-d2e7-50d8baba545f.png)
RGB[0-255]をArtnet出力します。

やっていること
RampにてLED点灯用画像作成、ここでピクセル数を指定できる。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/9d67ef48-25fc-e239-00db-dffb9d574a36.png)

RGB配列のデータpixcelNum*[r,g,b](0-255)がほしいので、
画像をtopToでChopに
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/f165ef9d-2a74-5063-d04c-f23d4429d680.png)

shuffle1でch(r,g,b)をch(r)に統合
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/77393c9f-d412-8605-79ba-40ad713c5b3e.png)

Shuffle2でsampleをchに変換。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/e1cb9a94-0be6-b8a0-8453-34b01bd02c08.png)

Mathで0-1を0-255に
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/73076076-0293-fbeb-f793-eed3d3c88834.png)


TouchdesignerのArtnet設定。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/e449d8d0-34ee-2b8f-29d5-9dac99fa8770.png)
255.255.255でマルチキャストになる。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/71b40db1-a916-f838-b404-4fa35aafb2ba.png)



C4-ExtendでのArtNet確認
Homeから[Settings]/[In/out configuration]の右上ツールセットにInputWatcherがある。Universeを合わせてWATCHINPUTすると今着ているデータを見れる。すごい
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/dd0cbeac-0fc1-d407-07bc-0564aa320cdf.png)

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/142c4ee1-c42f-346c-c588-6d6e78c6885e.png)
カラー情報まで見れる。有難い。
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/149571/4d2ffc85-7896-6c98-6342-0f31a52a5f9e.png)
