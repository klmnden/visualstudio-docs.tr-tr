---
title: IEnumDebugModules2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugModules2
helpviewer_keywords:
- IEnumDebugModules2
ms.assetid: 4fe28074-a960-41ad-b74d-b57f04c0c0ad
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 548bcd0328f7bdf52e47eb9a4295168ca47a2517
ms.sourcegitcommit: 6196d0b7fdcb08ba6d28a8151ad36b8d1139f2cc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65226695"
---
# <a name="ienumdebugmodules2"></a>IEnumDebugModules2
Bu arabirim, modüllerin listesini numaralandırır.

## <a name="syntax"></a>Sözdizimi

```
IEnumDebugModules2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE) için bir program yüklü modüller listesini temsil etmek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Visual Studio çağrıları [EnumModules](../../../extensibility/debugger/reference/idebugprogram2-enummodules.md) bu arabirimi elde edilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumDebugModules2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[Next](../../../extensibility/debugger/reference/ienumdebugmodules2-next.md)|Bir numaralandırma sıralı modüllerinin belirtilen bir sayı alır.|
|[Skip](../../../extensibility/debugger/reference/ienumdebugmodules2-skip.md)|Bir numaralandırma sıralı modülleri belirtilen sayıda atlar.|
|[Reset](../../../extensibility/debugger/reference/ienumdebugmodules2-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|
|[Clone](../../../extensibility/debugger/reference/ienumdebugmodules2-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|
|[GetCount](../../../extensibility/debugger/reference/ienumdebugmodules2-getcount.md)|Modüller sayısını alır.|

## <a name="remarks"></a>Açıklamalar
 Visual Studio, öncelikli olarak güncelleştirmek için bu arabirimi kullanan **modülleri** penceresi.

 Visual Studio'da hata ayıklama amacıyla, modül sınırları, bu nedenle çapraz kod yönergeleri mantıksal bir dizi programdır modülleri için tek bir listesi için gereken [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) arabirimi. Listedeki ilk modülü genellikle ilişkili programı için ilk giriş noktası içerir.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [EnumModules](../../../extensibility/debugger/reference/idebugprogram2-enummodules.md)