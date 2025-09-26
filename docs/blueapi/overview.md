# Overview

!!! info "API Reference"
    [https://labs.alphaus.cloud/blueapidocs/](https://labs.alphaus.cloud/blueapidocs/)

**Blue API** allows you to programmatically access our services such as [Ripple](https://alphaus.cloud/en/product/ripple/), [WavePro](https://alphaus.cloud/en/product/wave/), and [Octo](https://www.alphaus.cloud/en/octo). It uses [protocol buffers](https://developers.google.com/protocol-buffers/) for service and message definitions, and [gRPC](https://grpc.io/) for implementation and server/client stub generation. It also uses [grpc-gateway](https://grpc-ecosystem.github.io/grpc-gateway/) for proxying JSON/REST requests to gRPC, and generating [OpenAPI](https://www.openapis.org/) documentation. This way, you have the option to use our APIs using either gRPC or JSON/REST, or both.

Apart from Octo, some of the APIs currently supported in Ripple, and WavePro are still not available in Blue. In the meantime, you can still use our JSON/REST APIs [here](../apiref/index.md). We plan to upgrade as many of our JSON/REST APIs as possible over to gRPC as it is significantly more efficient in terms of throughput and CPU usage compared to JSON/REST API. However, we don't intend to deprecate our JSON/REST APIs once the transition is completed. You should be able to use both.

---
