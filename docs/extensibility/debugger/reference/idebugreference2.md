---
title: IDebugReference2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugReference2
helpviewer_keywords:
- IDebugReference2 interface
ms.assetid: 3cfed312-f532-4bce-84a5-1677c14567d7
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 66d35b636516df1052ffa2a70c25da79851dd833
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66329648"
---
# <a name="idebugreference2"></a>IDebugReference2
Bu arabirim, yığın çerçeve özelliği veya diğer bir özelliği bir başvuruyu temsil eder.

> [!NOTE]
> `IDebugReference2` Gelecekte kullanım ve tüm metotlarını döndürmelidir için ayrılmış `E_NOTIMPL`.

## <a name="syntax"></a>Sözdizimi

```
IDebugReference2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 DE başvuru değeri belirli bir türünü göstermek için bu arabirimi uygular. Örneğin, değer, bellek veya kayıtları ve değerlerinin listesini görüntülemek için kullanılan bir bellek bağlamında ifade değerlendirme sonucu bir sayısal değer olabilir.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Çağrı [GetReference](../../../extensibility/debugger/reference/idebugproperty2-getreference.md) bu arabirimi elde edilir. [GetParent](../../../extensibility/debugger/reference/idebugreference2-getparent.md) ve [GetDerivedMostReference](../../../extensibility/debugger/reference/idebugreference2-getderivedmostreference.md) da bu arabirimi döndürür.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugReference2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetReferenceInfo](../../../extensibility/debugger/reference/idebugreference2-getreferenceinfo.md)|Alır [DEBUG_REFERENCE_INFO](../../../extensibility/debugger/reference/debug-reference-info.md) açıklayan bu başvuru yapısı.|
|[SetValueAsString](../../../extensibility/debugger/reference/idebugreference2-setvalueasstring.md)|Bu başvuruyu bir dize değerini ayarlar.|
|[SetValueAsReference](../../../extensibility/debugger/reference/idebugreference2-setvalueasreference.md)|Bu başvurunun dışında başka bir başvuru değerini ayarlar.|
|[EnumChildren](../../../extensibility/debugger/reference/idebugreference2-enumchildren.md)|Bu başvurunun alt numaralandırır.|
|[GetParent](../../../extensibility/debugger/reference/idebugreference2-getparent.md)|Bu başvurunun ana alır.|
|[GetDerivedMostReference](../../../extensibility/debugger/reference/idebugreference2-getderivedmostreference.md)|Bu başvurunun en çok türetilen referansını alır.|
|[GetMemoryBytes](../../../extensibility/debugger/reference/idebugreference2-getmemorybytes.md)|Bu başvuru başvurduğu bellek bayt alır.|
|[GetMemoryContext](../../../extensibility/debugger/reference/idebugreference2-getmemorycontext.md)|Bu başvuru için bir bellek bağlamı alır.|
|[GetSize](../../../extensibility/debugger/reference/idebugreference2-getsize.md)|Bu başvuru bayt cinsinden boyutunu alır.|
|[SetReferenceType](../../../extensibility/debugger/reference/idebugreference2-setreferencetype.md)|Bu başvuru türünü ayarlar.|
|[Compare](../../../extensibility/debugger/reference/idebugreference2-compare.md)|Bu başvuru başka ile karşılaştırır.|

## <a name="remarks"></a>Açıklamalar

> [!NOTE]
> Bu kullanım "özelliğinin" ile bir sınıfın üye değişkeni anlamı olsa da karıştırılmamalıdır bir `IDebugReference2` böyle bir varlık temsil edebilir.

- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) bir özelliği temsil ederken `IDebugReference2` genellikle hata ayıklanan programa içinde bir nesneye başvuru bir özelliğe başvuruyu temsil eder.

 Bir özellik ve başvuru arasındaki temel fark, adlandırılmamış bir örneğine bir başvuru başvuruyor ancak bir özellik bir nesnenin, adlandırılmış bir örneğine başvurduğunu ' dir. Örneğin, bir özellik tarafından programın yığınındaki bir nesneye başvurabilir `"a.b"`. Başka bir özellik aynı nesneye başvurabilir `"c.d"`. Bu özelliğe başvuran yol gerektiren `"a.b"` veya `"c.d"` kapsam içinde yer. Bu aynı nesneye bir başvuru adsız; Bu nesne için bellek geçerli olduğu sürece nesne için belirtilebilir.

 Bir `IDebugProperty2` arabirimi düşünülebilir bir adı, türü ve bir adresi olan bir değer olarak. Bir `IDebugReference2`, diğer el, bir tür ve bir adres düşünülebilir.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [DEBUG_REFERENCE_INFO](../../../extensibility/debugger/reference/debug-reference-info.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)
- [GetReference](../../../extensibility/debugger/reference/idebugproperty2-getreference.md)