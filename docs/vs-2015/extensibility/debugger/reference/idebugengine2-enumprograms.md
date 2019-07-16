---
title: IDebugEngine2::EnumPrograms | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugEngine2::EnumPrograms
helpviewer_keywords:
- IDebugEngine2::EnumPrograms
ms.assetid: 56bf98eb-beec-4e5f-9ebe-46c922e54c56
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: dc004de59b6ae219f47dc0874913c8e6e6ceb0f5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68196002"
---
# <a name="idebugengine2enumprograms"></a>IDebugEngine2::EnumPrograms
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir hata ayıklama altyapısı (DE) ayıklanan bütün programların bir listesini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT EnumPrograms(   
   IEnumDebugPrograms2** ppEnum  
);  
```  
  
```csharp  
int EnumPrograms(   
   out IEnumDebugPrograms2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppEnum`  
 [out] Döndürür bir [IEnumDebugPrograms2](../../../extensibility/debugger/reference/ienumdebugprograms2.md) tarafından bir DE ayıklanan bütün programların listesini içeren nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)   
 [IEnumDebugPrograms2](../../../extensibility/debugger/reference/ienumdebugprograms2.md)
