---
title: IDiaSymbol::findSymbolsByRVAForAcceleratorPointerTag | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
ms.assetid: 024ccd78-5867-4ca7-bc26-548758e9ac53
caps.latest.revision: 6
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: ee1aea023124fb8277fd13cf341a63fca92c37cd
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "68149869"
---
# <a name="idiasymbolfindsymbolsbyrvaforacceleratorpointertag"></a>IDiaSymbol::findSymbolsByRVAForAcceleratorPointerTag
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Karşılık gelen bir etiket değeri verildiğinde, bu yöntem bu saplama işlevinde belirtilen göreli sanal adresten bulunan simgeleri bir sabit listesi döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
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
