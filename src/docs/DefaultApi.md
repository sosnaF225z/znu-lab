# DefaultApi

All URIs are relative to *https://api.taskmanager.com/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createProject**](DefaultApi.md#createProject) | **POST** /projects | Create a new project |
| [**createTask**](DefaultApi.md#createTask) | **POST** /projects/{projectId}/tasks | Add a task to a project |
| [**getProjectTasks**](DefaultApi.md#getProjectTasks) | **GET** /projects/{projectId}/tasks | Get tasks for a specific project |
| [**getProjects**](DefaultApi.md#getProjects) | **GET** /projects | List all projects |


<a id="createProject"></a>
# **createProject**
> createProject(projectInput)

Create a new project

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.taskmanager.com/v1");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    ProjectInput projectInput = new ProjectInput(); // ProjectInput | 
    try {
      apiInstance.createProject(projectInput);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createProject");
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
| **projectInput** | [**ProjectInput**](ProjectInput.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Project successfully created |  -  |

<a id="createTask"></a>
# **createTask**
> createTask(projectId, taskInput)

Add a task to a project

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.taskmanager.com/v1");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    UUID projectId = UUID.randomUUID(); // UUID | 
    TaskInput taskInput = new TaskInput(); // TaskInput | 
    try {
      apiInstance.createTask(projectId, taskInput);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createTask");
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
| **projectId** | **UUID**|  | |
| **taskInput** | [**TaskInput**](TaskInput.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Task successfully created |  -  |

<a id="getProjectTasks"></a>
# **getProjectTasks**
> List&lt;Task&gt; getProjectTasks(projectId)

Get tasks for a specific project

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.taskmanager.com/v1");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    UUID projectId = UUID.randomUUID(); // UUID | 
    try {
      List<Task> result = apiInstance.getProjectTasks(projectId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getProjectTasks");
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
| **projectId** | **UUID**|  | |

### Return type

[**List&lt;Task&gt;**](Task.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of tasks associated with the project |  -  |

<a id="getProjects"></a>
# **getProjects**
> List&lt;Project&gt; getProjects()

List all projects

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.taskmanager.com/v1");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    try {
      List<Project> result = apiInstance.getProjects();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getProjects");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List&lt;Project&gt;**](Project.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of projects |  -  |

