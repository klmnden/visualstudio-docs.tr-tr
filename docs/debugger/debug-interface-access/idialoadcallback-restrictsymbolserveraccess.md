---
title: Idialoadcallback::restrictsymbolserveraccess | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback::RestrictSymbolServerAccess method
ms.assetid: db37ad9f-f75e-4f0c-83bf-21a6e66ba859
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0de567f0417714e1246e11ba074c9b0134e92ce8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839777"
---
# <a name="idialoadcallbackrestrictsymbolserveraccess"></a>IDiaLoadCallback::RestrictSymbolServerAccess
Erişim bir simge sunucusuna simgeleri çözme izin verilip verilmediğini belirler.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT RestrictSymbolServerAccess();
```

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Herhangi bir dışındaki kod dönüş `S_OK` bir simge sunucusuna simgeleri çözme kullanımını engeller.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)