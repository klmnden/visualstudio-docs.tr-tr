---
title: StartTrackingContext | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
api_name:
- StartTrackingContext
api_location:
- filetracker.dll
api_type:
- COM
helpviewer_keywords:
- StartTrackingContext
ms.assetid: 720cd295-38e7-4974-86db-b8106b1207ba
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 3a23ea93cb1ca486b6804b778f7532ba4c39c900
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54802994"
---
# <a name="starttrackingcontext"></a>StartTrackingContext
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Bir izleme bağlamına başlayın.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT WINAPI StartTrackingContext(LPCTSTR intermediateDirectory, LPCTSTR taskName);  
```  
  
#### <a name="parameters"></a>Parametreler  
 [in] `intermediateDirectory`  
 İzleme günlüğü depolanacağı dizin.  
  
 [in] `taskName`  
 İzleme bağlamı tanımlar. Bu ad, günlük dosyası adı oluşturmak için kullanılır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 [HRESULT] (<!-- TODO: review code entity reference <xref:assetId:///HRESULT?qualifyHint=False&amp;autoUpgrade=True>  -->) [başarılı] ile (<!-- TODO: review code entity reference <xref:assetId:///SUCCEEDED?qualifyHint=False&amp;autoUpgrade=True>  -->) izleme bağlamına oluşturulduysa biti ayarlanmamış.  
  
## <a name="requirements"></a>Gereksinimler  
 **Üst bilgi:** FileTracker.h
