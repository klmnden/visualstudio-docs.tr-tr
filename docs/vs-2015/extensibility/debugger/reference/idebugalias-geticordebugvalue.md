---
title: IDebugAlias::GetICorDebugValue | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugAlias::GetICorDebugValue
helpviewer_keywords:
- IDebugAlias::GetICorDebugValue method
ms.assetid: b9eb39ee-84af-4ace-9cfe-236b3d48aff5
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 67ab8a7343cd320470515b757dfca905a0a4690e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68156287"
---
# <a name="idebugaliasgeticordebugvalue"></a>IDebugAlias::GetICorDebugValue
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

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
 Bu yöntem yalnızca yönetilen değerlere uygulanır ( `ICorDebugValue` arabirim kullanılabilir [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] ve tanımlanan [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] SDK cordebug.idl dosyasında).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md)
