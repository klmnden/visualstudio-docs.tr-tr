---
title: IDebugPointerObject::SetBytes | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPointerObject::SetBytes
helpviewer_keywords:
- IDebugPointerObject::SetBytes method
ms.assetid: 8c578b38-38d7-46f3-bb2e-8a730fccd334
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 9d467b037f4e2affea53a142304507f876630999
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54792051"
---
# <a name="idebugpointerobjectsetbytes"></a>IDebugPointerObject::SetBytes
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Art arda bayt dizisinden işaret değeri ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT SetBytes(   
   DWORD  dwStart,  
   DWORD  dwCount,  
   BYTE*  pBytes,  
   DWORD* pdwBytes  
);  
```  
  
```csharp  
int SetBytes(  
   uint     dwStart,   
   uint     dwCount,   
   byte[]   pBytes,   
   out uint pdwBytes  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwStart`  
 [in] Belirtilen nesnenin başından itibaren bayt cinsinden uzaklık.  
  
 `dwCount`  
 [in] Ayarlanacak bayt sayısı.  
  
 `pBytes`  
 [in] Yeni değeri temsil eden bir bayt dizisi. Bu değer, belirtilen uzaklıkta başlayan belirli nesne içinde depolanır.  
  
 `pdwBytes`  
 [out] Bayt sayısı gerçekte ayarlamak döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem kullanılır bu tarafından temsil edilen işaretçinin [IDebugPointerObject](../../../extensibility/debugger/reference/idebugpointerobject.md) işaret türü basit tür veya basit bir dizi temel türlerin (diğer bir deyişle, basit bir bayt dizisi tarafından temsil edilen bir dizi). Bu `IDebugPointerObject` nesne (onu işaret etmelidir bir bellek adresi) bir null başvuru olamaz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [GetBytes](../../../extensibility/debugger/reference/idebugpointerobject-getbytes.md)   
 [IDebugPointerObject](../../../extensibility/debugger/reference/idebugpointerobject.md)
