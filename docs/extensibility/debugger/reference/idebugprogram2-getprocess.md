---
title: IDebugProgram2::GetProcess | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::GetProcess
helpviewer_keywords:
- IDebugProgram2::GetProcess
ms.assetid: 1d602485-ebaf-451c-9165-f2e226f20a90
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b1dcfc207a485a3b1eb5ec24930f613692fac69e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54962988"
---
# <a name="idebugprogram2getprocess"></a>IDebugProgram2::GetProcess
Bu programı çalıştırmayı işlem alın.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetProcess(  
   IDebugProcess2** ppProcess  
);  
```  
  
```csharp  
int GetProcess(  
   out IDebugProcess2 ppProcess  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppProcess`  
 [out] Döndürür [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) işlemi temsil eden arabirim.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklama altyapısı (DE) uygulayan sürece [IDebugEngineLaunch2](../../../extensibility/debugger/reference/idebugenginelaunch2.md) arabirimi, bu yöntemin DE'ın kullanımı döndürmelidir her zaman `E_NOTIMPL` bir DE buna ve bu nedenle çalıştırdığı işlemi yapamazsınız belirleyemediğinden Bu yöntemin bir uygulaması, karşılar.  
  
 Uygulama `IDebugEngineLaunch2` arabirimi anlamına gelir; işlem oluşturma DE bilmeniz gerekir bu nedenle DE'ın uygulaması [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) arabirimi içinde çalıştığı hangi işlemin bilmeniz mümkün.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IDebugEngineLaunch2](../../../extensibility/debugger/reference/idebugenginelaunch2.md)