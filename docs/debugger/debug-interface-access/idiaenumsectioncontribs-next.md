---
title: Idiaenumsectioncontribs::Next | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumSectionContribs::Next method
ms.assetid: a6bb2adb-ee6d-4f3c-ab5b-e89361c8880e
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 915588402264ac6ba7076f3e9cd95b347b946689
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53936275"
---
# <a name="idiaenumsectioncontribsnext"></a>IDiaEnumSectionContribs::Next
Belirtilen bir numaralandırma sıralı bölümü Katkıları sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT Next(   
   ULONG                celt,   
   IDiaSectionContrib** rgelt,  
   ULONG*               pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 celt  
 [in] Alınacak Numaralandırıcı bölümüne katkı sayısı.  
  
 http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp  
 [out] İle doldurulacak bir dizi [Idiasectioncontrib](../../debugger/debug-interface-access/idiasectioncontrib.md) istenen bölüm katkılarını temsil eden nesneleri.  
  
 pceltFetched  
 [out] Bölüm Katkıları getirilen bir numaralandırıcı döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` daha fazla bölüm katkı varsa. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumsectioncontribs](../../debugger/debug-interface-access/idiaenumsectioncontribs.md)   
 [IDiaSectionContrib](../../debugger/debug-interface-access/idiasectioncontrib.md)