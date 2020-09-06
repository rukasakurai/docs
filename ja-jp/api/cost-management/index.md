# APIでAzureのコストを取得する方法

## 公式ドキュメント
APIでAzureのコストを取得する手法の公式ドキュメントは[こちら](https://docs.microsoft.com/ja-jp/rest/api/cost-management/query/usage)になります

## PostmanでのQuery例
### 1. ツールの用意
- POSTをする手段としての[Postman](https://www.postman.com/)

### 2. Bearトークンの取得
PostmanからQueryする際にAPIの認証にはBearerトークンを使うことができます。
以下のように取得することができます
1. ブラウザのDeveloper toolsのNetworkタブを開く
2. https://portal.azure.com にログイン
3. Azureの何かしらのAPIの呼び出しを開く（例: https://management.azure.com/batch?api-version=xx）
4. Header>Request Headers>authorizationの「Bearer xxxx」をコピー

### 3. POSTの構築
#### URL
```https://management.azure.com/subscriptions/{subscription id}/resourceGroups/{resource group}/providers/Microsoft.CostManagement/query/?api-version=2019-11-01```
#### Headers
|Key|Value|
|---|---|
|Authorization|Bearer {Bearer Token}|