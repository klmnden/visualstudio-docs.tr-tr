---
title: Idiaenumlinenumbers::Next | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumLineNumbers::Next method
ms.assetid: 363d5b40-1316-4ab8-836f-63637f619e0a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 66abd987e3da4fadaac9d5b2de6664c4ae9e24ac
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62829764"
---
# <a name="idiaenumlinenumbersnext"></a>IDiaEnumLineNumbers::Next
Belirtilen bir numaralandırma sıralı satır numaralarını sayısını alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Next ( 
   ULONG            celt,
   IDiaLineNumber** rgelt,
   ULONG*           pceltFetched
);
```

#### <a name="parameters"></a>Parametreler
 celt

[in] Alınacak Numaralandırıcı satır numaralarını sayısı.

 http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp

[out] Bir dizi döndürür [Idialinenumber](../../debugger/debug-interface-access/idialinenumber.md) istenen satır numaralarını temsil eden nesneleri.

 pceltFetched

[out] Satır numaraları getirilen bir numaralandırıcı döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa daha fazla satır numarası yok. Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumLineNumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)
- [IDiaLineNumber](../../debugger/debug-interface-access/idialinenumber.md)
- [IDiaSession::findLinesByLinenum](../../debugger/debug-interface-access/idiasession-findlinesbylinenum.md)