---
title: StopTrackingAndCleanup | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
apiname:
- StopTrackingAndCleanup
apilocation:
- filetracker.dll
apitype: COM
helpviewer_keywords:
- StopTrackingAndCleanup
ms.assetid: 9f8c5994-2dfc-43c3-a5fb-89b2f8990429
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 56f4fb82ab0e9792cadbeeea05499744e4c8ce46
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56621311"
---
# <a name="stoptrackingandcleanup"></a>StopTrackingAndCleanup
Tüm izleme durdurur ve izleme oturumu tarafından kullanılan belleği serbest bırakır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT WINAPI StopTrackingAndCleanup(void);
```

## <a name="return-value"></a>Dönüş değeri
 Döndürür bir **HRESULT** ile **başarılı** izleme durduruldu durumunda biti ayarlanmamış.

## <a name="requirements"></a>Gereksinimler
 **Üst bilgi:** *FileTracker.h*

## <a name="see-also"></a>Ayrıca bkz.
- [StartTrackingContext](../msbuild/starttrackingcontext.md)