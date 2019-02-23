---
title: IDebugPortPicker | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugPortPicker interface
ms.assetid: 8b7f6685-a3c5-4355-b706-c1b574f6ff84
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 845e197b186d462b74aaf8cf3cd7218e4606dfc7
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56716551"
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