---
title: Idebugsyncoperation arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugSyncOperation interface
ms.assetid: 8d714492-1836-462c-980a-c99e91a2c81b
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7184be62a8ad2b65e81d1ad82f01f0ce3f4668c5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63004887"
---
# <a name="idebugsyncoperation-interface"></a>IDebugSyncOperation Arabirimi
Belirli bir engellenmiş iş parçacığı, iç içe geçmiş sırada gerçekleştirilmesi gerekir (örneğin, ifade değerlendirme için) bir işlem soyutlamak bir komut dosyası altyapısı sağlar. Arabirimin de yanıt vermeyen işlemleri iptal etmek için bir mekanizma sağlar.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugSyncOperation` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugSyncOperation::GetTargetThread](../../winscript/reference/idebugsyncoperation-gettargetthread.md)|Bu eşzamanlı bir işlem için hedef uygulama iş parçacığı döndürür.|  
|[IDebugSyncOperation::Execute](../../winscript/reference/idebugsyncoperation-execute.md)|Zaman uyumlu işlem gerçekleştirir ve döndürür.|  
|[IDebugSyncOperation::InProgressAbort](../../winscript/reference/idebugsyncoperation-inprogressabort.md)|Bir başka bir iş parçacığı üzerinde devam eden işlemi iptal eder.|