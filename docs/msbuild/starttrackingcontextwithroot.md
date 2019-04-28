---
title: StartTrackingContextWithRoot | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
apiname:
- StartTrackingContextWithRoot
apilocation:
- filetracker.dll
apitype: COM
helpviewer_keywords:
- StartTrackingContextWithRoot
ms.assetid: f6ef2b76-8035-4a14-8195-aa221c46ef48
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 53f2c1ebd5896eaa8a4b9d5ff4e5cb7856a1f8e2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62939111"
---
# <a name="starttrackingcontextwithroot"></a>StartTrackingContextWithRoot
Bir kök işaret belirten bir yanıt dosyası kullanarak bir izleme bağlamına başlatır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT WINAPI StartTrackingContextWithRoot(LPCTSTR intermediateDirectory, LPCTSTR taskName, LPCTSTR rootMarkerResponseFile);
```

#### <a name="parameters"></a>Parametreler
[in] `intermediateDirectory`

 İzleme günlüğü depolanacağı dizin.

[in] `taskName`

 İzleme bağlamı tanımlar. Bu ad, günlük dosyası adı oluşturmak için kullanılır.

[in] `rootMarkerResponseFile`

 Bir kök işaret içeren bir yanıt dosyasının yol adı. Kök adı, tüm izleme için bir bağlam birlikte gruplandırmak için kullanılır.

## <a name="return-value"></a>Dönüş değeri
 Bir **HRESULT** ile **başarılı** izleme bağlamına oluşturulduysa biti ayarlanmamış.

## <a name="requirements"></a>Gereksinimler
 **Üst bilgi:** *FileTracker.h*

## <a name="see-also"></a>Ayrıca bkz.
- [StartTrackingContext](../msbuild/starttrackingcontext.md)