---
title: IDebugObject2::GetBackingFieldForProperty | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugObject2::GetBackingFieldForProperty
helpviewer_keywords:
- IDebugObject2::GetBackingFieldForProperty method
ms.assetid: e72c6338-5573-4fad-8075-f3ade3435424
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 5eadbed61638ff1442c4ed7033426e245abf930a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54760545"
---
# <a name="idebugobject2getbackingfieldforproperty"></a>IDebugObject2::GetBackingFieldForProperty
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Alan veya değişken (varsa) alır, yedekleme bu nesne tarafından temsil edilen özelliği.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetBackingFieldForProperty(  
   IDebugObject2** ppObject  
);  
```  
  
```csharp  
int GetBackingFieldForProperty(  
   out IDebugObject2 ppObject  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppObject`  
 [out] Bir [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md) yedekleme alanını tanımlayan nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md) temsil eden bir yönetilen kod sınıf özelliği, diğer bir deyişle, bir get yöntemi nesnesi ve/veya set erişimcisine. Bu özellikler genellikle özelliği tarafından yönetilen değeri içeren bir değişkeni gerektirir. Bu değişken yedekleme alanı olarak bilinir. Nesne için yedekleme alanı yok ise, ardından bir null değer döndürmek emin olun: bazı çağıranlar dönüş değerine dikkatini ödeme değil ancak bunun yerine, bir null değer döndürüldü, görmek için görüneceğini `ppObject`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)
