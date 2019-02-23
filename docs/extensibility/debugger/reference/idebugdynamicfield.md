---
title: IDebugDynamicField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDynamicField
helpviewer_keywords:
- IDebugDynamicField interface
ms.assetid: caffbd95-7596-4714-84b1-b964e89a78bb
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d94a685b9c79069a047e32155234f9bf6a50d5c5
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56692027"
---
# <a name="idebugdynamicfield"></a>IDebugDynamicField
Bu arabirim, bir değişken türünü temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugDynamicField : IDebugField
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirim, çalışma zamanında belirlenebilir herhangi bir türü için bir temel sınıf olarak sembol sağlayıcıları tarafından uygulanır. Yalnızca yönetilen kod için budur.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim, daha özel arabirimler türetilebilir temel bir sınıfı temsil eder.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Bu arabirim, devralınan dışındaki herhangi bir yöntem sağlamaz `IDebugField`.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)