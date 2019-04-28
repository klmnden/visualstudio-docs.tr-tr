---
title: Idiaenumsourcefiles::Item | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumSourceFiles::Item method
ms.assetid: 3c19d7ed-0232-4b0e-9b10-f33ed9e0c93b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 403aa09a487ea1587ab30389f180afecec5ac6bf
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62833349"
---
# <a name="idiaenumsourcefilesitem"></a>IDiaEnumSourceFiles::Item
Bir kaynak dosyası kullanarak bir dizini alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Item ( 
   DWORD            index,
   IDiaSourceFile** sourceFile
);
```

#### <a name="parameters"></a>Parametreler
 dizin

[in] Dizin [Idiasourcefile](../../debugger/debug-interface-access/idiasourcefile.md) alınacak nesne. İçin 0 aralığındaki dizinidir `count`-1, burada `count` tarafından döndürülen [Idiaenumsourcefiles::get_Count](../../debugger/debug-interface-access/idiaenumsourcefiles-get-count.md) yöntemi.

 Kaynakdosya

[out] Döndürür bir [Idiasourcefile](../../debugger/debug-interface-access/idiasourcefile.md) istenen kaynak dosyasını temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumSourceFiles](../../debugger/debug-interface-access/idiaenumsourcefiles.md)
- [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)