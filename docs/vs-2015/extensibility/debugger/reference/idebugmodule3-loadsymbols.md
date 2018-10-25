---
title: IDebugModule3::LoadSymbols | Microsoft Docs
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
- IDebugModule3::LoadSymbols
helpviewer_keywords:
- IDebugModule3::LoadSymbols
ms.assetid: 7548c8c1-cbc6-48aa-a845-19058d4a85bb
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1f40970f3ced7a40512d4b9ce61d1b33c46477a9
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49816553"
---
# <a name="idebugmodule3loadsymbols"></a>IDebugModule3::LoadSymbols
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Geçerli modül için sembolleri yükler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT LoadSymbols(  
   void  
);  
```  
  
```csharp  
int LoadSymbols();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem başarılı olursa, döndürür `S_OK`. Başarısız olursa hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem geçerli bir arama yolundan sembolleri yükler (hangi değiştirilebilir çağırarak [SetSymbolPath](../../../extensibility/debugger/reference/idebugengine3-setsymbolpath.md) yöntemi).  
  
 Bu yöntem üzerinden tercih edilen [ReloadSymbols_Deprecated](../../../extensibility/debugger/reference/idebugmodule2-reloadsymbols-deprecated.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugModule3](../../../extensibility/debugger/reference/idebugmodule3.md)   
 [SetSymbolPath](../../../extensibility/debugger/reference/idebugengine3-setsymbolpath.md)

