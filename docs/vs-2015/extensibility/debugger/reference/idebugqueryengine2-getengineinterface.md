---
title: IDebugQueryEngine2::GetEngineInterface | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugQueryEngine2::GetEngineInterface
helpviewer_keywords:
- IDebugQueryEngine2::GetEngineInterface
ms.assetid: ed84aa98-7ec7-48f3-97ae-821090bc3664
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 12bdcf9de9731095a224f394cab13f3833f126de
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68158119"
---
# <a name="idebugqueryengine2getengineinterface"></a>IDebugQueryEngine2::GetEngineInterface
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Özel hata ayıklama altyapısı (DE) arabirimini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetEngineInterface(   
   IUnknown** ppUnk  
);  
```  
  
```csharp  
int GetEngineInterface(   
   out object ppUnk  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppUnk`  
 [out] Döndürür bir `IUnknown` hata ayıklama altyapısı (DE) ve hangi bir DE ile ilişkili diğer herhangi bir geçerli arabirimi için sorgulanabilir nesnesini temsil eder (örneğin [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md) veya [IDebugEngineLaunch2](../../../extensibility/debugger/reference/idebugenginelaunch2.md)).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Arama Bu yöntemden alınan arabirimler üzerinden oturum hata ayıklama manager'ın işleme bozar ve hatalı bir duruma alma veya hata ayıklama sırasında hatalar üretme SDM neden olabilir çünkü elde edilen arabirimi dikkatli kullanılmalıdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugQueryEngine2](../../../extensibility/debugger/reference/idebugqueryengine2.md)   
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)   
 [IDebugEngineLaunch2](../../../extensibility/debugger/reference/idebugenginelaunch2.md)
