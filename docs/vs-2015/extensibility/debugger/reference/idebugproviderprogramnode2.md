---
title: IDebugProviderProgramNode2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProviderProgramNode2
helpviewer_keywords:
- IDebugProviderProgramNode2
ms.assetid: f0bca1cc-afbe-44cf-b5aa-d078aa685d24
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ca5027acbc985ee9afcd8ecd4cf67d2adca40d66
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54757083"
---
# <a name="idebugproviderprogramnode2"></a>IDebugProviderProgramNode2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, işlem sınırları ötesinde programı ilişkili arabirimleri sürekliliğe devreder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProviderProgramNode2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE) bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) hazırlama arabirimleri arasında işlem sınırları desteklemek için.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Çağrı [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) üzerinde bir `IDebugProgramNode2` arabirimi bu arabirim elde edilir. Bu arabirim alınamıyorsa DE arabirimleri sıralama desteklemez.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Bu arabirim, aşağıdaki yöntemi uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[UnmarshalDebuggeeInterface](../../../extensibility/debugger/reference/idebugproviderprogramnode2-unmarshaldebuggeeinterface.md)|Belirtilen bir arabirim işlem sınırları alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim DE ayıklanan programın ayrı işlem alanında çalıştırıldığında uygulanır: Örneğin, DE çalışırken hata ayıklanan programa işlem alanına yerine Visual Studio işlem alanında.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)
