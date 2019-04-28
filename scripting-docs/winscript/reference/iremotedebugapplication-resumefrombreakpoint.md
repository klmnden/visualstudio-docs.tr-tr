---
title: IRemoteDebugApplication::ResumeFromBreakPoint | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IRemoteDebugApplication.ResumeFromBreakPoint
apilocation:
- pdm.dll
helpviewer_keywords:
- IRemoteDebugApplication::ResumeFromBreakPoint
ms.assetid: a613cc2b-1d69-4713-a235-64372c253b4a
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5844381188cb03c99ab0a44ed9b9e0fdbab67e6e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62944165"
---
# <a name="iremotedebugapplicationresumefrombreakpoint"></a>IRemoteDebugApplication::ResumeFromBreakPoint
Bir kesme noktasına şu anda bir uygulama devam eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT ResumeFromBreakPoint(  
   IRemoteDebugApplicationThread*  prptFocus,  
   BREAKRESUMEACTION               bra,  
   ERRORRESUMEACTION               era  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `prptFocus`  
 [in] Atlama modu tarafından etkilendiği için olan iş parçacığı modları, atlamak için.  
  
 `bra`  
 [in] Uygulama sürdürdükten gerçekleştirilecek eylem.  
  
 `era`  
 [in] Uygulama bir hata nedeniyle durduruldu durumunda gerçekleştirilecek eylem.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bir kesme noktasına şu anda bir uygulama devam eder.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iremotedebugapplication arabirimi](../../winscript/reference/iremotedebugapplication-interface.md)   
 [BREAKRESUMEACTION numaralandırması](../../winscript/reference/breakresumeaction-enumeration.md)   
 [ERRORRESUMEACTION Sabit Listesi](../../winscript/reference/errorresumeaction-enumeration.md)