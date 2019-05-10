---
title: IDebugProperty3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProperty3
helpviewer_keywords:
- IDebugProperty3 interface
ms.assetid: 8f9be68d-4490-4eca-8f6b-8a10ed77e226
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4f999d19ecee85d9664793a3d8e3ecc48fedbbdf
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65457601"
---
# <a name="idebugproperty3"></a>IDebugProperty3
Bu arabirim için destek sağlar:

- Özellikle ilişkili bir rasgele uzun dize alınıyor.

- Benzersiz bir kimlik özelliği ile ilişkilendirme.

- Bir özellik için özel görüntüleyiciler listesi alınıyor.

- Bir özelliğin değerini ortaya çıkan hataları rapor etme özelliğini ile ayarlama

## <a name="syntax"></a>Sözdizimi

```
IDebugProperty3 : IDebugProperty2
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE) bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) uzun dizeler, özellik kimlikleri ve özel görüntüleyiciler için destek sağlamak için.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde bir `IDebugProperty2` arabirimi bu arabirim elde edilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Devralınan yöntemleri yanı sıra `IDebugProperty2`, `IDebugProperty3` arabirimi aşağıdaki yöntemleri sunar.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetStringCharLength](../../../extensibility/debugger/reference/idebugproperty3-getstringcharlength.md)|Özellik ile ilişkilendirilmiş dize uzunluğunu döndürür.|
|[GetStringChars](../../../extensibility/debugger/reference/idebugproperty3-getstringchars.md)|Bir kullanıcı tarafından sağlanan arabellek dizeyi döndürür.|
|[CreateObjectID](../../../extensibility/debugger/reference/idebugproperty3-createobjectid.md)|Bu özellik için benzersiz bir kimliği oluşturur.|
|[DestroyObjectID](../../../extensibility/debugger/reference/idebugproperty3-destroyobjectid.md)|Bu özellik için benzersiz kimlik yok eder.|
|[GetCustomViewerCount](../../../extensibility/debugger/reference/idebugproperty3-getcustomviewercount.md)|Bu özellik ile görüntülenebilir özel görüntüleyiciler sayısını döndürür.|
|[GetCustomViewerList](../../../extensibility/debugger/reference/idebugproperty3-getcustomviewerlist.md)|Bu özellik ile görüntülenebilir özel görüntüleyiciler listesini döndürür.|
|[SetValueAsStringWithError](../../../extensibility/debugger/reference/idebugproperty3-setvalueasstringwitherror.md)|Herhangi bir sorun oluştu, hata iletisi döndüren, bu özelliğin değerini ayarlar.|

## <a name="remarks"></a>Açıklamalar
- [SetValueAsStringWithError](../../../extensibility/debugger/reference/idebugproperty3-setvalueasstringwitherror.md) oturum hata ayıklama Yöneticisi (SDM) bir özelliğin değerini ayarlamak için tercih edilen yoludur.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)
- [IDebugCustomViewer](../../../extensibility/debugger/reference/idebugcustomviewer.md)