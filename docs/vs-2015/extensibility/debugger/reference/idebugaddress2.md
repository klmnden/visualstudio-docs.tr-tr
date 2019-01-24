---
title: IDebugAddress2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugAddress2
helpviewer_keywords:
- IDebugAddress2 interface
ms.assetid: b150e0ed-4ac0-4f8c-9732-4b3e54b9d243
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 23fb27643a209e870165e521d63079a3b6c650eb
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54765668"
---
# <a name="idebugaddress2"></a>IDebugAddress2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirimi bu arabirim tarafından temsil edilen nesnenin adresini sahibi işlem kimliğine erişim sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugAddress2 : IDebugAddress  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Sembol sağlayıcısı bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi. Bu arabirim, bu adrese ilgili nesnenin sahibi olan işlem kimliğine erişim sağlar.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Kullanım [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) bu arabirimden edinme [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi.  
  
## <a name="methods-in-vtable-order"></a>Sipariş vtable'da yöntemleri  
 Devralınan yöntemleri yanı sıra [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi bu arabirim, aşağıdaki yöntemi uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetProcessID](../../../extensibility/debugger/reference/idebugaddress2-getprocessid.md)|Bu arabirim tarafından temsil edilen nesnenin sahibi olan işlemin Kimliğini alır.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sembol sağlayıcısı arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)
