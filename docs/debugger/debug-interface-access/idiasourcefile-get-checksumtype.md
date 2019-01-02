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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 750d48cad07251f34e988fa8a6ced618821c443d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53825922"
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
  
|Sağlama türü|CryptoAPI etiketi|Açıklama|  
|-------------------|---------------------|-----------------|  
|0|\<yok >|Sağlama mevcut.|  
|1.|`CALG_MD5`|bir MD5 karma algoritması ile oluşturulan bir sağlama toplamı.|  
|2|`CALG_SHA1`|SHA1 karma algoritması ile oluşturulan bir sağlama toplamı.|  
  
 `CryptoAPI` Olan etiketleri `ALG_ID` sabit listesi. Karma algoritmaları hakkında daha fazla bilgi için `CryptoAPI` Microsoft bölümünü [!INCLUDE[winsdkshort](../../debugger/debug-interface-access/includes/winsdkshort_md.md)].  
  
 Kaynak dosyası için asıl sağlama toplamı bayt elde etmek için çağrı [Idiasourcefile::get_checksum](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasourcefile](../../debugger/debug-interface-access/idiasourcefile.md)   
 [IDiaSourceFile::get_checksum](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md)