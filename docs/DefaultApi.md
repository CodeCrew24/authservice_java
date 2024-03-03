# DefaultApi

All URIs are relative to *http://localhost:3000/auth*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**clientGet**](DefaultApi.md#clientGet) | **GET** /client | Get client ID and secret |
| [**loginClientPost**](DefaultApi.md#loginClientPost) | **POST** /login/client | Logs in a user using client ID and secret |
| [**regenerateClientCredentialsPost**](DefaultApi.md#regenerateClientCredentialsPost) | **POST** /regenerate-client-credentials | Regenerate client credentials |
| [**registerPost**](DefaultApi.md#registerPost) | **POST** /register | Registers a new user |


<a id="clientGet"></a>
# **clientGet**
> ClientGet200Response clientGet(username, password)

Get client ID and secret

Returns the client ID and client secret of the user associated with the provided username and password.

### Example
```java
// Import classes:
import authservice.client.ApiClient;
import authservice.client.ApiException;
import authservice.client.Configuration;
import authservice.client.models.*;
import authservice.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000/auth");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String username = "johndoe"; // String | User's username
    String password = "password123"; // String | User's password
    try {
      ClientGet200Response result = apiInstance.clientGet(username, password);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#clientGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **username** | **String**| User&#39;s username | |
| **password** | **String**| User&#39;s password | |

### Return type

[**ClientGet200Response**](ClientGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Client ID and client secret retrieved successfully |  -  |
| **401** | Unauthorized (invalid credentials) |  -  |
| **500** | Internal server error |  -  |

<a id="loginClientPost"></a>
# **loginClientPost**
> LoginClientPost200Response loginClientPost(clientId, clientSecret)

Logs in a user using client ID and secret

Authenticates a user with the provided client ID and secret. Returns a JWT token, token type (Bearer), and expiry time in seconds.

### Example
```java
// Import classes:
import authservice.client.ApiClient;
import authservice.client.ApiException;
import authservice.client.Configuration;
import authservice.client.models.*;
import authservice.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000/auth");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String clientId = "abc123-xyz456"; // String | User's client ID
    String clientSecret = "def789-ghi012"; // String | User's client secret
    try {
      LoginClientPost200Response result = apiInstance.loginClientPost(clientId, clientSecret);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#loginClientPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **clientId** | **String**| User&#39;s client ID | |
| **clientSecret** | **String**| User&#39;s client secret | |

### Return type

[**LoginClientPost200Response**](LoginClientPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Login successful |  -  |
| **401** | Unauthorized (invalid client credentials) |  -  |
| **500** | Internal server error |  -  |

<a id="regenerateClientCredentialsPost"></a>
# **regenerateClientCredentialsPost**
> RegenerateClientCredentialsPost200Response regenerateClientCredentialsPost(username, password)

Regenerate client credentials

Regenerates the client ID and client secret of the user associated with the provided username and password. Returns the new client ID and client secret in the response.

### Example
```java
// Import classes:
import authservice.client.ApiClient;
import authservice.client.ApiException;
import authservice.client.Configuration;
import authservice.client.models.*;
import authservice.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000/auth");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String username = "johndoe"; // String | User's username
    String password = "password123"; // String | User's password
    try {
      RegenerateClientCredentialsPost200Response result = apiInstance.regenerateClientCredentialsPost(username, password);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#regenerateClientCredentialsPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **username** | **String**| User&#39;s username | |
| **password** | **String**| User&#39;s password | |

### Return type

[**RegenerateClientCredentialsPost200Response**](RegenerateClientCredentialsPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Client credentials regenerated successfully |  -  |
| **401** | Unauthorized (invalid credentials) |  -  |
| **500** | Internal server error |  -  |

<a id="registerPost"></a>
# **registerPost**
> RegisterPost201Response registerPost(username, password, role)

Registers a new user

Creates a new user with the provided username, password, and role. Returns the generated client ID and client secret in the response.

### Example
```java
// Import classes:
import authservice.client.ApiClient;
import authservice.client.ApiException;
import authservice.client.Configuration;
import authservice.client.models.*;
import authservice.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:3000/auth");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String username = "johndoe"; // String | Unique username for the user
    String password = "password123"; // String | User's password
    String role = "user"; // String | 
    try {
      RegisterPost201Response result = apiInstance.registerPost(username, password, role);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#registerPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **username** | **String**| Unique username for the user | |
| **password** | **String**| User&#39;s password | |
| **role** | **String**|  | [default to user] [enum: user, admin, moderator, guest, superadmin] |

### Return type

[**RegisterPost201Response**](RegisterPost201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | User registered successfully |  -  |
| **400** | Bad request (e.g., username already taken) |  -  |
| **500** | Internal server error |  -  |

