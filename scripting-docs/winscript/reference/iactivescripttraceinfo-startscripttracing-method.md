---
title: Iactivescripttraceınfo::startscripttracing yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 90fac5ed-ce15-49b7-a6f1-605ede6f34e2
caps.latest.revision: 3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6462597f55b6b0ceee885d207572e9669a350600
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54093650"
---
# <a name="iactivescripttraceinfostartscripttracing-method"></a>IActiveScriptTraceInfo::StartScriptTracing Yöntemi
Betik izleme başlatır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT StartScriptTracing(     [in] IActiveScriptSiteTraceInfo * pSiteTraceInfo,     [in] GUID guidContextID );   
```  
  
#### <a name="parameters"></a>Parametreler  
 `pSiteTraceInfo`  
 Ana bilgisayarın Iactivescriptsitetraceınfo işaretçisi.  
  
 `guidContextId`  
 Bağlam GUID.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bu yöntemin dönüş olası değerler şunlardır:  
  
1.  S_OK: Başarılı.  
  
2.  E_poınter: `pSiteTraceInfo` bir NULL işaretçidir.  
  
3.  E_NOTIMPL: Henüz uygulanmadı.