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
ms.openlocfilehash: cb05bb6a424b5639e0ee98e96c80315c51081ace
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56688322"
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