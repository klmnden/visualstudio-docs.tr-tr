---
title: Windows betik konakları | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Windows Script Host, implementing hosts
ms.assetid: 9d5f6471-b318-40f3-be01-d9cd0b1cdd47
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: eec1824bd3ba1a8acb7e3c540656151cd4b11d1f
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58145115"
---
# <a name="windows-script-hosts"></a>Windows Komut Dosyası Konakları
Microsoft Windows betik sistemi uygularken, güvenli bir şekilde bir komut dosyası altyapısı yalnızca çağrıları kabul edilebilir [Iactivescriptsite](../winscript/reference/iactivescriptsite.md) konak aşağıdakileri yapar sürece temel iş parçacığının bağlamında arabirim:  
  
- Bir ana iş parçacığı (ileti döngüsü içeren genellikle iş parçacığı) seçer.  
  
- Ana iş parçacığında komut dosyası altyapısı örneği oluşturur.  
  
- Özellikle, örneklerini olduğu gibi izin verilen altyapısı yöntemlerden yalnızca temel iş parçacığı komut çağrıları [IActiveScript::InterruptScriptThread](../winscript/reference/iactivescript-interruptscriptthread.md) ve [IActiveScript::Clone](../winscript/reference/iactivescript-clone.md).  
  
- Komut dosyası altyapısının dağıtım nesnesi yalnızca ana iş parçacığından çağırır.  
  
- Bir pencere tutucu sağlanırsa, ileti döngüsü ana iş parçacığında çalıştırmasını sağlar.  
  
- Ana bilgisayarın nesnesindeki nesneleri yalnızca kaynak olayları temel bir iş parçacığı modeli sağlar.  
  
  Bu kurallar, tek iş parçacıklı tüm konaklar tarafından otomatik olarak izlenir. Yukarıda açıklanan kısıtlı modeli çağırarak takılan betik iptal etmek bir konak izin vermek için kasıtlı olarak gevşek yeterince [IActiveScript::InterruptScriptThread](../winscript/reference/iactivescript-interruptscriptthread.md) (CTRL + BREAK işleyicisi veya benzeri tarafından başlatılan) başka bir iş parçacığından yenilemek için bir betik kullanarak yeni bir iş parçacığı yinelenen [IActiveScript::Clone](../winscript/reference/iactivescript-clone.md).  
  
## <a name="remarks"></a>Açıklamalar  
 Bu kısıtlamaların hiçbirini bir ücretsiz iş parçacıklı uygulamak için seçtiği bir konağa uygulamayı [Iactivescriptsite](../winscript/reference/iactivescriptsite.md) arabirimi ve ücretsiz iş parçacıklı nesne modeli. Böyle bir konak kullanabilirsiniz [IActiveScript](../winscript/reference/iactivescript.md) kısıtlama olmadan tüm iş parçacığı, arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Windows Komut Dosyası Arabirimleri](../winscript/windows-script-interfaces.md)