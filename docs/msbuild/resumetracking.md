---
title: ResumeTracking | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
apiname:
- ResumeTracking
apilocation:
- filetracker.dll
apitype: COM
helpviewer_keywords:
- ResumeTracking
ms.assetid: d637e019-7c50-4b0a-812e-bc822001e697
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2f0bc04dfa06672e7764676be87584c2a757a50b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54940589"
---
# <a name="resumetracking"></a>ResumeTracking
Geçerli bağlamda izlemeyi sürdürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT WINAPI ResumeTracking();  
```  
  
## <a name="return-value"></a>Dönüş değeri  
 Bir **HRESULT** ile **başarılı** izleme devam ediyor durumunda biti ayarlanmamış. **E_FAIL** izleme bağlamı kullanılabilir olmadığından ettirilemiyor, döndürülür.  
  
## <a name="requirements"></a>Gereksinimler  
 **Üst bilgi:** *FileTracker.h*  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [SuspendTracking](../msbuild/suspendtracking.md)