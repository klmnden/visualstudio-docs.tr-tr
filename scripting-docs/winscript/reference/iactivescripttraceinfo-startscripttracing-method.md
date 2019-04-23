---
title: Iactivescripttraceınfo::startscripttracing yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 90fac5ed-ce15-49b7-a6f1-605ede6f34e2
caps.latest.revision: 3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b87971e1fd2e484aa54ff4de56ee56e00b19b1e6
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60101021"
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
  
1. S_OK: Başarılı.  
  
2. E_poınter: `pSiteTraceInfo` bir NULL işaretçidir.  
  
3. E_NOTIMPL: Henüz uygulanmadı.