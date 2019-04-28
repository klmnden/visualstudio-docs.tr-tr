---
title: IDiaSession::findSymbolsByRVAForAcceleratorPointerTag | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: a073cc45-0c7b-417e-b5fc-a3b08beccdbc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5bcf399dcf80cb574b6018dde5ffa44e72a4c988
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839218"
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
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
- [IDiaEnumSymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)