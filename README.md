# azure-marketplace-client-java

SaaS fulfillment APIs, version 2
- API version: 1.0.0
  - Build date: 2020-04-19T20:04:00.284-07:00[America/Los_Angeles]

This spec details the APIs that enable partners to sell their SaaS applications in the AppSource marketplace and the Azure Marketplace. These APIs are a requirement for transactable SaaS offers on the AppSource and Azure Marketplace.


*Automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen)*


## Requirements

Building the API client library requires:
1. Java 1.7+
2. Maven/Gradle

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>com.microsoft.azure.marketplace</groupId>
  <artifactId>azure-marketplace-client-java</artifactId>
  <version>0.1.0</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "com.microsoft.azure.marketplace:azure-marketplace-client-java:0.1.0"
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

* `target/azure-marketplace-client-java-0.1.0.jar`
* `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.auth.*;
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.generated.SaasFulfillmentApi;

import java.io.File;
import java.util.*;

public class SaasFulfillmentApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();

        // Configure OAuth2 access token for authorization: OAuth2
        OAuth OAuth2 = (OAuth) defaultClient.getAuthentication("OAuth2");
        OAuth2.setAccessToken("YOUR ACCESS TOKEN");

        SaasFulfillmentApi apiInstance = new SaasFulfillmentApi();
        SubscriberPlan body = new SubscriberPlan(); // SubscriberPlan | 
        UUID subscriptionId = new UUID(); // UUID | 
        ApiVersion apiVersion = new ApiVersion(); // ApiVersion | Version of the API.
        String contentType = "contentType_example"; // String | application/json
        UUID xMsRequestid = new UUID(); // UUID | A unique string value for tracking the request from the client, preferably a GUID. If this value isn't provided, one will be generated and provided in the response headers.
        UUID xMsCorrelationid = new UUID(); // UUID | A unique string value for operation on the client. This parameter correlates all events from client operation with events on the server side. If this value isn't provided, one will be generated and provided in the response headers.
        try {
            apiInstance.activateSubscription(body, subscriptionId, apiVersion, contentType, xMsRequestid, xMsCorrelationid);
        } catch (ApiException e) {
            System.err.println("Exception when calling SaasFulfillmentApi#activateSubscription");
            e.printStackTrace();
        }
    }
}
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.auth.*;
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.generated.SaasFulfillmentApi;

import java.io.File;
import java.util.*;

public class SaasFulfillmentApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();

        // Configure OAuth2 access token for authorization: OAuth2
        OAuth OAuth2 = (OAuth) defaultClient.getAuthentication("OAuth2");
        OAuth2.setAccessToken("YOUR ACCESS TOKEN");

        SaasFulfillmentApi apiInstance = new SaasFulfillmentApi();
        UUID subscriptionId = new UUID(); // UUID | 
        ApiVersion apiVersion = new ApiVersion(); // ApiVersion | Version of the API.
        String contentType = "contentType_example"; // String | application/json
        UUID xMsRequestid = new UUID(); // UUID | A unique string value for tracking the request from the client, preferably a GUID. If this value isn't provided, one will be generated and provided in the response headers.
        UUID xMsCorrelationid = new UUID(); // UUID | A unique string value for operation on the client. This parameter correlates all events from client operation with events on the server side. If this value isn't provided, one will be generated and provided in the response headers.
        try {
            apiInstance.deleteSubscription(subscriptionId, apiVersion, contentType, xMsRequestid, xMsCorrelationid);
        } catch (ApiException e) {
            System.err.println("Exception when calling SaasFulfillmentApi#deleteSubscription");
            e.printStackTrace();
        }
    }
}
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.auth.*;
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.generated.SaasFulfillmentApi;

import java.io.File;
import java.util.*;

public class SaasFulfillmentApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();

        // Configure OAuth2 access token for authorization: OAuth2
        OAuth OAuth2 = (OAuth) defaultClient.getAuthentication("OAuth2");
        OAuth2.setAccessToken("YOUR ACCESS TOKEN");

        SaasFulfillmentApi apiInstance = new SaasFulfillmentApi();
        UUID subscriptionId = new UUID(); // UUID | 
        UUID operationId = new UUID(); // UUID | 
        ApiVersion apiVersion = new ApiVersion(); // ApiVersion | Version of the API.
        String contentType = "contentType_example"; // String | application/json
        UUID xMsRequestid = new UUID(); // UUID | A unique string value for tracking the request from the client, preferably a GUID. If this value isn't provided, one will be generated and provided in the response headers.
        UUID xMsCorrelationid = new UUID(); // UUID | A unique string value for operation on the client. This parameter correlates all events from client operation with events on the server side. If this value isn't provided, one will be generated and provided in the response headers.
        try {
            OperationType result = apiInstance.getOperationStatus(subscriptionId, operationId, apiVersion, contentType, xMsRequestid, xMsCorrelationid);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SaasFulfillmentApi#getOperationStatus");
            e.printStackTrace();
        }
    }
}
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.auth.*;
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.generated.SaasFulfillmentApi;

import java.io.File;
import java.util.*;

public class SaasFulfillmentApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();

        // Configure OAuth2 access token for authorization: OAuth2
        OAuth OAuth2 = (OAuth) defaultClient.getAuthentication("OAuth2");
        OAuth2.setAccessToken("YOUR ACCESS TOKEN");

        SaasFulfillmentApi apiInstance = new SaasFulfillmentApi();
        UUID subscriptionId = new UUID(); // UUID | 
        ApiVersion apiVersion = new ApiVersion(); // ApiVersion | Version of the API.
        String contentType = "contentType_example"; // String | application/json
        UUID xMsRequestid = new UUID(); // UUID | A unique string value for tracking the request from the client, preferably a GUID. If this value isn't provided, one will be generated and provided in the response headers.
        UUID xMsCorrelationid = new UUID(); // UUID | A unique string value for operation on the client. This parameter correlates all events from client operation with events on the server side. If this value isn't provided, one will be generated and provided in the response headers.
        try {
            Subscription result = apiInstance.getSubscription(subscriptionId, apiVersion, contentType, xMsRequestid, xMsCorrelationid);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SaasFulfillmentApi#getSubscription");
            e.printStackTrace();
        }
    }
}
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.auth.*;
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.generated.SaasFulfillmentApi;

import java.io.File;
import java.util.*;

public class SaasFulfillmentApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();

        // Configure OAuth2 access token for authorization: OAuth2
        OAuth OAuth2 = (OAuth) defaultClient.getAuthentication("OAuth2");
        OAuth2.setAccessToken("YOUR ACCESS TOKEN");

        SaasFulfillmentApi apiInstance = new SaasFulfillmentApi();
        UUID subscriptionId = new UUID(); // UUID | 
        ApiVersion apiVersion = new ApiVersion(); // ApiVersion | Version of the API.
        String contentType = "contentType_example"; // String | application/json
        UUID xMsRequestid = new UUID(); // UUID | A unique string value for tracking the request from the client, preferably a GUID. If this value isn't provided, one will be generated and provided in the response headers.
        UUID xMsCorrelationid = new UUID(); // UUID | A unique string value for operation on the client. This parameter correlates all events from client operation with events on the server side. If this value isn't provided, one will be generated and provided in the response headers.
        try {
            PlansResponse result = apiInstance.listAvailablePlans(subscriptionId, apiVersion, contentType, xMsRequestid, xMsCorrelationid);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SaasFulfillmentApi#listAvailablePlans");
            e.printStackTrace();
        }
    }
}
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.auth.*;
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.generated.SaasFulfillmentApi;

import java.io.File;
import java.util.*;

public class SaasFulfillmentApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();

        // Configure OAuth2 access token for authorization: OAuth2
        OAuth OAuth2 = (OAuth) defaultClient.getAuthentication("OAuth2");
        OAuth2.setAccessToken("YOUR ACCESS TOKEN");

        SaasFulfillmentApi apiInstance = new SaasFulfillmentApi();
        UUID subscriptionId = new UUID(); // UUID | 
        ApiVersion apiVersion = new ApiVersion(); // ApiVersion | Version of the API.
        String contentType = "contentType_example"; // String | application/json
        UUID xMsRequestid = new UUID(); // UUID | A unique string value for tracking the request from the client, preferably a GUID. If this value isn't provided, one will be generated and provided in the response headers.
        UUID xMsCorrelationid = new UUID(); // UUID | A unique string value for operation on the client. This parameter correlates all events from client operation with events on the server side. If this value isn't provided, one will be generated and provided in the response headers.
        try {
            OperationList result = apiInstance.listOperations(subscriptionId, apiVersion, contentType, xMsRequestid, xMsCorrelationid);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SaasFulfillmentApi#listOperations");
            e.printStackTrace();
        }
    }
}
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.auth.*;
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.generated.SaasFulfillmentApi;

import java.io.File;
import java.util.*;

public class SaasFulfillmentApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();

        // Configure OAuth2 access token for authorization: OAuth2
        OAuth OAuth2 = (OAuth) defaultClient.getAuthentication("OAuth2");
        OAuth2.setAccessToken("YOUR ACCESS TOKEN");

        SaasFulfillmentApi apiInstance = new SaasFulfillmentApi();
        ApiVersion apiVersion = new ApiVersion(); // ApiVersion | Version of the API.
        String contentType = "contentType_example"; // String | application/json
        String continuationToken = "continuationToken_example"; // String | Optional value, only used for ListSubscriptions.
        UUID xMsRequestid = new UUID(); // UUID | A unique string value for tracking the request from the client, preferably a GUID. If this value isn't provided, one will be generated and provided in the response headers.
        UUID xMsCorrelationid = new UUID(); // UUID | A unique string value for operation on the client. This parameter correlates all events from client operation with events on the server side. If this value isn't provided, one will be generated and provided in the response headers.
        try {
            SubscriptionsResponse result = apiInstance.listSubscriptions(apiVersion, contentType, continuationToken, xMsRequestid, xMsCorrelationid);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SaasFulfillmentApi#listSubscriptions");
            e.printStackTrace();
        }
    }
}
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.auth.*;
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.generated.SaasFulfillmentApi;

import java.io.File;
import java.util.*;

public class SaasFulfillmentApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();

        // Configure OAuth2 access token for authorization: OAuth2
        OAuth OAuth2 = (OAuth) defaultClient.getAuthentication("OAuth2");
        OAuth2.setAccessToken("YOUR ACCESS TOKEN");

        SaasFulfillmentApi apiInstance = new SaasFulfillmentApi();
        SubscriberPlan body = new SubscriberPlan(); // SubscriberPlan | 
        UUID subscriptionId = new UUID(); // UUID | 
        ApiVersion apiVersion = new ApiVersion(); // ApiVersion | Version of the API.
        String contentType = "contentType_example"; // String | application/json
        UUID xMsRequestid = new UUID(); // UUID | A unique string value for tracking the request from the client, preferably a GUID. If this value isn't provided, one will be generated and provided in the response headers.
        UUID xMsCorrelationid = new UUID(); // UUID | A unique string value for operation on the client. This parameter correlates all events from client operation with events on the server side. If this value isn't provided, one will be generated and provided in the response headers.
        try {
            apiInstance.patchSubscription(body, subscriptionId, apiVersion, contentType, xMsRequestid, xMsCorrelationid);
        } catch (ApiException e) {
            System.err.println("Exception when calling SaasFulfillmentApi#patchSubscription");
            e.printStackTrace();
        }
    }
}
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.auth.*;
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.generated.SaasFulfillmentApi;

import java.io.File;
import java.util.*;

public class SaasFulfillmentApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();

        // Configure OAuth2 access token for authorization: OAuth2
        OAuth OAuth2 = (OAuth) defaultClient.getAuthentication("OAuth2");
        OAuth2.setAccessToken("YOUR ACCESS TOKEN");

        SaasFulfillmentApi apiInstance = new SaasFulfillmentApi();
        ApiVersion apiVersion = new ApiVersion(); // ApiVersion | Version of the API.
        String contentType = "contentType_example"; // String | application/json
        String xMsMarketplaceToken = "xMsMarketplaceToken_example"; // String | The token query parameter in the URL when the user is redirected to the SaaS partner's website from Azure (for example,  https://contoso.com/signup?token=..). Note, The URL decodes the token value from the browser before using it.
        UUID xMsRequestid = new UUID(); // UUID | A unique string value for tracking the request from the client, preferably a GUID. If this value isn't provided, one will be generated and provided in the response headers.
        UUID xMsCorrelationid = new UUID(); // UUID | A unique string value for operation on the client. This parameter correlates all events from client operation with events on the server side. If this value isn't provided, one will be generated and provided in the response headers.
        try {
            SubscriptionSummary result = apiInstance.resolve(apiVersion, contentType, xMsMarketplaceToken, xMsRequestid, xMsCorrelationid);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SaasFulfillmentApi#resolve");
            e.printStackTrace();
        }
    }
}
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.auth.*;
import com.microsoft.azure.marketplace.*;
import com.microsoft.azure.marketplace.generated.SaasFulfillmentApi;

import java.io.File;
import java.util.*;

public class SaasFulfillmentApiExample {

    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();

        // Configure OAuth2 access token for authorization: OAuth2
        OAuth OAuth2 = (OAuth) defaultClient.getAuthentication("OAuth2");
        OAuth2.setAccessToken("YOUR ACCESS TOKEN");

        SaasFulfillmentApi apiInstance = new SaasFulfillmentApi();
        UpdateOperation body = new UpdateOperation(); // UpdateOperation | 
        UUID subscriptionId = new UUID(); // UUID | 
        UUID operationId = new UUID(); // UUID | 
        ApiVersion apiVersion = new ApiVersion(); // ApiVersion | Version of the API.
        String contentType = "contentType_example"; // String | application/json
        UUID xMsRequestid = new UUID(); // UUID | A unique string value for tracking the request from the client, preferably a GUID. If this value isn't provided, one will be generated and provided in the response headers.
        UUID xMsCorrelationid = new UUID(); // UUID | A unique string value for operation on the client. This parameter correlates all events from client operation with events on the server side. If this value isn't provided, one will be generated and provided in the response headers.
        try {
            apiInstance.updateOperationStatus(body, subscriptionId, operationId, apiVersion, contentType, xMsRequestid, xMsCorrelationid);
        } catch (ApiException e) {
            System.err.println("Exception when calling SaasFulfillmentApi#updateOperationStatus");
            e.printStackTrace();
        }
    }
}
```

