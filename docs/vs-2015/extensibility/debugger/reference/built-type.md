---
title: BUILT_TYPE | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- BUILT_TYPE
helpviewer_keywords:
- BUILT_TYPE structure
ms.assetid: cc02c32c-0f65-4210-ad25-a9b1899066e8
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 6becf886d361e203dca313a7aa1dfdf166aa4614
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68153172"
---
# <a name="builttype"></a>BUILT_TYPE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yapı meta verilerinden harcanan alan türü hakkında bilgileri belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
typedef struct _tagTYPE_BUILT {  
   ULONG32      ulAppDomainID;  
   GUID         guidModule;  
   IDebugField* pUnderlyingField;  
} BUILT_TYPE;  
```  
  
```csharp  
public struct BUILT_TYPE {  
   public uint        ulAppDomainID;  
   public Guid        guidModule;  
   public IDebugField pUnderlyingField;  
};  
```  
  
#### <a name="parameters"></a>Parametreler  
 ulAppDomainID  
 Simgenin içinden gelen uygulama kimliği. Bu, uygulamanın bir örneğini benzersiz şekilde tanımlamak için kullanılır.  
  
 guidModule  
 Bu alan içeren modül GUID.  
  
 pUnderlyingField  
 Bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) yerleşik bu alanla ilişkilendirilmiş temel alan tanımlayan nesne.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yapı birleşimde bir parçası olarak görünür [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) ne zaman yapısı `dwKind` alanını `TYPE_INFO` yapısı ayarlandığında `TYPE_KIND_BUILT` (arasında bir değer [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md) sabit listesi).  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılar ve birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)   
 [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
