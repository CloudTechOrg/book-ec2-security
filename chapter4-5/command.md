### セッションマネージャーでEC2インスタンスにアクセス
```
$ sudo su -
```

### 脆弱性の存在する古いパッケージをインストール
```
# yum --showduplicates list | grep httpd.x86_64
# rpm -qa | grep httpd
# systemctl enable httpd.service
# systemctl start httpd.service
# systemctl status httpd.service
```
