---
title: '&lt;Açıklama&gt; öğesi (ClickOnce dağıtımı) | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- urn:schemas-microsoft-com:asm.v2#description
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <description> element [ClickOnce deployment manifest]
ms.assetid: 18f6919e-a3ab-4942-a57d-167fabfac44e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6c359b188894c40f017e3d2a0e06d52de87e9c5f
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56618568"
---
# <a name="ltdescriptiongt-element-clickonce-deployment"></a>&lt;Açıklama&gt; öğesi (ClickOnce dağıtımı)
Bir kabuk varlığı oluşturmak için kullanılan uygulama bilgilerini tanımlar ve bir **Program Ekle veya Kaldır** Denetim Masası'ndaki öğesi.

## <a name="syntax"></a>Sözdizimi

```xml

      <description 
   publisher 
   product
   suiteName
   supportUrl
/>
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 `description` Öğesi gereklidir ve içinde `urn:schemas-microsoft-com:asm.v1` ad alanı. Alt öğe içerir ve aşağıdaki özniteliklere sahiptir.

|Öznitelik|Açıklama|
|---------------|-----------------|
|`publisher`|Gerekli. Windows simge yerleşimi için kullanılan şirket adını tanımlayan **Başlat** menü ve **Program Ekle veya Kaldır** Denetim Masası, yükleme için dağıtım yapılandırıldığında.|
|`product`|Gerekli. Tam ürün adını tanımlar. Windows yüklü simgesi başlığı olarak kullanılan **Başlat** menüsü.|
|`suiteName`|İsteğe bağlı. Bir alt klasörde tanımlayan `publisher` Windows klasöründe **Başlat** menüsü.|
|`supportUrl`|İsteğe bağlı. Gösterilen destek URL'sini belirtir **Program Ekle veya Kaldır** Denetim Masası'ndaki öğesi. Windows uygulama desteği için bu URL için bir kısayol da oluşturulur **Başlat** dağıtım yüklemesi için yapılandırıldığında menüsü.|

## <a name="remarks"></a>Açıklamalar
 Description öğesi tüm dağıtım yapılandırmaları gerekir.

## <a name="example"></a>Örnek
 Aşağıdaki kod örneğinde gösterilmiştir bir `description` öğesinde bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] dağıtım bildirimi. Bu kod örneği için sağlanan daha büyük bir örneğin parçasıdır [ClickOnce dağıtım bildirimi](../deployment/clickonce-deployment-manifest.md) konu.

```xml
<description
  asmv2:publisher="My Company Name"
  asmv2:product="My Application"
  xmlns="urn:schemas-microsoft-com:asm.v1" />
```

## <a name="see-also"></a>Ayrıca bkz.
- [ClickOnce dağıtım bildirimi](../deployment/clickonce-deployment-manifest.md)