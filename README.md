1. S3にバケットを作成して、jsonファイルを保存
<img width="1032" alt="20" src="https://user-images.githubusercontent.com/65029417/187232271-b077d6af-f0bc-479f-bed5-3891fd16a06c.png">

2. s3のバケットに保存したjsonファイルを読み込んで、新たなjsonファイルをs3に保存出来るように修正。

3. lambda関数を作成し、2で作成したソースコードをzip化して、lambda関数にアップロードする。
<img width="1291" alt="21" src="https://user-images.githubusercontent.com/65029417/187233310-4d530853-fc56-4454-81a9-04d0959f4874.png">

4. lambda関数にAmazonS3FullAccessポリシーが含まれている、LAMロールを付与する。(lambda関数がs3にアクセスするため。)
<img width="617" alt="22" src="https://user-images.githubusercontent.com/65029417/187234062-76778ede-0874-445c-81f9-83da3cebb150.png">

5. lambda関数でテストを実行すると成功する。
<img width="1277" alt="23" src="https://user-images.githubusercontent.com/65029417/187234411-9b5f5835-6033-40bf-9af5-ff810b5040e9.png">

6. s3バケットに新たなファイル(b.json)が作成されていることを確認。
<img width="938" alt="24" src="https://user-images.githubusercontent.com/65029417/187234820-e7b2d0cc-c043-4f07-9104-0b79338778b9.png">
