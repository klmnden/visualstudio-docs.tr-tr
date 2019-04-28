---
title: JsDebugReadMemoryFlags listelemesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- JsDebugReadMemoryFlags
apilocation:
- jscript9diag.dll
ms.assetid: 0d98d154-9cb1-49de-b2df-a2d029d343b7
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c908fdbf17b13b84355dff208b7f3106bfc72087
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62830468"
---
# <a name="jsdebugreadmemoryflags-enumeration"></a>JsDebugReadMemoryFlags Listelemesi
Bellek okunduğu sıradaki davranışı belirten bayraklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
enum JsDebugReadMemoryFlags{   None = 0,   JsDebugAllowPartialRead= 0x1} JsDebugReadMemoryFlags;  
```  
  
## <a name="members"></a>Üyeler  
  
### <a name="values"></a>Değerler  
  
|Ad|Açıklama|  
|----------|-----------------|  
|`JsDebugAllowPartialRead`|Arayanın bellek parçası başarılı okuma yalnızca başarılı olması için okuma işlemi istediğini gösterir. Bu ayarlanırsa 'Adres' geçersiz ise bir e_jsdebug_ınvalıd_memory_address hatası yalnızca gerçekleştirilecektir. Bu bayrağı açık ise, istenen belleğin herhangi bir kısmı okunamaz ise bir e_jsdebug_ınvalıd_memory_address hatası oluşur.|  
|`None`|Arayanın ReadMemory için varsayılan davranışı istediğini gösterir.|  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Windows Betik Arabirimleri Başvurusu](../../winscript/reference/windows-script-interfaces-reference.md)