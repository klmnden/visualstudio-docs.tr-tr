---
title: Idiasession::findsymbolbyaddr | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::findSymbolByAddr method
ms.assetid: c130abc5-4d0a-4d2d-8286-94fde36ddd4a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fcbe9e97eb429fa7427ae0e3da4dce77281b40a0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839283"
---
# <a name="idiasessionfindsymbolbyaddr"></a>IDiaSession::findSymbolByAddr
İçeriyor veya belirtilen bir adres için en yakın olan bir belirtilen simge türü alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT findSymbolByAddr ( 
   DWORD        isect,
   DWORD        offset,
   SymTagEnum   symtag,
   IDiaSymbol** ppSymbol
);
```

#### <a name="parameters"></a>Parametreler
 `isect`

[in] Bölüm bileşeni adresi belirtir.

 `offset`

[in] Adres uzaklık bileşeni belirtir.

 `symtag`

[in] Bulunacak simge türü. Değerleri verilerinden alınır [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) sabit listesi.

 `ppSymbol`

[out] Döndürür bir [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) sembol temsil eden bir nesne alındı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="example"></a>Örnek

```C++
IDiaSymbol* pFunc;
pSession->findSymbolByAddr( isect, offset, SymTagFunction, &pFunc );
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [SymTagEnum Numaralandırması](../../debugger/debug-interface-access/symtagenum.md)