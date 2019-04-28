---
title: Idiaenumsourcefiles::Next | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumSourceFiles::Next method
ms.assetid: 83bf6317-ff39-4c5c-8987-cba34e7a6983
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 29424c2b12884cae7f803a46e15f7183d9690d96
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62829634"
---
# <a name="idiaenumsourcefilesnext"></a>IDiaEnumSourceFiles::Next
Belirtilen bir sabit listesi sırası kaynak dosyalarında sayısını alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Next ( 
   ULONG            celt,
   IDiaSourceFile** rgelt,
   ULONG*           pceltFetched
);
```

#### <a name="parameters"></a>Parametreler
 celt

[in] Alınacak Numaralandırıcı kaynak dosya sayısı.

 http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp

[out] İle doldurulacak bir dizi [Idiasourcefile](../../debugger/debug-interface-access/idiasourcefile.md) istenen kaynak dosyalarını temsil eden nesneleri.

 pceltFetched

[out] Kaynak dosyalarının getirilen bir numaralandırıcı döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` daha fazla kaynak dosya yoksa. Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumSourceFiles](../../debugger/debug-interface-access/idiaenumsourcefiles.md)
- [IDiaSession::findLinesByLinenum](../../debugger/debug-interface-access/idiasession-findlinesbylinenum.md)
- [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)