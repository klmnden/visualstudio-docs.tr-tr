---
title: METADATA_ADDRESS_LOCAL | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- METADATA_ADDRESS_LOCAL
helpviewer_keywords:
- METADATA_ADDRESS_LOCAL structure
ms.assetid: 635f6bc5-c486-4e0e-83db-36f15e543843
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b29c9ec3d424dfb88f4cbe14e6e8baea87737d8e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54916696"
---
# <a name="metadataaddresslocal"></a>METADATA_ADDRESS_LOCAL
Bu yapı (genellikle bir işlev veya yöntem), bir kapsamdaki yerel değişkenin adresini temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
typedef struct _tagMETADATA_ADDRESS_LOCAL {  
   _mdToken  tokMethod;  
   IUnknown* pLocal;  
   DWORD     dwIndex;  
} METADATA_ADDRESS_LOCAL;  
```  
  
```csharp  
public struct METADATA_ADDRESS_LOCAL {  
   public int    tokMethod;  
   public object pLocal;  
   public uint   dwIndex;  
}  
```  
  
## <a name="terms"></a>Koşulları  
 tokMethod  
 Yöntem veya işlev Kimliğini yerel değişken, parçasıdır.  
  
 [C++] `_mdToken` olduğu bir `typedef` 32-bit `int`.  
  
 pLocal  
 Belirteci adresi bu yapıyı temsil eder.  
  
 dwIndex  
 Bu yöntem veya işlev ya da başka bir değer (dile özgü) yerel değişken dizini olabilir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yapı, birleşim içinde parçasıdır [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md) ne zaman yapısı `dwKind` alanını `DEBUG_ADDRESS_UNION` yapısı ayarlandığında `ADDRESS_KIND_LOCAL` (arasında bir değer [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md) sabit listesi).  
  
 `Warning:` [Yalnızca C++]  Varsa `pLocal` çağırmalısınız sonra null değil `Release` belirteci işaretçinin (`addr` bir alandır [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) yapısı):  
  
```  
if (addr.dwKind == ADDRESS_KIND_METADATA_LOCAL &&  addr.addr.addrLocal.pLocal != NULL)  
{  
    addr.addr.addrLocal.pLocal->Release();  
}  
```  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılar ve birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)   
 [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)   
 [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md)