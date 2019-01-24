---
title: AddMessage | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 102a0404-a00c-4566-93f3-01bc8df63280
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: f01d4e80c3740ae27b5df8badbc74989c2da2c60
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54757929"
---
# <a name="addmessage"></a>AddMessage
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Grafik tanılama için özel bir ileti ekler *baş üstü* (baş yukarı Göster).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
void AddMessage(  
  wchar_t const * szMessage  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `szMessage`  
 Baş üstü için eklenecek ileti.  
  
## <a name="remarks"></a>Açıklamalar  
 Grafik tanılama baş üstü grafik tanılama altında çalışmakta olan uygulamayı sol üst köşesinde görüntülenir. Uygulama ve grafik bilgilerini yakalama ve bu işlevi çağrılarak eklenir iletileri hakkında çalışma zamanı bilgileri görüntüler.  
  
 Baş üstü için bir ileti eklemek için grafik bilgilerini yakalama etkin gerekmez; diğer bir deyişle, bir ileti örneği eklenebilir `VsgDbg` sınıfı, ancak [Init](../debugger/init.md) ilk olarak üye işlev yok. İletileri yalnızca baş üstü görüntülenir, grafik günlük dosyasına kaydedilmez.
