## Step Functionsのステートマシン用のIAMロール作成
### cloudtech-hands-on-stepfunctions-role
|  |  |  |
| - | - | - |
|  設定項目 | 設定値 | 備考 |
| ロール名 | cloudtech-hands-on-stepfunctions-role |  |
| 許可1<br>AWS管理のポリシー | CloudWatchLogsFullAccess |  |
| 許可2<br>インラインポリシー | 名前：stepfunctions-policy<br>JSON：(後続のJSON参照) |  |
| 信頼関係 | JSON：(後続のJSON参照) |  |
| タグ | キー： Purpose、値： cloudtech |  |

### cloudtech-hands-on-runcommand-role
|  |  |  |
| - | - | - |
|  設定項目 | 設定値 | 備考 |
| ロール名 | cloudtech-hands-on-runcommand-role |  |
| 許可1<br>インラインポリシー | 名前：runcommand-policy<br>JSON：(後続のJSON参照) |  |
| 信頼関係 | JSON：(後続のJSON参照) |  |
| タグ | キー： Purpose、値： cloudtech |  |

### cloudtech-hands-on-backup-role
|  |  |  |
| - | - | - |
|  設定項目 | 設定値 | 備考 |
| ロール名 | cloudtech-hands-on-backup-role |  |
| 許可1<br>AWS管理のポリシー | AWSBackupServiceRolePolicyForBackup |  |
| 信頼関係 | JSON：(後続のJSON参照) |  |
| タグ | キー： Purpose、値： cloudtech |  |

