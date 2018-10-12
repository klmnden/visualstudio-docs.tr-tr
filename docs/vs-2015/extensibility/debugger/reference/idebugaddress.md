---
title: IDebugAddress | Microsoft Docs
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
- IDebugAddress
helpviewer_keywords:
- IDebugAddress interface
ms.assetid: bc709ff7-4966-4f36-9af2-690efe2cea1d
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b620dfe22c16842b2bc887e669db45c86f6c4948
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49277036"
---
# <a name="idebugaddress"></a>IDebugAddress
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, bir öğenin adresi temsil eder. Bu sembol işleyici tarafından döndürülür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugAddress : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Sembol sağlayıcısı, bir nesnenin bir adresi temsil etmek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Birçok yöntemlerde pek çok arabirimi bu arabirim döndürür.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Bu arabirim, aşağıdaki yöntemi uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetAddress](../../../extensibility/debugger/reference/idebugaddress-getaddress.md)|Alır bir [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) yapısı, konumu ve bir nesne tanımlayan.|  
  
## <a name="remarks"></a>Açıklamalar  
 Sembol sağlayıcısı, bir nesne ve konumuna (örneğin, işlev, yöntemi veya sınıf) belirli bir kapsam içinde temsil etmek için bu arabirimi döndürür. Bu arabirim döndürüldüğü ve sembol sağlayıcısı ve ifade çeşitli yöntemlere geçirilen değerlendiricisi. Normalde, sembol sağlayıcısı bu arabirimi içeriğini yorumlamak için gereken tek varlıktır.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sembol sağlayıcısı arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)

