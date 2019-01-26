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
ms.openlocfilehash: 026fb2dedbfb67aa64c1a8e074e8c4017f9e69aa
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54955810"
---
# <a name="writecontexttlogs"></a>WriteContextTLogs
Geçerli bağlam için günlük dosyalarını yazar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT WINAPI WriteContextTLogs(LPCTSTR intermediateDirectory, LPCTSTR tlogRootName);  
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
 [WriteAllTLogs](../msbuild/writealltlogs.md)