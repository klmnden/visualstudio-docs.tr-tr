---
title: IDebugTypeFieldBuilder2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugTypeFieldBuilder2 interface
ms.assetid: 23911c5b-2bbf-4734-9976-87a0bd6ea36c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b5fe9f0ba0182662a429cd7003caca5c48288309
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54955277"
---
# <a name="idebugtypefieldbuilder2"></a>IDebugTypeFieldBuilder2
Genişletir **IDebugTypeFieldBuilder** dizi türleri oluşturabilmek için.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugTypeFieldBuilder2 : IDebugTypeFieldBuilder  
```  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim, sembol Sağlayıcısı'ndan edinilebilir.  
  
## <a name="methods"></a>Yöntemler  
 Yöntemlere ek olarak [IDebugTypeFieldBuilder](../../../extensibility/debugger/reference/idebugtypefieldbuilder.md) arabirimi bu arabirim, aşağıdaki yöntemi uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[CreateArrayOfType](../../../extensibility/debugger/reference/idebugtypefieldbuilder2-createarrayoftype.md)|Belirtilen tür ve size bir dizi oluşturur.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll