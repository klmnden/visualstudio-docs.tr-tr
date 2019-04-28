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
ms.openlocfilehash: 0e2ff32a4eb2218a8b3d09188c787156e484147f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62996692"
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
- [SuspendTracking](../msbuild/suspendtracking.md)