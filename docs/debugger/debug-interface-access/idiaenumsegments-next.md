---
title: Idiaenumsegments::Next | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumSegments::Next method
ms.assetid: 53f61874-d821-47ab-a1f5-27e982804a6a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 965e226d4d3cfef563ee8237b96734e4d620ae42
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55009745"
---
# <a name="idiaenumsegmentsnext"></a>IDiaEnumSegments::Next
Belirtilen bir numaralandırma sıralı segmentleri sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT Next (   
   ULONG         celt,   
   IDiaSegment** rgelt,  
   ULONG*        pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 celt  
 [in] Alınacak numaralandırıcıyı kesimleri sayı.  
  
 http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp  
 [out] İstenen ile doldurulacak bir dizi [Idiasegment](../../debugger/debug-interface-access/idiasegment.md) segmentleri temsil eden nesneleri.  
  
 pceltFetched  
 [out] Segment sayısı getirilen bir numaralandırıcı döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` daha fazla segment varsa. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumsegments](../../debugger/debug-interface-access/idiaenumsegments.md)   
 [IDiaSegment](../../debugger/debug-interface-access/idiasegment.md)