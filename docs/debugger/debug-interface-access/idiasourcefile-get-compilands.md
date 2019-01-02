---
title: Idiasourcefile::get_compilands | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSourceFile::get_compilands method
ms.assetid: 57deb50a-9c22-43ea-a80c-eab205997bc4
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f799e543cfe5c94fb9f17d9a1e994e7fc3a68ab9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53948361"
---
# <a name="idiasourcefilegetcompilands"></a>IDiaSourceFile::get_compilands
Bu dosya başvuran satır numarasına sahip bir derleme, bir numaralandırıcı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_compilands (   
   IDiaEnumSymbols** ppRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppRetVal`  
 [out] Döndürür bir [Idiaenumsymbols](../../debugger/debug-interface-access/idiaenumsymbols.md) bu dosyayı başvuran satır numaraları olan tüm derleme listesini içeren nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasourcefile](../../debugger/debug-interface-access/idiasourcefile.md)   
 [IDiaEnumSymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)