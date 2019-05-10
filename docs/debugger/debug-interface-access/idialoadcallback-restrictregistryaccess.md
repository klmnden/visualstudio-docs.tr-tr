---
title: Idialoadcallback::restrictregistryaccess | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback::RestrictRegistryAccess method
ms.assetid: de4760c3-a746-4bab-8065-1388fed31b67
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 25e6397b65c717be65a9a707dd0a53fc70321acb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62828489"
---
# <a name="idialoadcallbackrestrictregistryaccess"></a>IDiaLoadCallback::RestrictRegistryAccess
Kayıt defteri sorguları sembol arama yollarını bulmak için kullanılabilir olmadığını belirler.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT RestrictRegistryAccess();
```

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Herhangi bir dışındaki kod dönüş `S_OK` simge arama yolu için kayıt defterini sorgulayarak engeller.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)