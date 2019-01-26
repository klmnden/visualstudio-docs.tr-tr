---
title: ToggleHUD | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 7261e01d-3c72-46ce-9fb3-5f33b2ddb901
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e49066d4625990119159ea72f59a3a3fe59d581c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54953308"
---
# <a name="togglehud"></a>ToggleHUD
Grafik tanılama değiştirir *baş üstü* (baş yukarı Göster) kaplama veya kapat.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
void ToggleHUD();  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Grafik tanılama baş üstü grafik tanılama altında çalışmakta olan uygulamayı sol üst köşesinde görüntülenir. Uygulama ve grafik bilgilerini yakalama ve çağırarak eklenen iletileri hakkında çalışma zamanı bilgilerini görüntüler [AddMessage](addmessage.md) üye işlevi.  
  
 Baş üstü geçiş yapmak için grafik bilgilerini yakalama etkin gerekmez; diğer bir deyişle, bir örneği üzerinden değiştirilebilir `VsgDbg` sınıfı, ancak [Init](init.md) üye işlevi ilk kez çağrılması gerekmez.