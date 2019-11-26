
<!-- TOC -->

- [はじめに](#はじめに)
- [インストール手順](#インストール手順)
    - [VirtualBox](#virtualbox)
    - [CentOS7のインストール](#centos7のインストール)
    - [ネットワーク設定とSSH接続確認](#ネットワーク設定とssh接続確認)

<!-- /TOC -->

# 1. はじめに
この手順ではVirtualBoxのインストールからCentOs7のインストールとネットワークのセットアップまでを紹介します。

# 2. インストール手順

## 2.1. VirtualBox
VirtualBoxをインストールします。

1. VirtualBoxのインストーラーを起動する。<br />![インストーラー起動](./images/setup/Installing-VirtualBox/01.png)
1. Custom Setupが表示されるので必要であれば編集する。（デフォルトを使用）<br />![カスタムセットアップ1](./images/setup/Installing-VirtualBox/02.png)
1. インストール後の各種設定に聞かれるので必要なものにチェックする。（デフォルトを使用）<br />![カスタムセットアップ2](./images/setup/Installing-VirtualBox/03.png)
1. ネットワークインターフェースをインストールする警告が表示されるので"Yes"を選択する。<br />![警告](./images/setup/Installing-VirtualBox/04.png)
1. インストール直前の確認が促され問題なければInstallを押下する。<br />![インストール確認](./images/setup/Installing-VirtualBox/05.png)
1. インストールが開始される。（インストール中）<br />![インストール](./images/setup/Installing-VirtualBox/06.png)
1. インストールが完了したらFinishを押下する。<br />![インストール完了](./images/setup/Installing-VirtualBox/07.png)

## 2.2. CentOS7のインストール
作成した仮想マシンにCentOS7をインストールする。

1. VirtualBoxを開く。<br />![CentOS7_手順01](./images/setup/Installing-CentOS7/01.png)
1. 仮想マシン > 新規を押下する。<br />![CentOS7_手順02](./images/setup/Installing-CentOS7/02.png)
1. "仮想マシンの作成"の項目を編集する。<br />![CentOS7_手順03](./images/setup/Installing-CentOS7/03.png)
1. メモリを編集する。<br />![CentOS7_手順04](./images/setup/Installing-CentOS7/04.png)
1. ハードディスクを選択する。（今回は仮想ハードディスクを作成）<br />![CentOS7_手順05](./images/setup/Installing-CentOS7/05.png)
1. ハードディスクのファイルタイプを選択する。（今回はVDIを使用）<br />![CentOS7_手順06](./images/setup/Installing-CentOS7/06.png)
1. 物理ハードディスクにあるストレージを選択する。（今回は可変サイズ）<br />![CentOS7_手順07](./images/setup/Installing-CentOS7/07.png)
1. ファイルの場所とサイズを編集して作成する。（場所はデフォルトでサイズは16GB）<br />![CentOS7_手順08](./images/setup/Installing-CentOS7/08.png)
1. 仮想マシン（側のみ）が作成されたことを確認する。<br />![CentOS7_手順09](./images/setup/Installing-CentOS7/09.png)
1. 作成した仮想マシンの設定を開く。<br />![CentOS7_手順10](./images/setup/Installing-CentOS7/10.png)
1. ストレージを選択する。<br />![CentOS7_手順11](./images/setup/Installing-CentOS7/11.png)
1. 属性の光学ドライブにあるディスクマークを選択する。<br />![CentOS7_手順12](./images/setup/Installing-CentOS7/12.png)
1. インストールするCentOS7のイメージを選択する。<br />![CentOS7_手順13](./images/setup/Installing-CentOS7/13.png)
1. イメージが選択された事を確認する。<br />![CentOS7_手順14](./images/setup/Installing-CentOS7/14.png)
1. 仮想マシンの起動を押下する。<br />![CentOS7_手順15](./images/setup/Installing-CentOS7/16.png)
1. 仮想マシンが起動される。<br />![CentOS7_手順16](./images/setup/Installing-CentOS7/17.png)
1. ロード画面が表示される。<br />![CentOS7_手順17](./images/setup/Installing-CentOS7/18.png)
1. インストーラー画面が表示され言語を選択する。<br />![CentOS7_手順18](./images/setup/Installing-CentOS7/19.png)
1. インストール先を選択する。<br />![CentOS7_手順19](./images/setup/Installing-CentOS7/20.png)
1. 先ほど作成したディスクを選択する。<br />![CentOS7_手順20](./images/setup/Installing-CentOS7/21.png)
1. "インストールの開始"を押下する。<br />![CentOS7_手順21](./images/setup/Installing-CentOS7/22.png)
1. ユーザーの設定に切り換わる。<br />![CentOS7_手順22](./images/setup/Installing-CentOS7/23.png)
1. rootのパスワードの編集画面が表示される。<br />![CentOS7_手順23](./images/setup/Installing-CentOS7/24.png)
1. rootのパスワードを編集して完了を押下する。<br />![CentOS7_手順24](./images/setup/Installing-CentOS7/25.png)
1. しばらくすると再起動を促されるので再起動ボタンが表示されたら押下する。<br />![CentOS7_手順25](./images/setup/Installing-CentOS7/26.png)
1. 仮想マシン上でlogin画面が表示される。<br />![CentOS7_手順26](./images/setup/Installing-CentOS7/27.png)


## 2.3. ネットワーク設定とSSH接続確認
下記の手順はNATとホストオンリーアダプターの設定について紹介する。

1. ツール > 作成を押下してホストオンリーネットワークを作成する。<br />![手順1](./images/setup/Setup-Envloyment/01.png)
1. ホストオンリーネットワークが作成されたことを確認する。<br />![手順2](./images/setup/Setup-Envloyment/02.png)
1. 仮想マシンの設定を押下する。<br />![手順3](./images/setup/Setup-Envloyment/03.png)
1. 設定一覧のネットワークを選択する。<br />![手順4](./images/setup/Setup-Envloyment/04.png)
1. タブのアダプター2を開きホストオンリーアダプターを選択する。<br />![手順5](./images/setup/Setup-Envloyment/05.png)
1. 名前を前述で作成したホストオンリーネットワークを選択する。（MACアドレスを覚えておくこと）<br />![手順6](./images/setup/Setup-Envloyment/06.png)
1. 仮想マシンを起動する。<br />![手順7](./images/setup/Setup-Envloyment/07.png)
1. 仮想マシンが起動してlogin画面よりログインする。<br />![手順8](./images/setup/Setup-Envloyment/08.png)
1. "ip a"と打ってネットワークが認識されている事を確認する。<br />![手順9](./images/setup/Setup-Envloyment/09.png)
1. "nmtui"と打ってネットワーク設定を開く。<br />![手順10](./images/setup/Setup-Envloyment/10.png)
1. ホストオンリーアダプターを選択する。（画面では文字化けしている個所）<br />![手順11](./images/setup/Setup-Envloyment/11.png)
1. <Edit...>を押下する。![手順](./images/setup/Setup-Envloyment/12.png)
1. ホストオンリーアダプターのネットワーク編集画面が表示される。<br />![手順12](./images/setup/Setup-Envloyment/13.png)
1. 画面の通り編集する項目を開く。<br />![手順13](./images/setup/Setup-Envloyment/14.png)
1. 画面のように各項目を入力して<OK>を選択する。<br />![手順14](./images/setup/Setup-Envloyment/15.png)
1. ホストオンリーアダプターのEthernetにあった文字化けが解消されている。<br />![手順15](./images/setup/Setup-Envloyment/16.png)
1. 次にNATを編集する。<br />![手順16](./images/setup/Setup-Envloyment/17-01.png)
1. Automatically connectを有効にして<OK>を押下する。<br />![手順17](./images/setup/Setup-Envloyment/17-02.png)
1. Quitで編集を終了する。<br />![手順18](./images/setup/Setup-Envloyment/17-99.png)
1. "ip a"コマンドでIPアドレスが設定されたことを確認する。（systemctl restart network.serviceでネットワークの再起動を忘れずに）<br />![手順19](./images/setup/Setup-Envloyment/18.png)
1. Tera Termを開く。<br />![手順20](./images/setup/Setup-Envloyment/19.png)
1. 先ほど設定したIPアドレスを入力してOKを押下する。<br />![手順21](./images/setup/Setup-Envloyment/20.png)
1. 警告画面が表示されるが、そのままOKを押下する。<br />![手順22](./images/setup/Setup-Envloyment/21.png)
1. root/パスワードを入力する。<br />![手順23](./images/setup/Setup-Envloyment/22.png)
1. Tera Termで接続が出来ることを確認する。<br />![手順24](./images/setup/Setup-Envloyment/23.png)