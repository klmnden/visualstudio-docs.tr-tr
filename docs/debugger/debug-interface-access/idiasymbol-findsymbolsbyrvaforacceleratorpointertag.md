---
title: IDiaSymbol::findSymbolsByRVAForAcceleratorPointerTag | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 024ccd78-5867-4ca7-bc26-548758e9ac53
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: eb7765f4864208d4dbc494f2877efc0d87c695a9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55039972"
---
# <a name="idiasymbolfindsymbolsbyrvaforacceleratorpointertag"></a>IDiaSymbol::findSymbolsByRVAForAcceleratorPointerTag
Karşılık gelen bir etiket değeri verildiğinde, bu yöntem bu saplama işlevinde belirtilen göreli sanal adresten bulunan simgeleri bir sabit listesi döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT findSymbolsByRVAForAcceleratorPointerTag (   
   DWORD             tagValue,  
   DWORD             rva,  
   IDiaEnumSymbols** ppResult);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `tagValue`  
 [in] İşaretçi etiket değeri için pointee sembol kayıtların bulunduğu.  
  
 `rva`  
 [in] Belirtilen etiket değeri ile pointee değişkenine karşılık gelen simgeleri filtrelemek üzere kullanılan rva.  
  
 `ppResult`  
 [out] Bir işaretçi bir `IDiaEnumSymbols` arabirim işaretçisini, bir sonuç ile başlatılır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
## <a name="remarks"></a>Açıklamalar  
 Yalnızca bu yöntemi çağıran bir `IDiaSymbol` karşılık gelen bir Hızlandırıcı saplama işlevi için arabirim.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [IDiaEnumSymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)