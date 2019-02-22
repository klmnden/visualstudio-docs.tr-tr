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
ms.openlocfilehash: 73ec1bacc0efd02020712f0aceadf69772de47a9
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56644334"
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
- [out içinde] Dosyadan okunan bayt ile doldurulmuş bir dizi.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, bir göreli sanal adres kullanarak bir çalıştırılabilir dosyadan veri baytı yüklenecek DIA destek kod tarafından çağrılır. Support, bu yöntem çağrılır [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaReadExeAtRVACallback](../../debugger/debug-interface-access/idiareadexeatrvacallback.md)
- [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)