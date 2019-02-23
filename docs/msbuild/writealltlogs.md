---
title: WriteAllTLogs | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
apiname:
- WriteAllTLogs
apilocation:
- filetracker.dll
apitype: COM
helpviewer_keywords:
- WriteAllTLogs
ms.assetid: 1fa3e10b-263c-4960-a9ad-485c02a7a872
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ee3f02be5494f85c0fa36be510f0a0c25caf53b6
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56704325"
---
# <a name="writealltlogs"></a>WriteAllTLogs
Tüm iş parçacıkları ve Bağlamlar için izleme günlüklerini yazar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT WINAPI WriteAllTLogs(LPCTSTR intermediateDirectory, LPCTSTR tlogRootName);
```

#### <a name="parameters"></a>Parametreler
[in] `intermediateDirectory`

 İzleme günlüğü depolanacağı dizin.

[in] `tlogRootName`

 Günlük dosyası adı kök adı.

## <a name="return-value"></a>Dönüş değeri
 Bir **HRESULT** ile **başarılı** izleme bağlamına oluşturulduysa biti ayarlanmamış.

## <a name="requirements"></a>Gereksinimler
 **Üst bilgi:** *FileTracker.h*

## <a name="see-also"></a>Ayrıca bkz.
- [WriteContextTLogs](../msbuild/writecontexttlogs.md)