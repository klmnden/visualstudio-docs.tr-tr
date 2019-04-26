---
title: Idiadatasource::get_lasterror | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaDataSource::get_lastError method
ms.assetid: cf08850b-8b75-4e8c-90bd-bd0214756f99
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3ad0570436dda6ac9ae52325c891b32a563cf6f7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62547370"
---
# <a name="idiadatasourcegetlasterror"></a>IDiaDataSource::get_lastError
Son yükleme hatası için dosya adını alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_lastError (
   BSTR* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 pRetVal

[out] Son yükleme hatayla ilişkili .pdb dosyasının adını içeren bir dize döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Bir yükleme işlemi nedeniyle son hata kodunu döndürür. Döndürür `E_INVALIDARG` varsa `pRetVal` parametresi `NULL`.

## <a name="example"></a>Örnek

```C++
BSTR    fileName;
HRESULT errorCode = pSource->get_lastError( &fileName );
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaDataSource](../../debugger/debug-interface-access/idiadatasource.md)