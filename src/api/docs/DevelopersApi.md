# SimpleDeveloperApi.DevelopersApi

All URIs are relative to *http://127.0.0.1:4010*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addInventory**](DevelopersApi.md#addInventory) | **POST** /developers | Add new Developer
[**searchInventory**](DevelopersApi.md#searchInventory) | **GET** /developers | searches all developers



## addInventory

> addInventory(opts)

Add new Developer

새로운 개발자를 추가합니다

### Example

```javascript
import SimpleDeveloperApi from 'simple_developer_api';

let apiInstance = new SimpleDeveloperApi.DevelopersApi();
let opts = {
  'developer': [{"id":2,"name":"최범수","age":26,"position":"frontend","major":"컴퓨터공학"}] // Developer | Inventory item to add
};
apiInstance.addInventory(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **developer** | [**Developer**](Developer.md)| Inventory item to add | [optional] 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## searchInventory

> [Developer] searchInventory()

searches all developers

모든 개발자들을 조회합니다 

### Example

```javascript
import SimpleDeveloperApi from 'simple_developer_api';

let apiInstance = new SimpleDeveloperApi.DevelopersApi();
apiInstance.searchInventory((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**[Developer]**](Developer.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

