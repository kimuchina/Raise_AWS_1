# ルートユーザーをMFAで保護する方法
'セキュリティ認証情報'→「MFAを割り当てる」をクリックすると、デバイス名を入力する欄が表示されます。自分のスマホに送られてくる認証コードがルートユーザーであることがすぐにわかるようなデバイス名にしましょう。MFAデバイスを選択する欄は認証アプリケーションにしてください。
次に、QRコードをGoogle Authenticatorで読み込むと認証コードが表示されるので、その異なる認証コードを二つ入力します。これでルートユーザーをMFAで保護できます。

# BillingをIAM ユーザーで閲覧できるようにする方法
マネジメントコンソールにあるルートユーザー名(人によって異なる)から「アカウント」をクリックします。画面遷移後、下にスクロールすると「IAMユーザ/ロールによる請求情報へのアクセス」があるので「IAMアクセスのアクティブ化」にチェックを入れて「更新」をクリックしてください。サイドバーから「ポリシー」を選択して、「ポリシーを作成」をクリックします。検索欄に「Billing」を記述して、それを選択してください。今回は要件が閲覧だけですので「読み取り」にチェックを入れて、「次へ」をクリック。任意のポリシー名を入力し、「ポリシーの作成」をクリックすることでBillingをIAM ユーザーで閲覧できます。

# AdministratorAccess権限のIAM ユーザーを作成する方法
ルートユーザーでログインし、画面の上の検索欄から「IAM」と検索してください。サイドバーの「ユーザー」をクリックします。任意のユーザー名を入力し、「AWS マネジメントコンソールへのユーザーアクセスを提供する 」→「IAM ユーザーを作成します」→「自動生成されたパスワード」→「ユーザーは次回のサインイン時に新しいパスワードを作成する必要があります」をクリックしてください。今回は既存のIAMユーザー/グループがないので「ポリシーを直接アタッチする」を選択します。検索欄に「AdministratorAccess」で検索し、チェックを入れて「次へ」をクリック。これまでに記入した内容に間違いがないことを確認し、「ユーザーの作成」をクリックしてください。
これでAdministratorAccess権限のIAM ユーザーを作成することができますが、最後にCSVファイルを必ずダウンロードしておいてください。次回からこのIAMユーザーを利用するために必要となる認証情報が書かれています。

# Cloud9を作成する方法
サービスメニューから「Cloud9」と検索し、「環境を作成」をクリックします。任意の名前を記入して、今回は学習用にEC2を作成するだけなので一番スペックの低い「t2.micro」を選択します。その他の項目で変更点がなければ「作成」をクリックすることでCloud9を作成することができます。

# Cloud9でのプログラム作成から実行まで
「New File」をクリックし、任意のファイル名を記述します。そのファイルにコードを書き、「Run」を押すことでコードを実行することができます。
