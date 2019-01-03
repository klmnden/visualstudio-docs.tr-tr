---
title: AddMessage | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 102a0404-a00c-4566-93f3-01bc8df63280
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 6555072bcbebe24011ca0701f02f48bc1703c34a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53985741"
---
# <a name="addmessage"></a>AddMessage
Grafik tanılama için özel bir ileti ekler *baş üstü* (baş yukarı Göster).  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
void AddMessage(  
  wchar_t const * szMessage  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `szMessage`  
 Baş üstü için eklenecek ileti.  
  
## <a name="remarks"></a>Açıklamalar  
 Grafik tanılama baş üstü grafik tanılama altında çalışmakta olan uygulamayı sol üst köşesinde görüntülenir. Uygulama ve grafik bilgilerini yakalama ve bu işlevi çağrılarak eklenir iletileri hakkında çalışma zamanı bilgileri görüntüler.  
  
 Baş üstü için bir ileti eklemek için grafik bilgilerini yakalama etkin gerekmez; diğer bir deyişle, bir ileti örneği eklenebilir `VsgDbg` sınıfı, ancak [Init](init.md) ilk olarak üye işlev yok. İletileri yalnızca baş üstü görüntülenir, grafik günlük dosyasına kaydedilmez.