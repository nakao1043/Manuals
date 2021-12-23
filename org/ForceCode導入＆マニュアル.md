#### ForceCode導入＆マニュアル

1. ##### VSCodeの拡張機能「ForceCode」をインストール

   ![image-20211217112405565](img/image-20211217112405565.png)

   

2. ##### 開発環境ディレクトリ指定

   1. 「Ctrl+Shift+P」でコマンドメニュー表示

      「ForceCode: Create Project」を選択

      ![image-20211217112442121](img/image-20211217112442121.png)

      

   2. 開発環境ディレクトリを選択

      ![image-20211217113115865](img/image-20211217113115865.png)

      ※選択したディレクトリ直下にソースが展開される

   

3. ##### 開発環境の設定を行う

   1. 「New Org」を選択

      ![image-20211217113257528](img/image-20211217113257528.png)

      

   2. 実際の開発環境に合わせて環境の種類を選択

      ![image-20211217113434101](img/image-20211217113434101.png)

      

   3. 「No」を選択

      ![image-20211217113612254](img/image-20211217113612254.png)

      ※ファイルセーブと同時にSalesforceへのデプロイを行うか否かのオプション

      ​	デグレを防ぐため基本「No」を推奨

      

   4. 「Source」を選択

      ![image-20211217113827411](img/image-20211217113827411.png)

      

   5. 規定のブラウザでSFログイン画面が表示されるので対象の開発環境にログイン

      ![image-20211217113924849](img/image-20211217113924849.png)

      

   6. ログイン後、開発用メタデータとフォルダが開発環境ディレクトリに生成される

      ![image-20211217114120858](img/image-20211217114120858.png)

      

      ![image-20211217114351797](img/image-20211217114351797.png)

      

4. ##### ソースコード取得

   1. 「Ctrl+Shift+P」でコマンドメニュー表示

      「ForceCode: ForceCode Menu」を選択

      ![image-20211217114845998](img/image-20211217114845998.png)

      ※「Ctrl+Shift+C」で直接呼び出し可能

      

   2. 「Retrieve Package/Metadata」を選択
      

      ![image-20211217115104432](img/image-20211217115104432.png)

      

   3. 必要なソースの種類を選択

      ![image-20211217115321390](img/image-20211217115321390.png)

      

      ※VisualFoce + Apexのみの開発であれば以下がオススメ

      「Choose types」

      ![image-20211217115340552](img/image-20211217115340552.png)

      

      テキストボックスに「Apex」と入力し、以下の4種を選択して「OK」
      ![image-20211217115520378](img/image-20211217115520378.png)
      
      
      
      対象のソースが取得される
      ![image-20211217115633944](img/image-20211217115633944.png)

      

5. ##### 開発方法

   標準のSalesforce CLIと同様にソースコードをVSCode上で修正できる

   ![image-20211217120124564](img/image-20211217120124564.png)

   

   ソースデプロイ時はソース上のコンテキストメニューか「Ctrl + Shift + S」のショートカットで実行
   ![image-20211217120243024](img/image-20211217120243024.png)

   

6. VSCode上で新規VFページを定義

   1. 「Ctrl+Shift+P」でコマンドメニュー表示
      「ForceCode: ForceCode Menu」を選択

   2. 「New」を選択
      ![image-20211223151248982](img/image-20211223151248982.png)

      

   3. 「Visualforce Page」を選択
      ![image-20211223151340180](img/image-20211223151340180.png)

      

   4. 名前を指定
      ![image-20211223151615008](img/image-20211223151615008.png)

      

   5. 新規VFページの**メタデータ**が作成される
      ![image-20211223151853715](img/image-20211223151853715.png)

      ※デプロイしない限り、SF上には反映されない

      

7. VSCode上で新規VFコンポーネントを定義

   1. 6.2.までは同じ

   2. 「Visualforce Component」を選択
      ![image-20211223152000287](img/image-20211223152000287.png)

      

   3. 以降は6.4と同じ

      

8. VSCode上で新規Apexクラスを定義

   1. 6.2.までは同じ

   2. 「Class」を選択
      ![image-20211223152230354](img/image-20211223152230354.png)

      

   3. 以降は6.4と同じ

      

9. VSCode上でApexテストを実施

   1. 画面右のForceCode拡張機能アイコンをクリック
      ![image-20211223152416902](img/image-20211223152416902.png)

      

   2. 「CODE COVERGE」ペインの「Test Classes」内の実行したいテストクラスを選択
      クラス名右の「▶」をクリック
      ![image-20211223152527205](img/image-20211223152527205.png)

      

   3. 実行が正常に終了した場合、以下のメッセージが表示される
      ![image-20211223152811644](img/image-20211223152811644.png)

      

   4. カバレッジは「CODE COVERGE」ペインの「Sufficient Coverage」と「Insufficient　Coverage」から確認できる
      ![image-20211223154941368](img/image-20211223154941368.png)

      - Sufficient Coverage：カバレッジ75%以上のApexクラス
      - Insufficient Coverage：カバレッジ75%未満のApexクラス

      

   5. 通過していないステップをVSCode上から確認可能
      ![image-20211223155239795](img/image-20211223155239795.png)

      未到達ステップが塗りつぶし表示される

