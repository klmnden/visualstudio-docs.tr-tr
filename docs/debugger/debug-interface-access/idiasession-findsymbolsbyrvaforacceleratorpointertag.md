---
title: IDiaSession::findSymbolsByRVAForAcceleratorPointerTag | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: a073cc45-0c7b-417e-b5fc-a3b08beccdbc
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ad2a0656b03fb057b631319e922a83605fa62a6e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53859470"
---
# <a name="idiasessionfindsymbolsbyrvaforacceleratorpointertag"></a>IDiaSession::findSymbolsByRVAForAcceleratorPointerTag
Bu yöntem karşılık gelen bir etiket değeri verildiğinde, belirtilen üst Hızlandırıcı saplama işlevinde belirtilen göreli sanal adresten bulunan simgeleri bir sabit listesi döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT findSymbolsByRVAForAcceleratorPointerTag (   
   IDiaSymbol*           parent,  
   DWORD                 tagValue,  
   DWORD                 rva,  
   IDiaEnumSymbols**     ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `parent`  
 [in] Bir `IDiaSymbol` aranacak Hızlandırıcı saplama işlevi karşılık gelir.  
  
 `tagValue`  
 [in] İşaretçi etiket değeri.  
  
 `rva`  
 [in] Göreli sanal adres.  
  
 `ppResult`  
 [out] Bir işaretçi bir `IDiaEnumSymbols` sonucu ile başlatılmış bir arabirim işaretçisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Yalnızca bu yöntemi çağıran bir `IDiaSymbol` karşılık gelen bir Hızlandırıcı saplama işlevi için arabirim.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [Idiaenumsymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)