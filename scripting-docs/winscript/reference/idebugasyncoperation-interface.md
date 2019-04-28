---
title: Idebugasyncoperation arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugAsyncOperation interface
ms.assetid: ebb2ea75-1443-4d8a-812d-171a166f5f9d
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 820ecc40924ace4153b76f46c8b8fd1603512ebb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62821789"
---
# <a name="idebugasyncoperation-interface"></a>IDebugAsyncOperation Arabirimi
Hata ayıklama işlemi Yöneticisi uygulayan `IDebugAsyncOperation` arabirimi. Bir dil altyapısı çağırır `IDebugApplication::CreateAsyncDebugOperation` bu arabirim için bir başvuru almak için yöntemi. Dil altyapısı kullanabilirsiniz `IDebugAsyncOperation` bir zaman uyumlu hata ayıklama işlemi zaman uyumsuz erişim sağlamak için arabirim.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugAsyncOperation` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugAsyncOperation::GetSyncDebugOperation](../../winscript/reference/idebugasyncoperation-getsyncdebugoperation.md)|Bu nesneyle ilişkili zaman uyumlu hata ayıklama işlemi döndürür.|  
|[IDebugAsyncOperation::Start](../../winscript/reference/idebugasyncoperation-start.md)|Başlamak zaman uyumsuz işlem neden olur.|  
|[IDebugAsyncOperation::Abort](../../winscript/reference/idebugasyncoperation-abort.md)|Bir işlem iptal eder.|  
|[IDebugAsyncOperation::QueryIsComplete](../../winscript/reference/idebugasyncoperation-queryiscomplete.md)|Hata ayıklama işlemi tamamlandı belirler.|  
|[IDebugAsyncOperation::GetResult](../../winscript/reference/idebugasyncoperation-getresult.md)|Zaman uyumlu hata ayıklama işlemi dönüş nesne parametresi ve dönüş değeri sağlar.|