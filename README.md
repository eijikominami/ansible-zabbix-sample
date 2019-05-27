# 概要
社内勉強会 fukushima.dev#9 Zabbixサーバハンズオン資料。
Ansibleを用いてローカルホストに**Zabbixサーバ**を構築します。

## Deployment

構築方法は以下の通り。

+ gitをインストールする

```bash
yum install -y git
```


+ プロジェクトをダウンロードする

```bash
git clone --recursive https://github.com/eijikominami/ansible-zabbix-sample.git
```

+ `Epel`リポジトリを追加する

  + Amazon Linux 2の場合
  
```bash
sudo amazon-linux-extras install -y epel
```

+ ansibleをインストールする

```bash
yum install -y ansible
```

+ ディレクトリを移動する

```bash
cd ansible-zabbix-sample/zabbix_sample
```

+ Ansibleプレイブックを実行する

```bash
sudo ansible-playbook site.yml 
```

+ ブラウザから`http://IP_ADDRESS/zabbix`にアクセスして初期設定を行う
+ OSを再起動する