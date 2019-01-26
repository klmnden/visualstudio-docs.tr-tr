---
title: IDebugProcess2::CauseBreak | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProcess2::CauseBreak
helpviewer_keywords:
- IDebugProcess2::CauseBreak
ms.assetid: efda8865-2319-4d53-90bf-6d9d74cd5195
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9e74f8b64dd2cd9b15a215d6cc7c051bee92bf3f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54958062"
---
# <a name="idebugprocess2causebreak"></a>IDebugProcess2::CauseBreak
Sonraki diğer bir deyişle bu işlemde çalışan kod program isteklerini durdurmak ve gönderme bir [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md) olay nesnesi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT CauseBreak(   
   void  
);  
```  
  
```csharp  
int CauseBreak();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)