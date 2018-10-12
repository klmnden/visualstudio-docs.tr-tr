---
title: ToggleHUD | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 7261e01d-3c72-46ce-9fb3-5f33b2ddb901
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 62d202bfca33619c14d00ec99dc44857cb01bb6a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49250453"
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



