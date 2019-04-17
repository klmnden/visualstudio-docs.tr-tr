---
title: WriteAllTLogs | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
api_name:
- WriteAllTLogs
api_location:
- filetracker.dll
api_type:
- COM
helpviewer_keywords:
- WriteAllTLogs
ms.assetid: 1fa3e10b-263c-4960-a9ad-485c02a7a872
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 371357249bb9674a636859c995ad076eb41c2a08
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59656433"
---
# <a name="writealltlogs"></a>WriteAllTLogs
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Tüm iş parçacıkları ve Bağlamlar için izleme günlüklerini yazar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT WINAPI WriteAllTLogs(LPCTSTR intermediateDirectory, LPCTSTR tlogRootName);  
```  
  
#### <a name="parameters"></a>Parametreler  
 [in] `intermediateDirectory`  
 İzleme günlüğü depolanacağı dizin.  
  
 [in] `tlogRootName`  
 Günlük dosyası adı kök adı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir [HRESULT])<!-- TODO: review code entity reference <xref:assetId:///HRESULT?qualifyHint=False&amp;autoUpgrade=True>  -->) [başarılı] () ile<!-- TODO: review code entity reference <xref:assetId:///SUCCEEDED?qualifyHint=False&amp;autoUpgrade=True>  -->) izleme bağlamına oluşturulduysa biti ayarlanmamış.  
  
## <a name="requirements"></a>Gereksinimler  
 **Üst bilgi:** FileTracker.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [WriteContextTLogs](../msbuild/writecontexttlogs.md)
