---
title: IDebugFunctionObject::CreateArrayObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugFunctionObject::CreateArrayObject
helpviewer_keywords:
- IDebugFunctionObject::CreateArrayObject method
ms.assetid: a380e53c-15f1-401f-927f-f366eea789e6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e179d3b96fd1aeb101ceb6df2bc0d9169c51cb9d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55006066"
---
# <a name="idebugfunctionobjectcreatearrayobject"></a>IDebugFunctionObject::CreateArrayObject
Bir dizi nesnesi oluşturur. Bu dizi ya da temel içeren ya da örnek değerleri nesne.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT CreateArrayObject(   
   OBJECT_TYPE    ot,  
   IDebugField*   pClassField,  
   DWORD          dwRank,  
   DWORD          dwDims[],  
   DWORD          dwLowBounds[],  
   IDebugObject** ppObject  
);  
```  
  
```csharp  
int CreateArrayObject(  
   enum_OBJECT_TYPE ot,   
   IDebugField      pClassField,   
   uint             dwRank,   
   uint[]           dwDims,   
   uint[]           dwLowBounds,   
   out IDebugObject ppObject  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ot`  
 [in] Bir değer belirtir [Nesne_türü](../../../extensibility/debugger/reference/object-type.md) yeni bir dizi nesne türünü gösteren sabit listesi.  
  
 `pClassField`  
 [in] Bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesnenin bir dizi örnek değerleri oluşturuyorsanız bir nesnenin sınıfını temsil eden nesne. Temel nesneler dizisi oluşturuyorsanız, bu parametre null bir değerdir.  
  
 `dwRank`  
 [in] Boyut veya dizinin boyut sayısı.  
  
 `dwDims`  
 [in] Dizinin her boyutunun boyutları.  
  
 `dwLowBounds`  
 [in] Her boyutun kaynağını (genellikle 0 veya 1).  
  
 `ppObject`  
 [out] Döndürür bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) yeni oluşturulan diziyi temsil eden nesne. Bu, aslında bir [IDebugArrayObject](../../../extensibility/debugger/reference/idebugarrayobject.md) nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Tarafından temsil edilen işlevi için bir dizi parametre temsil eden bir nesne oluşturmak için bu yöntemi çağırın [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)