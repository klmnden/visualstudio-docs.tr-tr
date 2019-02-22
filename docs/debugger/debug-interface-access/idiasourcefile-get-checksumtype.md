---
title: Idiasourcefile::get_checksumtype | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSourceFile::get_checksumType method
ms.assetid: 4c363e61-a6a9-409a-9cc0-d06eb2bee645
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 35e5719d285e9e99e5f7429685fa04a2c6d7f3ab
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56646401"
---
# <a name="idiasourcefilegetchecksumtype"></a>IDiaSourceFile::get_checksumType
Sağlama türünü alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_checksumType ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Sağlama türünü döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Sağlama toplamı, bir sağlama toplamı algoritması için eşlenmiş bir değer türüdür. Örneğin, standart PDB dosya biçimine genellikle aşağıdaki değerlerden biri olabilir:

|Sağlama türü|CryptoAPI Label|Açıklama|
|-------------------|---------------------|-----------------|
|0|\<yok >|Sağlama mevcut.|
|1.|`CALG_MD5`|bir MD5 karma algoritması ile oluşturulan bir sağlama toplamı.|
|2|`CALG_SHA1`|SHA1 karma algoritması ile oluşturulan bir sağlama toplamı.|

 `CryptoAPI` Olan etiketleri `ALG_ID` sabit listesi. Karma algoritmaları hakkında daha fazla bilgi için `CryptoAPI` Microsoft bölümünü [!INCLUDE[winsdkshort](../../debugger/debug-interface-access/includes/winsdkshort_md.md)].

 Kaynak dosyası için asıl sağlama toplamı bayt elde etmek için çağrı [Idiasourcefile::get_checksum](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)
- [IDiaSourceFile::get_checksum](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md)