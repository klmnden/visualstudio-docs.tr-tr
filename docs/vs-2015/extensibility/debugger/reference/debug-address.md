---
title: DEBUG_ADDRESS | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- DEBUG_ADDRESS
helpviewer_keywords:
- DEBUG_ADDRESS structure
ms.assetid: 79f5e765-9aac-4b6e-82ef-bed88095e9ba
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d001d29433573fedde3b4310f989667538b4b69c
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63444963"
---
# <a name="debugaddress"></a>DEBUG_ADDRESS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yapı bir adresi temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
typedef struct _tagDEBUG_ADDRESS {  
   ULONG32             ulAppDomainID;  
   GUID                guidModule;  
   _mdToken            tokClass;  
   DEBUG_ADDRESS_UNION addr;  
} DEBUG_ADDRESS;  
```  
  
```csharp  
public struct DEBUG_ADDRESS {  
   public uint                ulAppDomainID;  
   public Guid                guidModule;  
   public int                 tokClass;  
   public DEBUG_ADDRESS_UNION addr;  
}  
```  
  
## <a name="terms"></a>Koşulları  
 ulAppDomainID  
 İşlem kimliği  
  
 guidModule  
 Bu adres içeren modül GUID.  
  
 tokClass  
 Sınıf veya bu adres türünü tanımlayan belirteç.  
  
> [!NOTE]
> Bu değer bir sembol sağlayıcısı için özeldir ve bu nedenle genel dışındaki bir sınıf türü için bir tanımlayıcı olarak anlamı yoktur.  
  
 addr  
 A [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md) yapısı, tek tek adres türlerini açıklayan yapıları birleşimini içerir. Değer `addr`.`dwKind` geldiği [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md) birleşim yorumlamak nasıl yapıldığını açıklayan sabit listesi.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yapı geçirilir [GetAddress](../../../extensibility/debugger/reference/idebugaddress-getaddress.md) doldurulması için yöntemi.  
  
 **Uyarı [C++ yalnızca]**  
  
 Varsa `addr.dwKind` olduğu `ADDRESS_KIND_METADATA_LOCAL` ve `addr.addr.addrLocal.pLocal` çağırmalısınız sonra boş bir değer değil `Release` belirteci işaretçinin:  
  
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
 [GetAddress](../../../extensibility/debugger/reference/idebugaddress-getaddress.md)   
 [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)   
 [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md)
