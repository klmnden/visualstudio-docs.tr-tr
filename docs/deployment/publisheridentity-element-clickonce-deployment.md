---
title: '&lt;publisherIdentity&gt; öğesi (ClickOnce dağıtımı) | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- publisherIdentity Element [ClickOnce deployment manifest], introduction
- required element for signed manifests [ClickOnce], publisherIdentity Element
- publisherIdentity Element [ClickOnce deployment manifest], syntax, elements, and attributes
ms.assetid: 34c579db-d2f2-4b66-b9c8-47207f33d950
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 995b002784c1e76ceed36e51edb1ae893448f448
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62927545"
---
# <a name="ltpublisheridentitygt-element-clickonce-deployment"></a>&lt;publisherIdentity&gt; öğesi (ClickOnce dağıtımı)
Bu dağıtım bildirimi imzalayan yayımcı hakkında bilgi içerir.

## <a name="syntax"></a>Sözdizimi

```xml
<publisherIdentity
   name
   issuerKeyHash
/>
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 `publisherIdentity` Öğesi imzalı bildirimler için gereklidir. Aşağıdaki tabloda, öznitelikleri gösterir `publisherIdentity` öğeyi destekler.

|Öznitelik|Açıklama|
|---------------|-----------------|
|`name`|Gerekli. Bu uygulamayı yayımlayan taraf kimliğini açıklar.|
|`issuerKeyHash`|Gerekli. Ortak anahtar sertifika verenin SHA-1 karması içerir.|

#### <a name="parameters"></a>Parametreler

## <a name="property-valuereturn-value"></a>Özellik değeri/dönüş değeri

## <a name="exceptions"></a>Özel Durumlar

## <a name="remarks"></a>Açıklamalar

## <a name="requirements"></a>Gereksinimler

## <a name="subhead"></a>Alt başlık