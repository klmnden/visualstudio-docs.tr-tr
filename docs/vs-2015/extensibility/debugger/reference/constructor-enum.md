---
title: CONSTRUCTOR_ENUM | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- CONSTRUCTOR_ENUM
helpviewer_keywords:
- CONSTRUCTOR_ENUM enumeration
ms.assetid: 6d335b2c-66bc-460c-a4a6-4f3f1b697c2c
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6259f5cd5dce142364d455478a16e56e90116823
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49171671"
---
# <a name="constructorenum"></a>CONSTRUCTOR_ENUM
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Farklı türlerde oluşturucular seçer.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
typedef enum ConstructorMatchOptions {   
   crAll       = 0,  
   crNonStatic = 1,  
   crStatic    = 2  
} CONSTRUCTOR_ENUM;  
```  
  
```csharp  
public enum ConstructorMatchOptions {   
   crAll       = 0,  
   crNonStatic = 1,  
   crStatic    = 2  
};  
```  
  
## <a name="members"></a>Üyeler  
 crAll  
 Tüm oluşturucular seçer.  
  
 crNonStatic  
 Statik olmayan oluşturucular seçer.  
  
 crStatic  
 Statik oluşturucular seçer.  
  
## <a name="remarks"></a>Açıklamalar  
 Bağımsız değişken olarak geçirilen [EnumConstructors](../../../extensibility/debugger/reference/idebugclassfield-enumconstructors.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md)

