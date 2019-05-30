---
title: IDebugPortPicker | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugPortPicker interface
ms.assetid: 8b7f6685-a3c5-4355-b706-c1b574f6ff84
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 991480886c2c43c330ce37561d383ffdc420e214
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66340362"
---
# <a name="idebugportpicker"></a>IDebugPortPicker
Özelleştirilmiş bir kullanıcı Arabirimi, bağlantı noktası seçmek için temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugPortPicker : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirim, bağlantı noktası sağlayıcıları tarafından uygulanır. Bağlantı noktası sağlayıcısı, bağlantı noktası seçici bir CLSID gösterme ve işaret eden tanımlar `metricPortPickerCLSID` ölçüm sunulan CLSID konumunda.

## <a name="methods"></a>Yöntemler
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugPortPicker`.

|Yöntem|Açıklama|
|------------|-----------------|
|[DisplayPortPicker](../../../extensibility/debugger/reference/idebugportpicker-displayportpicker.md)|Kullanıcının bir bağlantı noktası seçmesine izin veren belirtilen iletişim kutusunu görüntüler.|
|[SetSite](../../../extensibility/debugger/reference/idebugportpicker-setsite.md)|Hizmet sağlayıcısı ayarlar.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll