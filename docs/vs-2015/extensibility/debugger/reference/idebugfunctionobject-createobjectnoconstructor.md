---
title: IDebugFunctionObject::CreateObjectNoConstructor | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugFunctionObject::CreateObjectNoConstructor
helpviewer_keywords:
- IDebugFunctionObject::CreateObjectNoConstructor method
ms.assetid: 4e2bd6d5-f4bd-4c10-a998-3db451c9a0c8
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 0ea00035eb220ccd08590ceaea6db98944f4657a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68179454"
---
# <a name="idebugfunctionobjectcreateobjectnoconstructor"></a>IDebugFunctionObject::CreateObjectNoConstructor
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir nesne ile hiçbir oluşturucu oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT CreateObjectNoConstructor(   
   IDebugField*   pClassObject,  
   IDebugObject** ppObject  
);  
```  
  
```csharp  
int CreateObjectNoConstructor(  
   IDebugField      pClassField,   
   out IDebugObject ppObject  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pClassObject`  
 [in] Bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) oluşturulacak nesne türünü temsil eden nesne.  
  
 `ppObject`  
 [out] Döndürür bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) temsil eden yeni oluşturulan nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir yapı veya, tarafından temsil edilen bir işlev parametresi olan (yani bir oluşturucu gerektirmez) karmaşık türün bir örneği temsil eden bir nesne oluşturmak için bu yöntemi çağırın [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) arabirimi.  
  
 Nesne parametresi bir oluşturucu gerektiriyorsa, çağrı [CreateObject](../../../extensibility/debugger/reference/idebugfunctionobject-createobject.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)   
 [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)   
 [CreateObject](../../../extensibility/debugger/reference/idebugfunctionobject-createobject.md)
