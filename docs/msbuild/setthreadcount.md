---
title: SetThreadCount | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
apiname:
- SetThreadCount
apilocation:
- filetracker.dll
apitype: COM
helpviewer_keywords:
- SetThreadCount
ms.assetid: 335335a5-8ca0-4e18-95f5-62aa6a691386
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 13e7e2bb1ecabc67f60da7b2d4c68b413fa9cf92
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53844372"
---
# <a name="setthreadcount"></a>SetThreadCount
Genel iş parçacığı sayısını ayarlar ve bu sayı geçerli iş parçacığına atar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cmd  
HRESULT WINAPI SetThreadCount(int threadCount);  
```  
  
#### <a name="parameters"></a>Parametreler  
 [in] `threadCount`  
 Kullanılacak iş parçacığı sayısı.  
  
## <a name="return-value"></a>Dönüş değeri  
 Bir **HRESULT** ile **başarılı** iş parçacığı sayısı güncelleştirdiyseniz biti ayarlanmamış.  
  
## <a name="requirements"></a>Gereksinimler  
 **Üst bilgi:** *FileTracker.h*