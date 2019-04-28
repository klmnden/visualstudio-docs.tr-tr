---
title: Ijsdebugprocess::createbreakpoint yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugProcess.CreateBreakPoint
apilocation:
- jscript9diag.dll
ms.assetid: a2cb4233-2846-4d11-aa13-21de43abda9f
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b398b93c2e7b5ad43abd35d385407b39c0c980f9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62557978"
---
# <a name="ijsdebugprocesscreatebreakpoint-method"></a>IJsDebugProcess::CreateBreakPoint Yöntemi
Belge belirtilen konumda bir kesme noktası ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CreateBreakPoint(  
   UINT64 documentId,  
   DWORD characterOffset,  
   DWORD characterCount,  
   BOOL isEnabled,  
   IJsDebugBreakPoint **ppDebugBreakPoint  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `documentId`  
 [in] Idebugdocumenttext öğesine işaretçi.  
  
 `characterOffset`  
 [in] Dosyanın başından itibaren karakter uzaklığı.  
  
 `characterCount`  
 [in] İçinde kesme noktasının ekleneceği belge metninin uzunluğu.  
  
 `isEnabled`  
 [in] Kesme noktasının etkinleştirilip etkinleştirilmeyeceğini belirtir.  
  
 `ppDebugBreakPoint`  
 [out] Oluşturulan kesme noktasını temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugProcess Arabirimi](../../winscript/reference/ijsdebugprocess-interface.md)