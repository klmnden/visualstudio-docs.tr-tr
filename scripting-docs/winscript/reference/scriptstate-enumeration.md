---
title: SCRIPTSTATE sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- SCRIPTSTATE
apilocation:
- scrobj.dll
helpviewer_keywords:
- SCRIPTSTATE enum
ms.assetid: 5f5deb05-c4bb-4964-8077-e624c6b2a14e
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fe6a05c5e73d26a8daa9e46c317422d85d1c40be
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58155556"
---
# <a name="scriptstate-enumeration"></a>SCRIPTSTATE Numaralandırması
Bir komut dosyası altyapısı durumunu belirtir. Bu sabit listesi tarafından kullanılan [IActiveScript::GetScriptState](../../winscript/reference/iactivescript-getscriptstate.md) , [IActiveScript::SetScriptState](../../winscript/reference/iactivescript-setscriptstate.md) , ve [IActiveScriptSite::OnStateChange](../../winscript/reference/iactivescriptsite-onstatechange.md) yöntemleri.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef enum tagSCRIPTSTATE {  
    SCRIPTSTATE_UNINITIALIZED = 0,  
    SCRIPTSTATE_INITIALIZED   = 5,  
    SCRIPTSTATE_STARTED       = 1,  
    SCRIPTSTATE_CONNECTED     = 2,  
    SCRIPTSTATE_DISCONNECTED  = 3,  
    SCRIPTSTATE_CLOSED        = 4  
} SCRIPTSTATE;  
```  
  
## <a name="enumeration-values"></a>Sabit listesi değerleri  
  
|||  
|-|-|  
|SCRIPTSTATE_UNINITIALIZED|Betik, yeni oluşturduğunuz ancak henüz kullanarak başlatılmamış bir `IPersist*` arabirimi ve [IActiveScript::SetScriptSite](../../winscript/reference/iactivescript-setscriptsite.md) .|  
|SCRIPTSTATE_INITIALIZED|Betik başlatıldı, ancak değil (diğer nesnelere bağlanma veya olayları indirme) çalıştıran veya herhangi bir kod yürütme. Kod sorgulanabilen yürütme için çağırarak [IActiveScriptParse::ParseScriptText](../../winscript/reference/iactivescriptparse-parsescripttext.md) yöntemi.|  
|SCRIPTSTATE_STARTED|Betik kodu yürütebilir henüz tarafından eklenen nesneleri olaylarını indirme değil ancak [IActiveScript::AddNamedItem](../../winscript/reference/iactivescript-addnameditem.md) yöntemi.|  
|SCRIPTSTATE_CONNECTED|Betik yüklenir ve olayları indirme için bağlı.|  
|SCRIPTSTATE_DISCONNECTED|Betik yüklenir ve bir çalışma zamanı yürütme durumu vardır, ancak geçici olarak olayları batmasını bağlantısı kesildi.|  
|SCRIPTSTATE_CLOSED|Betik kapatıldı. Komut dosyası altyapısı artık çalışır ve çoğu yöntemleri için hataları döndürür.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Sabitleri, Sabit Listeleri ve Hata Kodları](../../winscript/reference/active-script-constants-enumerations-and-error-codes.md)