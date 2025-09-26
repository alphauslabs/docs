# Overview

!!! info "API Reference"
    [https://labs.alphaus.cloud/blueapidocs/](https://labs.alphaus.cloud/blueapidocs/)

**Blue API** allows you to programmatically access our services such as [Ripple](https://alphaus.cloud/en/product/ripple/), [WavePro](https://alphaus.cloud/en/product/wave/), and [Octo](https://www.alphaus.cloud/en/octo). It uses [protocol buffers](https://developers.google.com/protocol-buffers/) for service and message definitions, and [gRPC](https://grpc.io/) for implementation and server/client stub generation. It also uses [grpc-gateway](https://grpc-ecosystem.github.io/grpc-gateway/) for proxying JSON/REST requests to gRPC, and generating [OpenAPI](https://www.openapis.org/) documentation. This way, you have the option to use our APIs using either gRPC or JSON/REST, or both.

Apart from Octo, some of the APIs currently supported in Ripple, and WavePro are still not available in Blue. In the meantime, you can still use our JSON/REST APIs [here](../apiref/index.md). We plan to upgrade as many of our JSON/REST APIs as possible over to gRPC as it is significantly more efficient in terms of throughput and CPU usage compared to JSON/REST API. However, we don't intend to deprecate our JSON/REST APIs once the transition is completed. You should be able to use both.

### List of supported APIs

| **API** | **Link** | **Additional info** |
|---------|----------|---------------------|
| Organization API | [https://labs.alphaus.cloud/blueapidocs/#/Organization](https://alphauslabs.github.io/blueapidocs/#/Organization) | - |
| IAM API | [https://labs.alphaus.cloud/blueapidocs/#/Iam](https://alphauslabs.github.io/blueapidocs/#/Iam) | [Link](./apis/iam.md) |
| Admin API | [https://labs.alphaus.cloud/blueapidocs/#/Admin](https://alphauslabs.github.io/blueapidocs/#/Admin) | - |
| Cost API | [https://labs.alphaus.cloud/blueapidocs/#/Cost](https://alphauslabs.github.io/blueapidocs/#/Cost) | - |
| Billing API | [https://labs.alphaus.cloud/blueapidocs/#/Billing](https://alphauslabs.github.io/blueapidocs/#/Billing) | [Link](./apis/billing/billinggroup.md) |
| Operations API | [https://labs.alphaus.cloud/blueapidocs/#/Operations](https://alphauslabs.github.io/blueapidocs/#/Operations) | - |
| Octo API | [https://labs.alphaus.cloud/blueapidocs/#/Cover](https://alphauslabs.github.io/blueapidocs/#/Cover) | - |
| Pricing API | [https://labs.alphaus.cloud/blueapidocs/#/Pricing](https://labs.alphaus.cloud/blueapidocs/#/Pricing) | - |
| Flow API | [https://labs.alphaus.cloud/blueapidocs/#/Flow](https://labs.alphaus.cloud/blueapidocs/#/Flow) | - |
| Prism API | [https://labs.alphaus.cloud/blueapidocs/#/Prism](https://labs.alphaus.cloud/blueapidocs/#/Prism) | - |
| Vortex API | [https://labs.alphaus.cloud/blueapidocs/#/Vortex](https://labs.alphaus.cloud/blueapidocs/#/Vortex) | - |
| Preferences API | [https://labs.alphaus.cloud/blueapidocs/#/Preferences](https://labs.alphaus.cloud/blueapidocs/#/Preferences) | - |

---
