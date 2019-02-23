---
title: IDebugProcessQueryProperties | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugProcessQueryProperties
ms.assetid: ce29a248-81a0-42c0-99a7-1606e8c548ec
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e54c51e4012bf129e7f8a8ad44fac8dca3e888c1
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56693678"
---
# <a name="idebugprocessqueryproperties"></a>IDebugProcessQueryProperties
Bu arabirim tarafından uygulanan bir uzantı arabirimdir [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) uygulayıcılar. Hata ayıklama işlem ortamı hakkında bilgi almak uygulayan sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugProcessQueryProperties: IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama işlemi yürütme ortamı hakkında bilgi edinmek için bu arabirimi uygulayın.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProcessQueryProperties`.

|Yöntem|Açıklama|
|------------|-----------------|
|[QueryProperty](../../../extensibility/debugger/reference/idebugprocessqueryproperties-queryproperty.md)|Bir özellik değeri için sorgular.|
|[QueryProperties](../../../extensibility/debugger/reference/idebugprocessqueryproperties-queryproperties.md)|Özellik değerleri için sorgular.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirim nadiren uygulanır.

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Portpriv.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)