---
title: 'Iscriptnode:: CreateChildEntry | Microsoft Docs'
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptNode. CreateChildEntry
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptNode::CreateChildEntry
ms.assetid: b9682505-4457-40e9-8691-235843637506
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 75369df719b0cd140ce621e916215eb18cf30a9e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62787625"
---
# <a name="iscriptnode-createchildentry"></a>Iscriptnode:: CreateChildEntry
Bir alt örneğini ekler `IScriptEntry`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CreateChildEntry(  
   ULONG              isn,  
   DWORD              dwCookie,  
   LPCOLESTR          pszDelimiter,  
   IScriptEntry       **ppse  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `isn`  
 [in] Üst alt dizini.  
  
 `dwCookie`  
 [in] Alt giriş konak nesnesiyle ilişkilendirmek için kullanılan bir uygulama tanımlı bir değer.  
  
 `pszDelimiter`  
 [in] Sonlandırma, betik bloğu sınırlayıcısı adresi. Ayrıştırma için konak betik bloğunun sonu algılamak için bir sınırlayıcı (örneğin, iki tek tırnak), genellikle kullanır.  
  
 Sınırlayıcı betik yazma altyapısı ön işleme sağlamasına olanak sağlar. Örneğin, altyapı, tek tırnak işareti ayırıcı olarak kullanılacak iki tek tırnak işaretleri ile değiştirebilir. Altyapısı sınırlayıcı nasıl kullanıldığını belirler.  
  
 Bir sınırlayıcıdan betik bloğunun sonu işaretlemez NULL olarak ayarlayın.  
  
 `ppse`  
 [out] Bir işaretçiye alan değişkenin adresini `IScriptEntry` alt örneğinin arabirimi.  
  
 İçin `IScriptNode` Bu parametre bir Web sayfasını temsil eden nesneleri döndüren bir `IScriptEntry` belirten bir betik bloğu örneği.  
  
 İçin `IScriptEntry` Bu parametre bir betik bloğu temsil eden nesneleri döndüren bir `IScriptEntry` belirten bir işlev nesnesi örneği.  
  
 İçin `IScriptEntry` bir işlevi temsil eden nesneleri nesnesi, bu yöntem başarısız olur.  
  
 İçin `IScriptScriptlet` nesneler, bu yöntem başarısız olur.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 `IScriptNode` Arabirimi bir Web sayfası veya öğelerini temsil eder. `IScriptEntry` Arabirimi (türetilen `IScriptNode`) bir betik bloğu ya da bir işlev nesnesi temsil eder. `IScriptScriptlet` Arabirimi (türetilen `IScriptEntry`) bir olay işleyicisini temsil eder.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iscriptnode arabirimi](../../winscript/reference/iscriptnode-interface.md)   
 [IScriptEntry Arabirimi](../../winscript/reference/iscriptentry-interface.md)