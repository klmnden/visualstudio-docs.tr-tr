---
title: Idiaenumınjectedsources::Next | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumInjectedSources::Next method
ms.assetid: 38af80fc-748f-4b15-bff1-823db21dd4d0
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: d40ed9acf9e8c82fa315517c0abc3eb6f6d3b036
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54776486"
---
# <a name="idiaenuminjectedsourcesnext"></a>IDiaEnumInjectedSources::Next
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Belirtilen bir numaralandırma sıralı eklenen kaynakları sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Next (   
   ULONG                celt,   
   IDiaInjectedSource** rgelt,  
   ULONG*               pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 celt  
 [in] Alınacak Numaralandırıcı eklenen kaynakları sayısı.  
  
 http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp  
 [out] Bir dizi döndürür [Idiaınjectedsource](../../debugger/debug-interface-access/idiainjectedsource.md) istenen eklenen kaynakları temsil eden nesneleri.  
  
 pceltFetched  
 [out] Eklenen kaynakları getirilen bir numaralandırıcı döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` artık eklenen kaynakları varsa. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumınjectedsources](../../debugger/debug-interface-access/idiaenuminjectedsources.md)   
 [IDiaInjectedSource](../../debugger/debug-interface-access/idiainjectedsource.md)
