---
title: IActiveScriptAuthor::AddScriptlet | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptAuthor.AddScriptlet
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptAuthor::AddScriptlet
ms.assetid: 879a6651-f187-4934-b130-c1247549900b
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 64df7bd4c0d0dde303cdc15d7111688d14c7dc49
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62935464"
---
# <a name="iactivescriptauthoraddscriptlet"></a>IActiveScriptAuthor::AddScriptlet
Kök düzeyinde alt sitesi olarak kod oluşturma yöntemini ekler `IScriptNode` nesne. Konak ayrıldığında tam adı, yalnızca iki düzeylerine sahip izin verilmez.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT AddScriptlet(  
   LPCOLESTR pszDefaultName,  
   LPCOLESTR pszCode,  
   LPCOLESTR pszItemName,  
   LPCOLESTR pszSubItemName,  
   LPCOLESTR pszEventName,  
   LPCOLESTR pszDelimiter,  
   DWORD dwCookie,  
   DWORD dwFlags  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszDefaultName`  
 [in] Kod oluşturma yöntemiyle ilişkilendirmek için varsayılan adı adresi.  
  
 `pszCode`  
 [in] Kod oluşturma yöntemi metni adresi.  
  
 `pszItemName`  
 [in] Üst düzey konak tam kod oluşturma adı tanıtıcısı arabellek adresi.  
  
 `pszSubItemName`  
 [in] Ana bilgisayarın tam kod oluşturma adı ikinci düzey tanıtıcısı arabellek adresi. Tek düzey adı varsa, NULL olarak ayarlayın.  
  
 `pszEventName`  
 [in] Kod oluşturma yöntemi bir olay işleyicisi olduğu olay adını içeren bir arabellek adresi.  
  
 `pszDelimiter`  
 [in] Sonlandırma, betik bloğu sınırlayıcısı adresi. Zaman `pszCode` ayrıştırılır metin akışından ana bilgisayar genellikle bir sınırlayıcı (örneğin, iki tek tırnak işareti) betik bloğunun sonu algılamak için kullanır. Sınırlayıcı betik bloğunun sonu işaretlemez ise bu parametre NULL olarak ayarlayın.  
  
 `dwCookie`  
 [in] Komut dosyasını bir konak nesnesi ile ilişkilendirmek için kullanılan bir uygulama tanımlı bir değer.  
  
 `dwFlags`  
 [in] Kullanılmıyor.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptAuthor Arabirimi](../../winscript/reference/iactivescriptauthor-interface.md)