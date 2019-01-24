---
title: IDebugProgramNode2::GetHostMachineName_V7 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProgramNode2::GetHostMachineName
helpviewer_keywords:
- IDebugProgramNode2::GetHostMachineName_V7
- IDebugProgramNode2::GetHostMachineNameIDebugProgramNode2::GetHostMachineName
ms.assetid: a992f2c9-f68b-4146-8cc2-027753bf7ce6
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ac639798ae5d1016b7d1c04753b6e0e758a7fe17
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54771546"
---
# <a name="idebugprogramnode2gethostmachinenamev7"></a>IDebugProgramNode2::GetHostMachineName_V7
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

KULLANIM DIŞI. KULLANMAYIN.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetHostMachineName_V7 (   
   BSTR* pbstrHostMachineName  
);  
```  
  
```csharp  
int GetHostMachineName_V7 (   
   out string pbstrHostMachineName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pbstrHostMachineName`  
 [out] Programın çalıştığı bilgisayarın adını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir uygulama her zaman döndürmelidir `E_NOTIMPL`.  
  
## <a name="remarks"></a>Açıklamalar  
  
> [!WARNING]
>  Sürümünden itibaren [!INCLUDE[vsprvslong](../../../includes/vsprvslong-md.md)], bu yöntem artık kullanılmamaktadır ve her zaman döndürmelidir `E_NOTIMPL`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)
