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
ms.openlocfilehash: 34954cd32b350a7c5f9c176deffd9943f8e05100
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56641396"
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