---
title: IActiveScriptProfilerControl2::PrepareProfilerStop | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptProfilerControl2::PrepareProfilerStop
ms.assetid: e43a63bc-c44f-44a8-9db4-29062b9e6a16
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 11a32f36ec6eddcc06faa77e093f19e8df503fa4
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58149321"
---
# <a name="iactivescriptprofilercontrol2prepareprofilerstop"></a>IActiveScriptProfilerControl2::PrepareProfilerStop
Profil Oluşturucu, tüm geçerli komut dosyası motorlarına profil oluşturmayı durdurmak için önerilere şu bildirir. Bu yöntemi kullanarak, tam çağrı yığınını edinebilirsiniz [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] profil oluşturma durdurduğunuzda çalışıyor.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT PrepareProfilerStop();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Yöntem herhangi bir parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 HRESULT döndürür. Olası değerler aşağıdaki gibidir:  
  
|Dönüş değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_FAIL`|Profil oluşturma başlatılamıyor.|  
|`S_FALSE`|Profil oluşturma, bir komut dosyası değil çalıştırılırken durduruldu.|  
|`ACTIVPROF_E_PROFILER_ABSENT`|Profil oluşturma etkin değil.|  
  
## <a name="remarks"></a>Açıklamalar  
 Çağırma `IActiveScriptProfilerControl2::PrepareProfilerStop` çağrı yığınındaki işlevler için olayları gönderilmesini sağlar. Bu yöntem, geçerli sekmesinde herhangi bir komut dosyası altyapısını profil oluşturmayı durdurmak önce çağrılacak sahiptir. Yöntem herhangi bir komut dosyası altyapısı için çağrılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptProfilerControl2::CompleteProfilerStart](../../winscript/reference/iactivescriptprofilercontrol2-completeprofilerstart.md)   
 [IActiveScriptProfilerControl2 Arabirimi](../../winscript/reference/iactivescriptprofilercontrol2-interface.md)