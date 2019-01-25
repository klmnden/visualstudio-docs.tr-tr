---
title: IDebugEngineLaunch2::CanTerminateProcess | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugEngineLaunch2::CanTerminateProcess
helpviewer_keywords:
- IDebugEngineLaunch2::CanTerminateProcess
ms.assetid: 7973454d-c957-4123-a0ee-80ebcdbbd2d1
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c46332f024f883183e4fa10321e1ecdcc8961c69
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54755986"
---
# <a name="idebugenginelaunch2canterminateprocess"></a>IDebugEngineLaunch2::CanTerminateProcess
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir işlemin sona erdirilecek belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT CanTerminateProcess (   
   IDebugProcess2* pProcess  
);  
```  
  
```csharp  
int CanTerminateProcess (   
   IDebugProcess2 pProcess  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pProcess`  
 [in] Bir [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) sonlandırılacak işlemi temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `S_FALSE` erişim reddedildiğinden altyapısı işlem, örneğin, sonlandırılamadı durumunda.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem döndürürse `S_OK`, ardından bunu [TerminateProcess](../../../extensibility/debugger/reference/idebugenginelaunch2-terminateprocess.md) yöntemi, aslında işlemi sonlandırmak için çağrılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugEngineLaunch2](../../../extensibility/debugger/reference/idebugenginelaunch2.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [TerminateProcess](../../../extensibility/debugger/reference/idebugenginelaunch2-terminateprocess.md)
