---
title: Jsdebugpropertyınfo yapısı | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- JsDebugPropertyInfo
apilocation:
- jscript9diag.dll
ms.assetid: 3a5463a7-2013-4846-9ab2-8beb675a5a6a
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 317cf5adc459c1491d037678616c17de2a619d96
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54095478"
---
# <a name="jsdebugpropertyinfo-structure"></a>JsDebugPropertyInfo Yapısı
Bir özellik hakkında bilgi gösterir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef struct tagJsDebugPropertyInfo{   BSTR name;   BSTR type;   BSTR value;   BSTR fullName;   JS_PROPERTY_ATTRIBUTES attr;} JsDebugPropertyInfo;  
```  
  
## <a name="members"></a>Üyeler  
 `name`  
 Özelliğin adı.  
  
 `type`  
 Özelliğin türü.  
  
 `value`  
 Özelliğin değeri.  
  
 `fullName`  
 Özelliğin tam adı.  
  
 `attr`  
 Özellik özniteliklerini temsil eden bir sabit listesi.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Windows Betik Arabirimleri Başvurusu](../../winscript/reference/windows-script-interfaces-reference.md)