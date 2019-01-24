---
title: SuspendTracking | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
api_name:
- SuspendTracking
api_location:
- filetracker.dll
api_type:
- COM
helpviewer_keywords:
- SuspendTracking
ms.assetid: f5e06e5a-8083-444c-99c1-07ba834226b5
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 91a72045e7e03a21bd827be1501251db823ca6ec
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54782551"
---
# <a name="suspendtracking"></a>SuspendTracking
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Geçerli bağlamda izleme askıya alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT WINAPI SuspendTracking(void);  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 [HRESULT] (<!-- TODO: review code entity reference <xref:assetId:///HRESULT?qualifyHint=False&amp;autoUpgrade=True>  -->) [başarılı] ile (<!-- TODO: review code entity reference <xref:assetId:///SUCCEEDED?qualifyHint=False&amp;autoUpgrade=True>  -->) izleme askıya alındı, biti ayarlanmamış.  
  
## <a name="requirements"></a>Gereksinimler  
 **Üst bilgi:** FileTracker.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ResumeTracking](../msbuild/resumetracking.md)
