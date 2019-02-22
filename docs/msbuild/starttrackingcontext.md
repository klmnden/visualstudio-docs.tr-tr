---
title: StartTrackingContext | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
apiname:
- StartTrackingContext
apilocation:
- filetracker.dll
apitype: COM
helpviewer_keywords:
- StartTrackingContext
ms.assetid: 720cd295-38e7-4974-86db-b8106b1207ba
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cd0033e189706ee999876a5554e61b1c85eb48ef
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56618815"
---
# <a name="starttrackingcontext"></a>StartTrackingContext
Bir izleme bağlamına başlayın.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT WINAPI StartTrackingContext(LPCTSTR intermediateDirectory, LPCTSTR taskName);
```

#### <a name="parameters"></a>Parametreler
- [in] `intermediateDirectory` İzleme günlüğünü depolanacağı dizin.

- [in] `taskName` İzleme bağlamı tanımlar. Bu ad, günlük dosyası adı oluşturmak için kullanılır.

## <a name="return-value"></a>Dönüş değeri
 Bir **HRESULT** ile **başarılı** izleme bağlamına oluşturulduysa biti ayarlanmamış.

## <a name="requirements"></a>Gereksinimler
 **Üst bilgi:** *FileTracker.h*