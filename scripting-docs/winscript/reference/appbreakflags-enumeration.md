---
title: APPBREAKFLAGS numaralandırması | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- APPBREAKFLAGS
apilocation:
- scrobj.dll
helpviewer_keywords:
- APPBREAKFLAGS constants
ms.assetid: ea8ed80f-2ddb-4800-bb3b-52b76ba6c7a0
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 49d9cef3583def8cd23e135b960e46979446b3bb
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54349029"
---
# <a name="appbreakflags-enumeration"></a>APPBREAKFLAGS Numaralandırması
Uygulamalar ve iş parçacıkları için geçerli hata ayıklama durumunu gösterir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum enum_APPBREAKFLAGS{APPBREAKFLAG_DEBUGGER_BLOCK= 0x00000001,APPBREAKFLAG_DEBUGGER_HALT= 0x00000002,APPBREAKFLAG_STEP= 0x00010000,APPBREAKFLAG_NESTED= 0x00020000,APPBREAKFLAG_STEPTYPE_SOURCE= 0x00000000,APPBREAKFLAG_STEPTYPE_BYTECODE= 0x00100000,APPBREAKFLAG_STEPTYPE_MACHINE= 0x00200000,APPBREAKFLAG_STEPTYPE_MASK= 0x00F00000,APPBREAKFLAG_IN_BREAKPOINT= 0x80000000};  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Değer|Açıklama|  
|------------|-----------|-----------------|  
|APPBREAKFLAG_DEBUGGER_BLOCK|0x00000001|Dil altyapısı ile BREAKREASON_DEBUGGER_BLOCK tüm iş parçacıkları üzerinde kesme hemen.|  
|APPBREAKFLAG_DEBUGGER_HALT|0x00000002|Dil altyapısı ile BREAKREASON_DEBUGGER_HALT hemen kesilmesine.|  
|APPBREAKFLAG_STEP|0x00010000|Dil altyapısı hemen BREAKREASON_STEP ile Adımlama iş parçacığında Kes.|  
|APPBREAKFLAG_NESTED|0x00020000|Bir kesme noktasında iç içe geçmiş yürütmesinde uygulamasıdır.|  
|APPBREAKFLAG_STEPTYPE_SOURCE|0x00000000|Hata ayıklayıcı kaynak düzeyinde Adımlama.|  
|APPBREAKFLAG_STEPTYPE_BYTECODE|0x00100000|Hata ayıklayıcı bayt kod düzeyinde Adımlama.|  
|APPBREAKFLAG_STEPTYPE_MACHINE|0x00200000|Hata ayıklayıcı, makine düzeyinde Adımlama.|  
|APPBREAKFLAG_STEPTYPE_MASK|0x00F00000|Hesaba katacak şekilde adım türleri için maske.|  
|APPBREAKFLAG_IN_BREAKPOINT|0x80000000|Bir kesme noktası işlemi devam ediyor.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bazı bayrakları diğer bayraklar atlama modu hata ayıklayıcının belirtirken dil altyapıları ilk fırsatta sonu belirtin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin komut dosyası hata ayıklayıcı sabitleri, numaralandırmaları ve yapıları](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)   
 [BREAKREASON Sabit Listesi](../../winscript/reference/breakreason-enumeration.md)