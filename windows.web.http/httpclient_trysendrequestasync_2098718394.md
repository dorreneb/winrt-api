---
-api-id: M:Windows.Web.Http.HttpClient.TrySendRequestAsync(Windows.Web.Http.HttpRequestMessage)
-api-type: winrt method
ms.custom: 19H1
---

<!-- Method syntax.
public IAsyncOperationWithProgress<HttpProgress> HttpClient.TrySendRequestAsync(HttpRequestMessage request)
-->

# Windows.Web.Http.HttpClient.TrySendRequestAsync

## -description
Sends an HTTP request to the specified [Uri](../windows.foundation/uri.md) as an asynchronous operation.

## -parameters
### -param request
The HTTP request message to send.

## -returns
The object representing the asynchronous operation.

## -remarks
This operation will not throw an exception on network errors. Instead you should examine the [HttpRequestResult](httprequestresult.md) to learn about the original HTTP request, the resulting HTTP response (if any) and error (if any). This operation will throw when the operation is canceled.

This operation will not block. The returned [IAsyncOperationWithProgress(HttpRequestResult,HttpProgress)](../windows.foundation/iasyncoperationwithprogress_2.md) object will complete after the whole response (including content) is read.

## -see-also
[HttpRequestMessage](httprequestmessage.md), [HttpRequestResult](httprequestresult.md), [HttpProgress](httpprogress.md), [HttpResponseMessage](httpresponsemessage.md)

## -examples

