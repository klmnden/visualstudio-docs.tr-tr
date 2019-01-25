---
title: Idiastackwalkframe | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkFrame interface
ms.assetid: 42d82845-d6f6-4846-9ecd-9dd169216077
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 27aab0ca87e589661798028ff38fb019dae815ed
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54760650"
---
# <a name="idiastackwalkframe"></a>IDiaStackWalkFrame
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Yığın bağlamı çağrıları arasında tutar [Idiaframedata::Execute](../../debugger/debug-interface-access/idiaframedata-execute.md) yöntemi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDiaStackWalkFrame : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDiaStackWalkFrame`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDiaStackWalkFrame::get_registerValue](../../debugger/debug-interface-access/idiastackwalkframe-get-registervalue.md)|Bir kayıt değeri alır.|  
|[IDiaStackWalkFrame::put_registerValue](../../debugger/debug-interface-access/idiastackwalkframe-put-registervalue.md)|Bir kayıt değeri ayarlar.|  
|[IDiaStackWalkFrame::readMemory](../../debugger/debug-interface-access/idiastackwalkframe-readmemory.md)|Bellek görüntüden okur.|  
|[IDiaStackWalkFrame::searchForReturnAddress](../../debugger/debug-interface-access/idiastackwalkframe-searchforreturnaddress.md)|Belirtilen yığın çerçevesinin yakın işlevi dönüş adresi arar.|  
|[IDiaStackWalkFrame::searchForReturnAddressStart](../../debugger/debug-interface-access/idiastackwalkframe-searchforreturnaddressstart.md)|Belirtilen yığın çerçevesinin veya belirtilen adres'e yakın bir dönüş adresi arar.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim, program yürütme sırasında okuma ve yazma kayıtlarını yanı sıra bellek erişim ve dönüş adresi bulmak için kullanılır.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 İstemci uygulaması bu arabirimi uygulayan ve bir arabirimin örneğini geçirir [Idiaframedata::Execute](../../debugger/debug-interface-access/idiaframedata-execute.md) yöntemi. Bu arabirim'ın aynı örneğine tekrar tekrar her çağrılması sırasında kasalar durumunu korumak için kullanılır `execute` yöntemi. `execute` Yöntemi de bu arabirimi dönüş adresi belirlemek için kullanır.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: dia2.h  
  
 Kitaplık: diaguids.lib  
  
 DLL: msdia80.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Arabirimler (arabirim erişimi SDK'SINDA hata ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [IDiaFrameData::execute](../../debugger/debug-interface-access/idiaframedata-execute.md)
