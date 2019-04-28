---
title: IDebugApplicationThreadEvents110::OnSuspendForBreakPoint | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationThreadEvents110::OnSuspendForBreakPoint
ms.assetid: 224245ac-2aa2-43ae-97ed-493afc3d0122
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a9e39af9784b139e935c271fca6db565136352cf
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63440430"
---
# <a name="idebugapplicationthreadevents110onsuspendforbreakpoint"></a>IDebugApplicationThreadEvents110::OnSuspendForBreakPoint
İş parçacığı bir kesme noktası için tam olarak askıya aldı ve henüz normal yürütmenin ettirdi değil olup olmadığını belirler.  
  
> [!IMPORTANT]
> [Idebugapplicationthreadevents110 arabirimi](../../winscript/reference/idebugapplicationthreadevents110-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT OnSuspendForBreakPoint( void );  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem, hiç parametre yok.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplicationThreadEvents110 Arabirimi](../../winscript/reference/idebugapplicationthreadevents110-interface.md)