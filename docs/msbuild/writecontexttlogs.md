---
title: WriteContextTLogs | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
apiname:
- WriteContextTLogs
apilocation:
- filetracker.dll
apitype: COM
helpviewer_keywords:
- WriteContextTLogs
ms.assetid: ffc6c7be-3f22-4624-9ffc-0122fe72b6ec
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3bde2d59bac380ca75fa8d5dcb8a1b6e5b98803e
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56598979"
---
# <a name="writecontexttlogs"></a>WriteContextTLogs
Geçerli bağlam için günlük dosyalarını yazar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT WINAPI WriteContextTLogs(LPCTSTR intermediateDirectory, LPCTSTR tlogRootName);
```

#### <a name="parameters"></a>Parametreler
- [in] `intermediateDirectory` İzleme günlüğünü depolanacağı dizin.

- [in] `tlogRootName` Günlük dosyası adı kök adı.

## <a name="return-value"></a>Dönüş değeri
 Bir **HRESULT** ile **başarılı** izleme bağlamına oluşturulduysa biti ayarlanmamış.

## <a name="requirements"></a>Gereksinimler
 **Üst bilgi:** *FileTracker.h*

## <a name="see-also"></a>Ayrıca bkz.
- [WriteAllTLogs](../msbuild/writealltlogs.md)