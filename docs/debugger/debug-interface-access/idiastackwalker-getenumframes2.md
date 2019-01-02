---
title: IDiaStackWalker::getEnumFrames2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalker2::getEnumFrames2 method
ms.assetid: 73196d3f-112c-4b3a-997b-7c6b815d4afc
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a6391e90a10477d07e5f35e8f5607bee3f412031
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53935937"
---
# <a name="idiastackwalkergetenumframes2"></a>IDiaStackWalker::getEnumFrames2
Belirli bir platform türü için bir yığın çerçevesi Numaralandırıcı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
  
      HRESULT getEnumFrames2(   
   enum  CV_CPU_TYPE_e    cpuid,  
   IDiaStackWalkHelper*   pHelper,  
   IDiaEnumStackFrames**  ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `cpuid`  
 [in] Bir değer [CV_CPU_TYPE_e numaralandırması](../../debugger/debug-interface-access/cv-cpu-type-e.md) platform türünü belirten numaralandırma.  
  
 `pHelper`  
 [in] Yardımcı [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md) nesne.  
  
 `ppEnum`  
 [out] Döndürür bir [Idiaenumstackframes](../../debugger/debug-interface-access/idiaenumstackframes.md) listesini içeren bir nesne [Idiastackframe](../../debugger/debug-interface-access/idiastackframe.md) nesneleri.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 X86 için yığın çerçeve listesini almak için platform, çağrı [IDiaStackWalker::getEnumFrames](../../debugger/debug-interface-access/idiastackwalker-getenumframes.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiastackwalker](../../debugger/debug-interface-access/idiastackwalker.md)   
 [CV_CPU_TYPE_e numaralandırması](../../debugger/debug-interface-access/cv-cpu-type-e.md)   
 [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)   
 [Idiastackframe](../../debugger/debug-interface-access/idiastackframe.md)   
 [IDiaStackWalker::getEnumFrames](../../debugger/debug-interface-access/idiastackwalker-getenumframes.md)