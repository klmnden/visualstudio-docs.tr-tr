---
title: IDiaSymbol::get_acceleratorPointerTags | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 30e13cee-e511-49ec-affd-99b0097071b2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c1724ee3e81ac00ed048f323105842361ec22bc7
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "62827300"
---
# <a name="idiasymbolgetacceleratorpointertags"></a>IDiaSymbol::get_acceleratorPointerTags
Bir C++ AMP Hızlandırıcısı saplama işlevi için karşılık gelen tüm Hızlandırıcı işaretçi etiket değerlerini döndürür.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_acceleratorPointerTags(
   DWORD          cnt,
   DWORD*         pcnt,
   DWORD*         pPointerTags);
```

#### <a name="parameters"></a>Parametreler
 `cnt`

[in] Çıkış dizinin boyutu `pPointerTags`.

 `pcnt`

[out] Hızlandırıcı işaretçi etiketleri sayısı C++ AMP Hızlandırıcısı saplama işlevi.

 `pPointerTags`

[out] A `DWORD` Hızlandırıcı işaretçi etiketi değerler ile doldurulan bir dizi işaretçi C++ AMP Hızlandırıcısı saplama işlevi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem üzerinde çağrılır bir `IDiaSymbol` karşılık gelen bir C++ AMP Hızlandırıcısı saplama işlevi için arabirim.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)