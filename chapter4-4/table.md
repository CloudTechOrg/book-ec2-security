### Systems Managerのアクセス権限を持つインスタンスプロファイルの作成
|  設定項目                    | 設定値        | 備考 | 
| ---------------------------- | ------------- | ---- | 
| 信頼されたエンティティタイプ | AWSのサービス |      | 
| ユースケース                 | EC2           |      | 

|  設定項目                    | 設定値        | 備考 | 
| ---------- | -------------------------------- | ---------------- | 
| ロール名   | cloudtech-hands-on-ec2-role      |                  | 
| 説明       | cloudtech-hands-on-ec2-role      |                  | 
| ステップ 1 | 信頼されたエンティティを選択する | デフォルトのまま | 
| ステップ 2 | 許可を追加する                   | デフォルトのまま | 
| タグを追加 | キー： Purpose、値： cloudtech   |                  | 

### EC2インスタンスの作成
|  設定項目                    | 設定値        | 備考 | 
| ---------------------------------------- | --------------------------------------------------------------- | ------------------------------------------------------------ | 
| Name                                     | dev-cloudtech-hands-on-server-01                                | 「さらにタグを追加」後、「設定項目」は「Name」に変更されます | 
| [さらにタグを追加]を選択し、[タグを追加] | キー： Purpose、値： cloudtech<br>リソースタイプ： インスタンス |                                                              | 
| Amazonマシンイメージ(AMI)                | Amazon Linux 2 AMI (HVM) - Kernel X.YY, SSD Volume Type         | X.YYはバージョンなのでずれます                               | 

|  設定項目                    | 設定値        | 備考 | 
| ------------------ | ----------------------------------- | ------------------------------------------------------------- | 
| インスタンスタイプ | t2.micro                            | 無料枠対象                                                    | 
| キーペア名         | キーペアなしで続行 (推奨されません) | Systems Managerのセッションマネージャーを利用するため不要です | 

|  設定項目                    | 設定値        | 備考 | 
| --------------------------------------- | --------------------------------------------------------------------- | ---------------------------- | 
| VPC                                     | vpc-0aa83d0f5f1f9282f (cloudtech-vpc)                                 |                              | 
| サブネット                              | subnet-0d659487fb6c7a398<br>cloudtech-subnet-private1-ap-northeast-1a | プライベートサブネットを指定 | 
| パブリック IP の自動割り当て            | 無効化                                                                | デフォルト                   | 
| ファイアウォール (セキュリティグループ) | 既存のセキュリティグループを選択する                                  |                              | 
| 共通のセキュリティグループ              | default                                                               |                              | 

|  設定項目                    | 設定値        | 備考 | 
| ---------------- | --------- | ---- | 
| ストレージを設定 | 8GiB、gp2 |      | 

|  設定項目                    | 設定値        | 備考 | 
| ---------------------------- | --------------------------- | ---- | 
| IAM インスタンスプロフィール | cloudtech-hands-on-ec2-role |      | 




