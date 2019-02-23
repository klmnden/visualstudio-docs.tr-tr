---
title: AddMessage | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 102a0404-a00c-4566-93f3-01bc8df63280
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 41a71a69c916bf2fff30b2dee8784d5d9997436b
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56705576"
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
 `szMessage` Baş üstü için eklenecek ileti.

## <a name="remarks"></a>Açıklamalar
 Grafik tanılama baş üstü grafik tanılama altında çalışmakta olan uygulamayı sol üst köşesinde görüntülenir. Uygulama ve grafik bilgilerini yakalama ve bu işlevi çağrılarak eklenir iletileri hakkında çalışma zamanı bilgileri görüntüler.

 Baş üstü için bir ileti eklemek için grafik bilgilerini yakalama etkin gerekmez; diğer bir deyişle, bir ileti örneği eklenebilir `VsgDbg` sınıfı, ancak [Init](init.md) ilk olarak üye işlev yok. İletileri yalnızca baş üstü görüntülenir, grafik günlük dosyasına kaydedilmez.