---
title: Idialoadcallback2::restrictoriginalpathaccess | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback2::RestrictOriginalPathAccess method
ms.assetid: 31fde3af-2824-4b0f-8d0d-cee6046596f6
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 970a188b5d72353dbb3ccf64fd74f3354f1ba888
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54791213"
---
# <a name="idialoadcallback2restrictoriginalpathaccess"></a>IDiaLoadCallback2::RestrictOriginalPathAccess
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Özgün hata ayıklama dizinindeki bir .pdb dosyası aramak uygun olup olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT RestrictOriginalPathAccess ();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Herhangi bir dışındaki kod dönüş `S_OK` özgün hata ayıklama dizinindeki bir .pdb dosyasını arayan engeller. Özgün hata ayıklama hata ayıklama etkin olduğunda çalıştırılabilir dosyaya derlenmiş sembol dosyası yolunu dizindir. Bu yolu mutlaka mevcut olduğu yürütülebilir dosya yolu ile aynı değil.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)
