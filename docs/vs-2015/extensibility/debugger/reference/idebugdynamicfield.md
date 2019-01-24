---
title: IDebugDynamicField | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugDynamicField
helpviewer_keywords:
- IDebugDynamicField interface
ms.assetid: caffbd95-7596-4714-84b1-b964e89a78bb
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 41cf0e397834f337863baa46abb4e6bbccee98ad
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54804881"
---
# <a name="idebugdynamicfield"></a>IDebugDynamicField
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, bir değişken türünü temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugDynamicField : IDebugField  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu arabirim, çalışma zamanında belirlenebilir herhangi bir türü için bir temel sınıf olarak sembol sağlayıcıları tarafından uygulanır. Yalnızca yönetilen kod için budur.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim, daha özel arabirimler türetilebilir temel bir sınıfı temsil eder.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Bu arabirim, devralınan dışındaki herhangi bir yöntem sağlamaz `IDebugField`.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sembol sağlayıcısı arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
