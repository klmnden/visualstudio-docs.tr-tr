---
title: IEnumCodePaths2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumCodePaths2
helpviewer_keywords:
- IEnumCodePaths2 interface
ms.assetid: 17ec9f9e-dc06-4532-b5db-da52efcc8630
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: eb1df4276c6156b6d53fbf40499f44a40275cba1
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56692755"
---
# <a name="ienumcodepaths2"></a>IEnumCodePaths2
Bu arabirim, kod yolları bir listesini temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IEnumCodePaths2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE) kod yolları bir listesini göstermek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Çağrı [EnumCodePaths](../../../extensibility/debugger/reference/idebugprogram2-enumcodepaths.md) bu arabirimi elde edilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumCodePaths2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[Next](../../../extensibility/debugger/reference/ienumcodepaths2-next.md)|Belirtilen bir kod yolları bir numaralandırma sıralı sayısını alır.|
|[Skip](../../../extensibility/debugger/reference/ienumcodepaths2-skip.md)|Belirtilen sayıda kod yolları bir numaralandırma sıralı atlar.|
|[Reset](../../../extensibility/debugger/reference/ienumcodepaths2-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|
|[Clone](../../../extensibility/debugger/reference/ienumcodepaths2-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|
|[GetCount](../../../extensibility/debugger/reference/ienumcodepaths2-getcount.md)|Kod yolu sayısını bir numaralandırıcı alır.|

## <a name="remarks"></a>Açıklamalar
 Bir kod yolu bir programda bir dal noktası veya işlev çağrısını temsil eder. Kod yolları bir listesi üzerinden, kod yürütme alınan yolu temsil eder.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)