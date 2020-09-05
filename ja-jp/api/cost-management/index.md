# APIでAzureのコストを取得する方法

## 公式ドキュメント
APIでAzureのコストを取得する手法の公式ドキュメントは[こちら](https://docs.microsoft.com/ja-jp/rest/api/cost-management/query/usage)になります

## PostmanでのQuery例
### 1. ツールの用意
- POSTをする手段としての[Postman](https://www.postman.com/)

### 2. POSTに必要な値の取得
#### Subscription ID
#### Resource Group名
#### Bearトークン

### 3. POSTの構築
#### URL
```
https://management.azure.com/subscriptions/{subscription id}/resourceGroups/{resource group}/providers/Microsoft.CostManagement/query/?api-version=2019-11-01
```
#### Headers
|Key|Value|
|---|---|
|Authorization|Bearer {Bearer Token}|