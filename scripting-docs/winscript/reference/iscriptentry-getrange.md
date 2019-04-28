---
title: IScriptEntry::GetRange | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptEntry.GetRange
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptEntry::GetRange
ms.assetid: 3ac18f0a-b470-4f4d-b8f5-2da3fdef74f1
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7baa284be4fa7f45f247df7f4b3d140869f254b1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62787743"
---
# <a name="iscriptentrygetrange"></a>IScriptEntry::GetRange
Başlangıç konumu ve bir giriş uzunluğunu döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetRange(  
   ULONG              *pichMin  
   ULONG              *pcch  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pichMin`  
 [out] İçin `IScriptEntry` belirten bir betik bloğu nesneleri 0 döndürür.  
  
 İçin `IScriptEntry` bir işlev nesnesi belirtin nesneleri geçerli betik bloğu içinde işlev başlangıç konumunu döndürür.  
  
 İçin `IScriptScriptlet` nesneleri, 0 döndürür.  
  
 `pcch`  
 [out] İçin `IScriptEntry` belirten bir betik bloğu nesneleri metnin uzunluğunu döndürür.  
  
 İçin `IScriptEntry` bir işlev nesnesi belirtin nesneleri işlev tanımı uzunluğunu döndürür.  
  
 İçin `IScriptScriptlet` nesneleri, giriş uzunluğunu döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IScriptEntry Arabirimi](../../winscript/reference/iscriptentry-interface.md)