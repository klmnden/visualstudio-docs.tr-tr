---
title: IScriptEntry::GetRange | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 6a4e053817ed4c503ebb41e2f3828da421e69ec7
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54088744"
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