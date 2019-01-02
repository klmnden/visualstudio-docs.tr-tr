---
title: IDebugAlias::GetICorDebugValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugAlias::GetICorDebugValue
helpviewer_keywords:
- IDebugAlias::GetICorDebugValue method
ms.assetid: b9eb39ee-84af-4ace-9cfe-236b3d48aff5
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 941417adad62b7a09abc1515800a9200baf0bfcb
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53939048"
---
# <a name="idebugaliasgeticordebugvalue"></a>IDebugAlias::GetICorDebugValue
Bu diğer adla ilişkilendirilmiş değeri temsil eden bir yönetilen kod arabirim alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetICorDebugValue(  
   IUnknown** ppUnk  
);  
```  
  
```csharp  
int GetICorDebugValue(  
   out object ppUnk  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppUnk`  
 [out] `IUnknown` bu diğer adla ilişkilendirilmiş değeri temsil eden arabirim. Bu arabirim için sorgulanabilir `ICorDebugValue` arabirimi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem yalnızca yönetilen değerlere uygulanır ( `ICorDebugValue` arabirim kullanılabilir [!INCLUDE[dnprdnshort](../../../code-quality/includes/dnprdnshort_md.md)] ve tanımlanan [!INCLUDE[dnprdnshort](../../../code-quality/includes/dnprdnshort_md.md)] SDK cordebug.idl dosyasında).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md)