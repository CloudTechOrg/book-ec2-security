### セッションマネージャーでEC2インスタンスにアクセス
```
$ sudo su -
```

### 脆弱性の存在する古いパッケージをインストール
```
# yum --showduplicates list | grep httpd.x86_64
# yum install httpd-2.4.33-2.amzn2.0.2
# rpm -qa | grep httpd
# systemctl enable httpd.service
# systemctl start httpd.service
# systemctl status httpd.service
```
