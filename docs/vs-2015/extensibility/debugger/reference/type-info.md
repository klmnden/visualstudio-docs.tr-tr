---
title: TYPE_INFO | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- TYPE_INFO
helpviewer_keywords:
- TYPE_INFO structure
ms.assetid: d725cb68-a565-49d1-a16f-ff0445c587a0
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: b780681ec94d347885cdc1134b4ef51776945dc8
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54765409"
---
# <a name="typeinfo"></a>TYPE_INFO
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yapı, çeşitli türlerdeki bir alan türü hakkında bilgi belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
struct _tagTYPE_INFO_UNION {  
   dwTYPE_KIND dwKind;  
   union {  
      METADATA_TYPE typeMeta;  
      PDB_TYPE      typePdb;  
      BUILT_TYPE    typeBuilt;  
      DWORD         unused;  
   } type;  
} TYPE_INFO;  
```  
  
```csharp  
public struct TYPE_INFO {  
   public uint   dwKind;  
   public IntPtr unionmember;  
};  
```  
  
#### <a name="parameters"></a>Parametreler  
 dwKind  
 Bir değer [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md) birleşim yorumlama belirleyen sabit listesi.  
  
 type.typeMeta  
 [Yalnızca C++] İçeren bir [METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md) , yapı `dwKind` olduğu `TYPE_KIND_METADATA`.  
  
 type.typePdb  
 [Yalnızca C++] İçeren bir [PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md) , yapı `dwKind` olduğu `TYPE_KIND_PDB`.  
  
 type.typeBuilt  
 [Yalnızca C++] İçeren bir [BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md) , yapı `dwKind` olduğu `TYPE_KIND_BUILT`.  
  
 Type.Unused  
 Kullanılmayan doldurma.  
  
 türü  
 Union adıdır.  
  
 unionmember  
 [C# yalnızca] Bu uygun yapı türüne göre sıralama `dwKind`.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yapı geçirilir [GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md) yöntemi burada da doldurulur. Yapı içeriğini yorumlanma şeklini dayanır `dwKind` alan.  
  
> [!NOTE]
>  [Yalnızca C++] Varsa `dwKind` eşittir `TYPE_KIND_BUILT`, arka plandaki serbest bırakmak gerekli ise [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesne yok etme `TYPE_INFO` yapısı. Bu çağrılarak gerçekleştirilir `typeInfo.type.typeBuilt.pUnderlyingField->Release()`.  
  
 [C# yalnızca] Aşağıdaki tablo nasıl yorumlanacağını gösterir `unionmember` türü her tür için üye. Bu örnek, türü bir tür için nasıl yapıldığını gösterir.  
  
|`dwKind`|`unionmember` yorumlanan|  
|--------------|----------------------------------|  
|`TYPE_KIND_METADATA`|[METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md)|  
|`TYPE_KIND_PDB`|[PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md)|  
|`TYPE_KIND_BUILT`|[BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md)|  
  
## <a name="example"></a>Örnek  
 Bu örnek nasıl yorumlanacağını gösterir `unionmember` üyesi `TYPE_INFO` C# yapısı. Bu örnek, yalnızca bir tür yorumlama gösterir (`TYPE_KIND_METADATA`), ancak diğerleri tam olarak aynı şekilde yorumlanır.  
  
```csharp  
using System;  
using System.Runtime.Interop.Services;  
using Microsoft.VisualStudio.Debugger.Interop;  
  
namespace MyPackage  
{  
    public class MyClass  
    {  
        public void Interpret(TYPE_INFO ti)  
        {  
            if (ti.dwKind == (uint)enum_dwTypeKind.TYPE_KIND_METADATA)  
            {  
                 METADATA_TYPE dataType = (METADATA_TYPE)Marshal.PtrToStructure(ti.unionmember,  
                                               typeof(METADATA_TYPE));  
            }  
        }  
    }  
}  
```  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılar ve birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md)   
 [GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md)   
 [METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md)   
 [PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md)   
 [BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md)
