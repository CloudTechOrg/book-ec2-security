## Step Functionsのステートマシン作成
### CloudWatch ロググループ
|  設定項目 | 設定値 | 備考 |
| - | - | - |
| ロググループ名 | /cloudtech/handson/ec2-vulnerability |  |
| 保持期間の設定 | 1日 | ハンズオンなので不要なログが残らないようにします |
| タグ | 新しいタグを追加<br>キー： Purpose、値： cloudtech |  |

### ステートマシン
|  設定項目 | 設定値 | 備考 |
| - | - | - |
| ステートマシン名 | cloudtech-hands-on-statemachine |  |
| 実行ロール | 既存のロールを選択する |  |
| 既存のロール | cloudtech-hands-on-stepfunctions-role |  |
| ログレベル<br> | ERROR |  |
| 実行データを含める | ✅ |  |
| CloudWatch ロググループ | 既存のロググループを選択<br>/cloudtech/handson/ec2-vulnerability |  |
| タグ | タグの追加<br>キー： Purpose、値： cloudtech |  |

