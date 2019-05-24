# 概要
社内勉強会 fukushima.dev#9 Zabbixサーバハンズオン資料。
Ansibleを用いてローカルホストに**Zabbixサーバ**を構築します。

## Deployment

構築方法は以下の通り。

+ プロジェクトをダウンロードする

```bash
git clone https://github.com/eijikominami/ansible-zabbix-sample.git
```

+ `Epel`リポジトリを追加する

  + Amazon Linux 2の場合
  
```bash
sudo amazon-linux-extras install -y epel
```

+ Ansibleプレイブックを実行する

```bash
sudo ansible-playbook site.yml 
```

+ ブラウザから`http://IP_ADDRESS/zabbix`にアクセスして初期設定を行う
+ OSを再起動する