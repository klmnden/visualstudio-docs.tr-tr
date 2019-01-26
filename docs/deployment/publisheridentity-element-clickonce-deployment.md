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
ms.openlocfilehash: d1fa91423a5c0ddf6b276095b53ae4461d7057c4
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55005533"
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