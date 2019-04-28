---
title: Idiareadexeatrvacallback::readexecutableatrva | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaReadExeAtRVACallback::ReadExecutableAtRVA method
ms.assetid: 3c1e965f-8f05-41a8-86d8-01830b2377c9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cf423ddc91926fb04adac849783b7c26b4c4f720
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62828482"
---
# <a name="idiareadexeatrvacallbackreadexecutableatrva"></a>IDiaReadExeAtRVACallback::ReadExecutableAtRVA
Bayt belirtilen göreli sanal adres (RVA) yürütülebilir dosyasından başlayarak belirtilen sayıda okur.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT ReadExecutableAtRVA ( 
   DWORD  relativeVirtualAddress,
   DWORD  cbData,
   DWORD* pcbData,
   BYTE   data[]
);
```

#### <a name="parameters"></a>Parametreler
 `relativeVirtualAddress`

[in] Okumanın başlatılacağı RVA yürütülebilir dosya.

 `cbData`

[in] Okunacak bayt sayısı.

 `pcbData`

[out] Okunan bayt sayısını döndürür.

 `data[]`

[out içinde] Dosyadan okunan bayt ile doldurulmuş bir dizi.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, bir göreli sanal adres kullanarak bir çalıştırılabilir dosyadan veri baytı yüklenecek DIA destek kod tarafından çağrılır. Support, bu yöntem çağrılır [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaReadExeAtRVACallback](../../debugger/debug-interface-access/idiareadexeatrvacallback.md)
- [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)