---
title: IDebugProgramNodeAttach2::OnAttach | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProgramNodeAttach2::OnAttach
helpviewer_keywords:
- IDebugProgramNodeAttach2::OnAttach
ms.assetid: 5fe52761-a508-4ab5-abdb-334fb6590334
caps.latest.revision: 4
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 845ec66215c5d999aaf3b5c9658bc0fb8e7295a7
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54779436"
---
# <a name="idebugprogramnodeattach2onattach"></a>IDebugProgramNodeAttach2::OnAttach
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

İlişkili programına iliştirir veya ekleme işlemi için erteler [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT OnAttach(  
   [in] REFGUID guidProgramId  
);  
```  
  
```csharp  
int OnAttach(  
   ref Guid guidProgramId  
};  
```  
  
#### <a name="parameters"></a>Parametreler  
 `guidProgramId`  
 [in] `GUID` ilişkili programına atamak için.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi çağırılmalıdır. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem ekleme işlemi sırasında önce çağrılır [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi çağrılır. `OnAttach` Yöntemi ekleme işlemi gerçekleştirebilir (Bu durumda, bu yöntemi döndürür `S_FALSE`) veya ekleme işlemi için erteleme `IDebugEngine2::Attach` yöntemi ( `OnAttach` yöntemi döndürür `S_OK`). Ya da bir olay `OnAttach` yöntemi ayarlayabilirsiniz `GUID` için ayıklanan programın belirli `GUID`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgramNodeAttach2](../../../extensibility/debugger/reference/idebugprogramnodeattach2.md)   
 [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)
