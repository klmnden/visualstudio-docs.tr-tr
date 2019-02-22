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
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56607960"
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

[out] C++ AMP Hızlandırıcısı saplama işlevi Hızlandırıcı işaretçi etiketleri sayısı.

 `pPointerTags`

[out] A `DWORD` C++ AMP Hızlandırıcısı saplama işlevi Hızlandırıcı işaretçi etiketi değerler ile doldurulan bir dizi işaretçi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem üzerinde çağrılır bir `IDiaSymbol` karşılık gelen bir C++ AMP Hızlandırıcısı saplama işlevi için arabirim.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)