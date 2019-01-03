---
title: IDebugGenericFieldInstance | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugGenericFieldInstance interface
ms.assetid: f68b4761-be8b-4801-9d4b-cde90e01d95e
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 9c265591d1836594b9190e031c1bfe3ab5a93813
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53990983"
---
# <a name="idebuggenericfieldinstance"></a>IDebugGenericFieldInstance
Yönetilen kod genel bir tür için bir alan örneğini temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugGenericFieldInstance : IUnknown  
```  
  
## <a name="methods"></a>Yöntemler  
 Bu arabirim, aşağıdaki yöntemleri uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetTypeArguments](../../../extensibility/debugger/reference/idebuggenericfieldinstance-gettypearguments.md)|Bu örneğin tür parametresi bağımsız değişkenlerini alır.|  
|[TypeArgumentCount](../../../extensibility/debugger/reference/idebuggenericfieldinstance-typeargumentcount.md)|Bu örnek için parametre bağımsız değişkenlerini türünün sayısını döndürür.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll