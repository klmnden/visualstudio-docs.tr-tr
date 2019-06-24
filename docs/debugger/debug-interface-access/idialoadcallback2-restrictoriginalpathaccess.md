---
title: Idialoadcallback2::restrictoriginalpathaccess | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback2::RestrictOriginalPathAccess method
ms.assetid: 31fde3af-2824-4b0f-8d0d-cee6046596f6
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 26539d4217682b4d5357f13e9f9368c81297da78
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839751"
---
# <a name="idialoadcallback2restrictoriginalpathaccess"></a>IDiaLoadCallback2::RestrictOriginalPathAccess
Özgün hata ayıklama dizinindeki bir .pdb dosyası aramak uygun olup olmadığını belirler.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT RestrictOriginalPathAccess ();
```

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Herhangi bir dışındaki kod dönüş `S_OK` özgün hata ayıklama dizinindeki bir .pdb dosyasını arayan engeller. Özgün hata ayıklama hata ayıklama etkin olduğunda çalıştırılabilir dosyaya derlenmiş sembol dosyası yolunu dizindir. Bu yolu mutlaka mevcut olduğu yürütülebilir dosya yolu ile aynı değil.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)