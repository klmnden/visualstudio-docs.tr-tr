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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9608ca6237a44d48d4ee4c4d8daf057d88fc5b53
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53947841"
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