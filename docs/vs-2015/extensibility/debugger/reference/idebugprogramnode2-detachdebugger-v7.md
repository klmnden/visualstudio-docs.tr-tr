---
title: IDebugProgramNode2::DetachDebugger_V7 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProgramNode2::DetachDebugger
helpviewer_keywords:
- IDebugProgramNode2::DetachDebugger
- IDebugProgramNode2::DetachDebugger_V7
ms.assetid: d2d4b78e-a2dd-4217-97a6-ab648fd2ee2f
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: cbca803b7caaef3e5a5ae4cbc46fc8e850a1575b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54771519"
---
# <a name="idebugprogramnode2detachdebuggerv7"></a>IDebugProgramNode2::DetachDebugger_V7
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

KULLANIM DIŞI. KULLANMAYIN.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT DetachDebugger_V7 (   
   void   
);  
```  
  
```csharp  
int DetachDebugger_V7 ();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir uygulama her zaman döndürmelidir `E_NOTIMPL`.  
  
## <a name="remarks"></a>Açıklamalar  
  
> [!WARNING]
>  Sürümünden itibaren [!INCLUDE[vsprvslong](../../../includes/vsprvslong-md.md)], bu yöntem artık kullanılmamaktadır ve her zaman döndürmelidir `E_NOTIMPL`.  
  
 Hata ayıklayıcı beklenmedik şekilde sona erdiğinde, bu yöntem çağrılır. Bu yöntem çağrıldığında, kullanıcı CİHAZDAN ayrılmış gibi sorgulamanıza DE programın devam edecektir. Daha fazla hata ayıklama olay gönderilmelidir. Programın başka bir hata ayıklayıcı örneğinden iliştirilebilir olduğu bir durumda olması gerekir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)
