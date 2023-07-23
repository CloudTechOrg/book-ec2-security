## EventBridge Schedulerによる定期実行設定
### EventBridge Schedulerを実行するためのIAMロール
|  設定項目                    | 設定値        | 備考 | 
| ---------------------------- | ------------- | ---- | 
| 信頼されたエンティティタイプ | カスタム信頼ポリシー |      | 
| カスタム信頼ポリシー          | JSON：(後続のJSON参照)       |      | 

|  設定項目                    | 設定値        | 備考 | 
| ---------- | -------------------------------- | ---------------- | 
| ロール名   | cloudtech-hands-on-scheduler-role      |                  | 
| 説明       | cloudtech-hands-on-scheduler-role      |                  | 
| ステップ 1 | 信頼されたエンティティを選択する | デフォルトのまま | 
| ステップ 2 | 許可を追加する                   | デフォルトのまま | 
| タグを追加 | キー： Purpose、値： cloudtech   |                  | 

| 設定項目 | 設定値 | 備考 |
| - | - | - |
| ポリシー名 | scheduler-policy |  |

### EventBridge Scheduler cloudtech-hands-on-schedule-prd
|  設定項目 | 設定値 | 備考 |
| - | - | - |
| スケジュール名 | cloudtech-hands-on-schedule-prd |  |
| 頻度 | 1回限りのスケジュール |  |
| 日付と時刻 | (この設定を行おうとしている時間から10分後ぐらい) | 都合の良いタイミングでOKです |
| フレックスタイムウィンドウ | オフ |  |

|  設定項目 | 設定値 | 備考 |
| - | - | - |
| ターゲットAPI | テンプレート化されたターゲット |  |
| AWS Step Functions StartExecution | ✅ |  |
| ステートマシン | cloudtech-handson-statemachine |  |
| 入力 | (後続のJSON参照) | インスタンスIDには、prd-cloudtech-hands-on-server-01のインスタンスのIDを入れてください |

|  設定項目 | 設定値 | 備考 |
| - | - | - |
| スケジュールを有効化 | 有効化 |  |
| 再試行ポリシー | 無効化 |  |
| デッドレターキュー(DLQ) | なし |  |
| 既存のロールを使用 | ✅ |  |
| 既存の役割を選択 | cloudtech-hands-on-scheduler-role |  |
