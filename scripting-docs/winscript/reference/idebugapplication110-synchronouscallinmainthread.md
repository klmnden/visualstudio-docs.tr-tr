---
title: IDebugApplication110::SynchronousCallInMainThread | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplication110::SynchronousCallInMainThread
ms.assetid: 57475ae5-1520-45ef-800d-ccfc6235a5d1
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d98f28f441096886c9ef7f26e63d876455a264e7
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63446370"
---
# <a name="idebugapplication110synchronouscallinmainthread"></a>IDebugApplication110::SynchronousCallInMainThread
Ana iş parçacığında zaman uyumlu bir çağrı yapar.  
  
> [!IMPORTANT]
> [Idebugapplication110 arabirimi](../../winscript/reference/idebugapplication110-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT SynchronousCallInMainThread([in] IDebugThreadCall* pptc, [in] DWORD_PTR dwParam1, [in] DWORD_PTR dwParam2, [in] DWORD_PTR dwParam3);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pptc`  
 [Idebugthreadcall arabirimi](../../winscript/reference/idebugthreadcall-interface.md) aranacak nesne.  
  
 `dwParam1`  
 Çağrısının ilk parametresi.  
  
 `dwParam1`  
 Çağrısının ilk parametresi.  
  
 `dwParam2`  
 Çağrı, ikinci parametre.  
  
 `dwParam3`  
 Çağrı'öğesinin üçüncü parametresi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplication110 Arabirimi](../../winscript/reference/idebugapplication110-interface.md)