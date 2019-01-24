---
title: '&lt;Zamanlamalar&gt; öğesi (Önyükleyici) | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- <Schedules> element [bootstrapper]
ms.assetid: 28d094cf-64f5-42b1-bd8a-3697082aab4f
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 85ffab2272a55bfe77c5f2a73c6e25967a203c85
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54771492"
---
# <a name="ltschedulesgt-element-bootstrapper"></a>&lt;Zamanlamalar&gt; öğesi (Önyükleyici)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

`Schedules` Ögesinin `Schedule` hangi komutları tarafından tanımlanan belirli zamanlarda tanımlayan öğeleri `Command` öğesi çalıştırılmalıdır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<Schedules>  
    <Schedule  
        Name  
    >  
        <BuildList />  
        <BeforePackage />  
        <AfterPackage />  
    </Schedule>  
</Schedules>  
```  
  
## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler  
 `Schedules` Öğesi alt öğesi olan `Product` öğesi. Her `Product` öğesi, en fazla bir olabilir `Schedules` öğesi. `Schedules` Öğesi özniteliklere sahip değildir.  
  
## <a name="schedule"></a>Zamanlama  
 `Schedule` Öğesi alt öğesi olan `Schedules` öğesi. A `Schedules` öğesi en az bir olmalı `Schedule` öğesi.  
  
 `Schedule` Aşağıdaki özniteliklere sahiptir.  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`Name`|Gerekli. Zamanlama öğesinin adı. Bu karşılık gelir `ScheduleName` özelliği `Command` öğesi. Olduğunda bir `Command` adlandırılmış zamanlama başvuran tarafından belirtilen zaman yalnızca yürütülecek `Schedule` öğesi. Zamanlamalar ayrıca ile ilişkili olabilir `FailIf` ve `BypassIf` koşullu bu testleri belirli bir zamanlamaya göre çalıştırma için kısıtlama öğeleri. Daha fazla bilgi için [ \<komutları > öğesi](../deployment/commands-element-bootstrapper.md).|  
  
 Belirli bir `Schedule` öğe aşağıdaki alt tam olarak birine sahip.  
  
## <a name="buildlist"></a>BuildList  
 `BuildList` Önyükleme uygulaması başladıktan hemen sonra bir komut çalıştırmak için yükleyici öğesi bildirir.  
  
## <a name="beforepackage"></a>BeforePackage  
 `BeforePackage` Öğesi belirtilen paket yüklenmeden önce bir komut çalıştırmak için yükleyici bildirir.  
  
## <a name="afterpackage"></a>AfterPackage  
 `AfterPackage` Öğesi belirtilen paket yüklendikten sonra bir komut çalıştırmak için yükleyici bildirir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [\<Ürün > öğesi](../deployment/product-element-bootstrapper.md)   
 [Ürün ve Paket Şema Başvurusu](../deployment/product-and-package-schema-reference.md)
