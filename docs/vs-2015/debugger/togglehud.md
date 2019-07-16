---
title: ToggleHUD | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 7261e01d-3c72-46ce-9fb3-5f33b2ddb901
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 87c2571926b92e59ae03e5e988bbf535474dc6d0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68144573"
---
# <a name="togglehud"></a>ToggleHUD
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Grafik tanılama değiştirir *baş üstü* (baş yukarı Göster) kaplama veya kapat.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
void ToggleHUD();  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Grafik tanılama baş üstü grafik tanılama altında çalışmakta olan uygulamayı sol üst köşesinde görüntülenir. Uygulama ve grafik bilgilerini yakalama ve çağırarak eklenen iletileri hakkında çalışma zamanı bilgilerini görüntüler [AddMessage](../debugger/addmessage.md) üye işlevi.  
  
 Baş üstü geçiş yapmak için grafik bilgilerini yakalama etkin gerekmez; diğer bir deyişle, bir örneği üzerinden değiştirilebilir `VsgDbg` sınıfı, ancak [Init](../debugger/init.md) üye işlevi ilk kez çağrılması gerekmez.
