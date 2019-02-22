---
title: Idiareadexeatoffsetcallback::readexecutableat | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaReadExeAtOffsetCallback::ReadExecutableAt method
ms.assetid: 30b1cef0-b366-4712-8e89-d21f640964f8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bda25b870c110324962d0249948929b207d98826
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56619686"
---
# <a name="idiareadexeatoffsetcallbackreadexecutableat"></a>IDiaReadExeAtOffsetCallback::ReadExecutableAt
Belirtilen sayıda baytı bir yürütülebilir dosya öğesinden belirtilen bir uzaklık başlayarak okur.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT ReadExecutableAt ( 
   DWORDLONG fileOffset,
   DWORD     cbData,
   DWORD*    pcbData,
   BYTE      data[]
);
```

#### <a name="parameters"></a>Parametreler
 fileOffset

[in] Okumanın başlatılacağı çalıştırılabilir dosyadaki uzaklık.

 cbData

[in] Okunacak bayt sayısı.

 pcbData

[out] Okunan bayt sayısını döndürür.

 veri]
- [out içinde] Dosyadan okunan bayt ile doldurulmuş bir dizi.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, bir mutlak dosya uzaklık kullanılarak çalıştırılabilir veri baytı yüklenecek DIA destek kod tarafından çağrılır. Support, bu yöntem çağrılır [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaReadExeAtOffsetCallback](../../debugger/debug-interface-access/idiareadexeatoffsetcallback.md)
- [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)