---
title: POPDIRLISTFUNC | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- POPLISTFUNC
helpviewer_keywords:
- POPDIRLISTFUNC callback function
ms.assetid: 0ee90fd2-5467-4154-ab4c-7eb02ac3a14c
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0fef3ab783c736fd2573e8d9df1a513e25d37020
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66326127"
---
# <a name="popdirlistfunc"></a>POPDIRLISTFUNC
Bu, verilen bir geri çağırma işlevini [SccPopulateDirList](../extensibility/sccpopulatedirlist-function.md) işleviyle dizinleri ve (isteğe bağlı olarak), kaynak denetimi altında olduğunu öğrenmek için dosya adları topluluğu.

 `POPDIRLISTFUNC` Yalnızca dizin ve dosya adları için geri çağırma'nin çağrılabilir (verilen listedeki `SccPopulateDirList` işlevi) olan gerçekten kaynak denetimi altında.

## <a name="signature"></a>İmza

```cpp
typedef BOOL (*POPDIRLISTFUNC)(
   LPVOID pvCallerData,
   BOOL bFolder,
   LPCSTR lpDirectoryOrFileName
);
```

## <a name="parameters"></a>Parametreler
 pvCallerData

[in] Verilen kullanıcı değeri [SccPopulateDirList](../extensibility/sccpopulatedirlist-function.md).

 bKlasör

[in] `TRUE` varsa adın `lpDirectoryOrFileName` bir dizin; Aksi takdirde adı bir dosya adıdır.

 lpDirectoryOrFileName

[in] Kaynak kodu denetimi altında dizin veya dosya adı tam yerel yolu.

## <a name="return-value"></a>Dönüş değeri
 IDE uygun hata kodu döndürür:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|İşleme devam edin.|
|SCC_I_OPERATIONCANCELED|İşlemeyi durdur.|
|SCC_E_xxx|Herhangi bir uygun kaynak denetimi hata işleme durdurmanız gerekir.|

## <a name="remarks"></a>Açıklamalar
 Varsa `fOptions` parametresinin `SccPopulateDirList` işlevi içeren `SCC_PDL_INCLUDEFILES` liste büyük bir olasılıkla dosya adları ve bunun yanı sıra dizin adları içerir bayrağı.

## <a name="see-also"></a>Ayrıca bkz.
- [IDE tarafından uygulanan geri çağırma işlevleri](../extensibility/callback-functions-implemented-by-the-ide.md)
- [SccPopulateDirList](../extensibility/sccpopulatedirlist-function.md)
- [Hata kodları](../extensibility/error-codes.md)