---
title: IActiveScriptProfilerControl::StartProfiling | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptProfilerControl.StartProfiling
apilocation:
- scrobj.dll
ms.assetid: 56a7b3b7-8c21-43d0-9d8b-53bbc19fabb9
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 780886e4ca21abbe11580992244cee0d6a28b134
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62993143"
---
# <a name="iactivescriptprofilercontrolstartprofiling"></a>IActiveScriptProfilerControl::StartProfiling
Komut dosyası altyapısına'profil oluşturmaya başlar. Komut dosyası altyapısı bir çağrı yaparak profil oluşturucu nesnesinin örneğini oluşturur. [CoCreateInstance](https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT StartProfiling(  
    [in] REFCLSID clsidProfilerObject,  
    [in] DWORD dwEventMask,  
    [in] DWORD dwContext);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `clsidProfilerObject`  
 [in] Oluşturulacak profil oluşturucu nesne tanımlayıcısı (CLSID) sınıfı.  
  
 `dwEventMask`  
 [in] Olay türlerini belirten bir 4 baytlık bit maskesi. BITS tanımlanan [profıler_event_mask numaralandırması](../../winscript/reference/profiler-event-mask-enumeration.md).  
  
 `dwContext`  
 [in] Profil Oluşturucu nesnesine geçirilen bir 4 baytlık değer.  
  
## <a name="return-value"></a>Dönüş Değeri  
 HRESULT döndürür. Olası değerler aşağıdaki gibidir:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`ACTIVPROF_E_PROFILER_PRESENT`|Profil oluşturma zaten etkin.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptProfilerControl Arabirimi](../../winscript/reference/iactivescriptprofilercontrol-interface.md)