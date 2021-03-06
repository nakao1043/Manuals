#### GitによるSF開発環境の管理

※以下はVSCodeを前提とした操作です

- 環境構築

1. ##### remote環境から環境をクローン

   1. 「リポジトリのクローン」を選択
   2. remote環境のPathを入力
      ![image-20211220143108533](img/image-20211220143108533.png)
   3. クローン先のディレクトリを指定
      ![image-20211220143357112](img/image-20211220143357112.png)
   4. クローンに成功した場合、下図のメッセージが表示される

      ![image-20211220143446942](img/image-20211220143446942.png)
   5. 「開く」をクリックして、クローンしたディレクトリ（以下、local環境）を開く

   

2. ##### local環境でdev ブランチをベースに自身のブランチを作成

   ブランチ名は[firstName_initial]-[lastName]Dev
   例）s-nakaoDev
   ![image-20211220150752857](img/image-20211220150752857.png)

   ※開発作業は上記の個人ブランチで必ず行う

   

3. ##### マージ作業

   ##### 前提：SF上のソースとremote環境のdev ブランチの同期が必ず取れている
   ##### 作業完了後、必ずマースマージを行う（例:1機能、1画面改修が終わった）

   1. local環境でdev ブランチをプル
   
     ![image-20211220151805957](img/image-20211220151805957.png)

      

   2. local環境でdev ブランチに自身のブランチをマージ

      例）「s-nakaoDev」を「dev」へMerge

      1. ブランチを「dev」に切り替え
         ![image-20211220152611301](img/image-20211220152611301.png)

         

      2. 「dev」へ「s-nakaoDev」をマージ
         ![image-20211220152757079](img/image-20211220152757079.png)
         
         
         ![image-20211220153030208](img/image-20211220153030208.png)
         
         
         
      3. 競合があれば**適切に**解消し、解消内容についてもコミット
         ![image-20211220151933612](img/image-20211220151933612.png)


   3. プッシュ
   
      ![image-20211220153204625](img/image-20211220153204625.png)
