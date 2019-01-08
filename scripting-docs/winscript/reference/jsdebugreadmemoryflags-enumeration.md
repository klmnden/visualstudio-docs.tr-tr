---
title: JsDebugReadMemoryFlags listelemesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: bef1f16ebcf678452f2fe4b0df3ade6350120f05
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54094035"
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