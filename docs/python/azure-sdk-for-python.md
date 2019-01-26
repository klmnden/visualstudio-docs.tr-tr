---
title: Python için Azure SDK
description: Python için Azure SDK'sı, Microsoft Azure hizmetlerinden herhangi bir platformda çalışan Python uygulamaları kullanmasını kolaylaştırır.
ms.date: 12/06/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: jillfra
ms.workload:
- python
- data-science
- azure
ms.openlocfilehash: b14066272fa160cf2b4fc9f344185a3b68751926
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55031727"
---
# <a name="consume-azure-services-using-the-azure-sdk-for-python"></a>Python için Azure SDK'sını kullanarak Azure hizmetlerini kullanma

Python için Azure SDK'sını kullanma ve Windows, MacOS ve Linux'ta çalışan uygulamalar Microsoft Azure hizmetlerini yönetmenize daha kolay hale getirir.

## <a name="installation"></a>Yükleme

Azure SDK'ın yüklendiği [Python paket dizinini](https://pypi.python.org/pypi/azure).

Yükleme **en son kararlı sürüm** (Python 2.7 ve 3.x gibi destekler):

```command
pip install azure
```

De izleyebilirsiniz [yüklemeniz Python ve SDK'sı](https://docs.microsoft.com/azure/python-how-to-install/) Azure belgeleri.

## <a name="documentation"></a>Belgeler

[Python Geliştirici Merkezi için Azure SDK'sı](https://docs.microsoft.com/python/azure/?view=azure-python) de faydalı kaynaklara, birçok öğretici dahil olmak üzere birçok vardır:

- [Azuyre Linux üzerinde App Service'te Web uygulamaları oluşturma](/azure/app-service/containers/quickstart-python).
- [Blob depolama](/azure/storage/blobs/storage-quickstart-blobs-python)
- [Tablo depolama](/azure/cosmos-db/table-storage-how-to-use-python)
- [Kuyruk depolama](/azure/storage/storage-python-how-to-use-queue-storage)
- [Azure Cosmos DB](/azure/cosmos-db/sql-api-python-application)
- [Service Bus kuyrukları](/azure/service-bus-messaging/service-bus-python-how-to-use-queues)
- [Hizmet veri yolu konuları/abonelikleri](/azure/service-bus-messaging/service-bus-python-how-to-use-topics-subscriptions)
- [Hizmet Yönetimi](/azure/cloud-services/cloud-services-python-how-to-use-service-management)

Belgeler olmadan ortak API'ler için birim testleri içindeki [SDK'sı GitHub deposu](https://github.com/Azure/azure-sdk-for-python) iyi bir bilgi kaynağı olan:

- [Birim testleri](https://github.com/Azure/azure-storage-python/tree/master/tests)
- [Service Bus birim testleri](https://github.com/Azure/azure-sdk-for-python/tree/master/azure-servicebus/tests)
- [Hizmet Yönetimi birim testleri](https://github.com/Azure/azure-sdk-for-python/tree/master/azure-servicemanagement-legacy/tests)

## <a name="support"></a>Destek

SDK'sı GitHub deposunu şu konumdadır [ https://github.com/Azure/azure-sdk-for-python ](https://github.com/Azure/azure-sdk-for-python).

[Deponun sorunlar dosya](https://github.com/Azure/azure-sdk-for-python/issues) problemleri bulun ya da SDK'sının kullanım ile ilgili sorularınız varsa.
