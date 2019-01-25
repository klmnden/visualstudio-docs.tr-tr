---
title: IDebugPointerField::GetDereferencedField | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPointerField::GetDereferencedField
helpviewer_keywords:
- IDebugPointerField::GetDereferencedField method
ms.assetid: 8de988ab-cd79-4287-be72-3c900f2fe407
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 02197f660189d4caf374fc5927f349fd5fc6b8b5
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54760557"
---
# <a name="idebugpointerfieldgetdereferencedfield"></a>IDebugPointerField::GetDereferencedField
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, bu işaretçi nesnesinin işaret ettiği nesnenin türü döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetDereferencedField(  
   IDebugField** ppField  
);  
```  
  
```csharp  
int GetDereferencedField(  
   out IDebugField ppField  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppField`  
 [out] Döndürür bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) açıklayan hedef nesnenin türü.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Örneğin, bir IF [IDebugPointerField](../../../extensibility/debugger/reference/idebugpointerfield.md) nesneyi işaret eden bir tamsayıya [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) bu yöntem tarafından döndürülen tür, tamsayı türü açıklar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPointerField](../../../extensibility/debugger/reference/idebugpointerfield.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