## Documentation for API Endpoints

All URIs are relative to *https://marketplaceapi.microsoft.com/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*SaasFulfillmentApi* | [**activateSubscription**](docs/SaasFulfillmentApi.md#activateSubscription) | **POST** /saas/subscriptions/{subscriptionId}/activate | Activate a subscription
*SaasFulfillmentApi* | [**deleteSubscription**](docs/SaasFulfillmentApi.md#deleteSubscription) | **DELETE** /saas/subscriptions/{subscriptionId} | Delete a subscription
*SaasFulfillmentApi* | [**getOperationStatus**](docs/SaasFulfillmentApi.md#getOperationStatus) | **GET** /saas/subscriptions/{subscriptionId}/operations/{operationId} | Get operation status
*SaasFulfillmentApi* | [**getSubscription**](docs/SaasFulfillmentApi.md#getSubscription) | **GET** /saas/subscriptions/{subscriptionId} | Get subscription
*SaasFulfillmentApi* | [**listAvailablePlans**](docs/SaasFulfillmentApi.md#listAvailablePlans) | **GET** /saas/subscriptions/{subscriptionId}/listAvailablePlans | List available plans
*SaasFulfillmentApi* | [**listOperations**](docs/SaasFulfillmentApi.md#listOperations) | **GET** /saas/subscriptions/{subscriptionId}/operations | List outstanding operations
*SaasFulfillmentApi* | [**listSubscriptions**](docs/SaasFulfillmentApi.md#listSubscriptions) | **GET** /saas/subscriptions/ | List subscriptions
*SaasFulfillmentApi* | [**patchSubscription**](docs/SaasFulfillmentApi.md#patchSubscription) | **PATCH** /saas/subscriptions/{subscriptionId} | Patch a subscription
*SaasFulfillmentApi* | [**resolve**](docs/SaasFulfillmentApi.md#resolve) | **POST** /saas/subscriptions/resolve | Resolve a subscription
*SaasFulfillmentApi* | [**updateOperationStatus**](docs/SaasFulfillmentApi.md#updateOperationStatus) | **PATCH** /saas/subscriptions/{subscriptionId}/operations/{operationId} | Update the status of an operation
*SaasMarketplaceMeterApi* | [**postBatchUsageEvent**](docs/SaasMarketplaceMeterApi.md#postBatchUsageEvent) | **POST** /batchUsageEvent | Posts a set of usage events to the marketplace metering service API.
*SaasMarketplaceMeterApi* | [**postUsageEvent**](docs/SaasMarketplaceMeterApi.md#postUsageEvent) | **POST** /usageEvent | Posts a single usage event to the marketplace metering service API.

## Documentation for Models

 - [AadIdentifier](docs/AadIdentifier.md)
 - [ApiVersion](docs/ApiVersion.md)
 - [BatchUsageEvent](docs/BatchUsageEvent.md)
 - [Error](docs/Error.md)
 - [ErrorDetail](docs/ErrorDetail.md)
 - [ErrorDetailError](docs/ErrorDetailError.md)
 - [ErrorError](docs/ErrorError.md)
 - [ErrorErrorAdditionalInfo](docs/ErrorErrorAdditionalInfo.md)
 - [OperationList](docs/OperationList.md)
 - [OperationType](docs/OperationType.md)
 - [Plan](docs/Plan.md)
 - [PlansResponse](docs/PlansResponse.md)
 - [SubscriberPlan](docs/SubscriberPlan.md)
 - [Subscription](docs/Subscription.md)
 - [SubscriptionSummary](docs/SubscriptionSummary.md)
 - [SubscriptionTerm](docs/SubscriptionTerm.md)
 - [SubscriptionsResponse](docs/SubscriptionsResponse.md)
 - [UpdateOperation](docs/UpdateOperation.md)
 - [UsageEvent](docs/UsageEvent.md)
 - [UsageEventOkResponse](docs/UsageEventOkResponse.md)

## Documentation for Authorization

Authentication schemes defined for the API:
### OAuth2

- **Type**: OAuth
- **Flow**: application
- **Authorization URL**: 
- **Scopes**: 
  - : 


## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author


