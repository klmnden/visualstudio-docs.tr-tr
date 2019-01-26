---
title: IDebugGenericParamField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugGenericParamField interface
ms.assetid: ba24f499-5ba7-4c67-83e6-923229b52327
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e7cc68af4d5b53a36e9affc038951e2be63de90f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54954624"
---
# <a name="idebuggenericparamfield"></a>IDebugGenericParamField
Yönetilen kod genel bir tür için bir parametreyi temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugGenericParamField : IDebugField  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Genel türler için destek kullanılır.  
  
## <a name="methods"></a>Yöntemler  
 Yöntemlere ek olarak [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) arabirimi bu arabirim, aşağıdaki yöntemleri uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[ConstraintCount](../../../extensibility/debugger/reference/idebuggenericparamfield-constraintcount.md)|Bu genel parametre ile ilişkili olan kısıtlamaları sayısını döndürür.|  
|[GetConstraints](../../../extensibility/debugger/reference/idebuggenericparamfield-getconstraints.md)|Bu genel parametre ile ilişkili olan kısıtlamaları alır.|  
|[GetFlags](../../../extensibility/debugger/reference/idebuggenericparamfield-getflags.md)|Bu genel parametresi için bayrakları alır.|  
|[GetIndex](../../../extensibility/debugger/reference/idebuggenericparamfield-getindex.md)|Bu genel parametre dizinini alır.|  
|[GetNameOfFormalParam](../../../extensibility/debugger/reference/idebuggenericparamfield-getnameofformalparam.md)|Bu genel parametre adını alır.|  
|[GetOwner](../../../extensibility/debugger/reference/idebuggenericparamfield-getowner.md)|Bu genel parametre türü veya yönteminde sahibi alır.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll