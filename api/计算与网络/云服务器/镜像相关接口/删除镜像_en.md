## 1. API Description
 

This API (DeleteImages) is used to delete one or more images.

Domain name for API request: <font style="color:red">image.api.qcloud.com</font>


* Any image with a status of "Creating..." or "In Use" cannot be deleted.
* A maximum of 10 custom images are allowed to be created for each region. Deletion of images can free the quota on account.


## 2. Input Parameters

The following list only provides API request parameters. For additional parameters, refer to [Public Request Parameters](/document/api/213/6976) page.

| Parameter Name | Required | Type | Description |
|---------|---------|---------|---------|
| imageIds.n | Yes | String | Image ID, which can be obtained from unImgId in the returned field of [DescribeImages](http://www.qcloud.com/doc/api/229/%E6%9F%A5%E8%AF%A2%E5%8F%AF%E7%94%A8%E7%9A%84%E9%95%9C%E5%83%8F%E5%88%97%E8%A1%A8) API (This API allows passing multiple IDs at a time). For the format of this parameter, refer to `id.n` section of API [Introduction](https://www.qcloud.com/doc/api/229/568)).


## 3. Output Parameters

| Parameter Name | Type | Description |
|---------|---------|---------|
| code | Int | Common error code. A value of 0 indicates success, and other values indicate failure. For more information, refer to [Common Error Codes](https://www.qcloud.com/doc/api/372/%E9%94%99%E8%AF%AF%E7%A0%81#1.E3.80.81.E5.85.AC.E5.85.B1.E9.94.99.E8.AF.AF.E7.A0.81) on Error Code page. |
| message | String | Module error message description depending on API. For more information, refer to [Module Error Codes](https://www.qcloud.com/doc/api/372/%E9%94%99%E8%AF%AF%E7%A0%81#2.E3.80.81.E6.A8.A1.E5.9D.97.E9.94.99.E8.AF.AF.E7.A0.81) on Error Code page. |
 
 

## 4. Example
 
Input
<pre>
  https://cvm.api.qcloud.com/v2/index.php?Action=DeleteImages
  &imageIds.0=img-xxxxxxxx
  &imageIds.1=img-xxxxxxxx
  &<<a href="https://www.qcloud.com/doc/api/229/6976">Public request parameters</a>>
</pre>

Output
Refer to [Format of Returned Results of Batch Asynchronous Task API](http://www.qcloud.com/doc/api/229/%E5%BC%82%E6%AD%A5%E4%BB%BB%E5%8A%A1%E6%8E%A5%E5%8F%A3%E8%BF%94%E5%9B%9E%E6%A0%BC%E5%BC%8F#2.-批量异步任务接口返回格式)





