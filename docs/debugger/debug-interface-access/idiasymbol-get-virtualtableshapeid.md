---
title: Idiasymbol::get_virtualtableshapeıd | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_virtualTableShapeId method
ms.assetid: cbee9944-817a-4805-9c08-fac8e0da58b7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bd390cbd2982033d31ccf8e577196e2c360be655
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63400124"
---
# <a name="idiasymbolgetvirtualtableshapeid"></a>IDiaSymbol::get_virtualTableShapeId
Simgenin sanal tablo şekli sembol tanımlayıcısını alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_virtualTableShapeId ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Sembol sanal tablo şekli sembol Kimliğini döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için mevcut olmadığı anlamına gelir.

## <a name="remarks"></a>Açıklamalar
 Tanımlayıcı, tüm sembolleri benzersiz olarak işaretlemek için DIA SDK'sı tarafından oluşturulan benzersiz bir değerdir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)