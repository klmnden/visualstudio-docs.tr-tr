---
title: '&lt;publisherIdentity&gt; öğesi (ClickOnce dağıtımı) | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- publisherIdentity Element [ClickOnce deployment manifest], introduction
- required element for signed manifests [ClickOnce], publisherIdentity Element
- publisherIdentity Element [ClickOnce deployment manifest], syntax, elements, and attributes
ms.assetid: 34c579db-d2f2-4b66-b9c8-47207f33d950
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 486e0bc5059e041f02e8dac4836c5ff59b27f63e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54766637"
---
# <a name="ltpublisheridentitygt-element-clickonce-deployment"></a>&lt;publisherIdentity&gt; öğesi (ClickOnce dağıtımı)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu dağıtım bildirimi imzalayan yayımcı hakkında bilgi içerir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
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
  
## <a name="property-valuereturn-value"></a>Özellik Değeri/Dönüş Değeri  
  
## <a name="exceptions"></a>Özel Durumlar  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="requirements"></a>Gereksinimler  
  
## <a name="subhead"></a>Alt başlık
