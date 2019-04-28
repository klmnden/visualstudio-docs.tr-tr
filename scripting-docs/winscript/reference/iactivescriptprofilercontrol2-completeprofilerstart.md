---
title: IActiveScriptProfilerControl2::CompleteProfilerStart | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptProfilerControl2::CompleteProfilerStart
ms.assetid: e14d94a2-39d3-40a1-84d9-6300fbe2b339
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 36a1f5d6a1401e2860b65a29c8e383627e83c6be
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62993030"
---
# <a name="iactivescriptprofilercontrol2completeprofilerstart"></a>IActiveScriptProfilerControl2::CompleteProfilerStart
Profil Oluşturucu, tüm geçerli komut dosyası motorlarına profil oluşturma başlatıldı bildirir. Bu yöntemi kullanarak, tam çağrı yığınını edinebilirsiniz [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] profil oluşturma işlemini başlattığınızda çalışıyor.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CompleteProfilerStart();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Yöntem herhangi bir parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 HRESULT döndürür. Olası değerler aşağıdaki gibidir:  
  
|Dönüş değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_FAIL`|Profil oluşturma başlatılamaz.|  
|`S_FALSE`|Bir komut dosyası değil çalıştırılırken, profil oluşturma başlatıldı.|  
|`ACTIVPROF_E_PROFILER_ABSENT`|Profil oluşturma etkin değil. Hiçbir geri çağırma ayarlandı.|  
|`E_OUTOFMEMORY`|Bir bellek yetersiz durum nedeniyle çağrı yığını alınamıyor.|  
  
## <a name="remarks"></a>Açıklamalar  
 Çağırma `IActiveScriptProfilerControl2::CompleteProfilerStart` zaten çağrı yığınındaki işlevler için olayları gönderilmesini sağlar. Bu yöntem, geçerli sekmesinde herhangi bir komut dosyası altyapısı başlangıçlara profil oluşturduktan sonra çağrılacak sahiptir. Yöntem herhangi bir komut dosyası altyapısı için çağrılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptProfilerControl2::PrepareProfilerStop](../../winscript/reference/iactivescriptprofilercontrol2-prepareprofilerstop.md)   
 [IActiveScriptProfilerControl2 Arabirimi](../../winscript/reference/iactivescriptprofilercontrol2-interface.md)