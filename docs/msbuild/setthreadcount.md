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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2b4bfb8e1f60ed668039011841e12021e0f0702f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54942015"
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