---
title: IDebugPort2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPort2
helpviewer_keywords:
- IDebugPort2 interface
ms.assetid: 8fd87f05-a950-4d14-b925-98be29d4facc
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fb489cddf090bf9958dee57f424ba009eb2c2209
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66326842"
---
# <a name="idebugport2"></a>IDebugPort2
Bu arabirim, bir makinedeki bir hata ayıklama bağlantı temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugPort2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Özel bağlantı noktası sağlayıcısı bir hata ayıklama bağlantı noktası bir makinede temsil etmek için bu arabirimi uygular.

 Bağlantı noktası gönderme bağlantı noktası olayları destekliyorsa, ayrıca uygulamalıdır <xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer> arabirimi desteklemek için bir <xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint> sırayla sağlayan arabirimi [IDebugPortEvents2](../../../extensibility/debugger/reference/idebugportevents2.md) arabirimi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Çağrılar [GetPort](../../../extensibility/debugger/reference/idebugportsupplier2-getport.md) veya [AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md) istenen bağlantı noktası gösteren bu bir arabirim döndürür.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugPort2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetPortName](../../../extensibility/debugger/reference/idebugport2-getportname.md)|Bağlantı noktası adı döndürür.|
|[GetPortId](../../../extensibility/debugger/reference/idebugport2-getportid.md)|Bağlantı noktası tanımlayıcısını döndürür.|
|[GetPortRequest](../../../extensibility/debugger/reference/idebugport2-getportrequest.md)|Bir bağlantı noktası (varsa) oluşturmak için kullanılan istek döndürür.|
|[GetPortSupplier](../../../extensibility/debugger/reference/idebugport2-getportsupplier.md)|Bu bağlantı için bağlantı noktası sağlayıcısı döndürür.|
|[GetProcess](../../../extensibility/debugger/reference/idebugport2-getprocess.md)|İşlem tanımlayıcısı verilen işlem için bir arabirim döndürür.|
|[EnumProcesses](../../../extensibility/debugger/reference/idebugport2-enumprocesses.md)|Bir bağlantı noktası üzerinde çalışan tüm işlemler numaralandırır.|

## <a name="remarks"></a>Açıklamalar
 Yerel bağlantı noktası işlemleri ve yerel makine üzerinde çalışan programlar erişim sağlar. Diğer bağlantı noktaları, Windows CE tabanlı bir cihaz için bir seri kablo bağlantısı veya ağ bağlantısı DCOM olmayan bir bilgisayara temsil edebilir. `IDebugPort2` Arabirimi adını ve bağlantı noktası tanıtıcısı bulun ve bağlantı noktası üzerinde çalışan tüm işlemler numaralandırmak için kullanılır. Başlatma ve bağlantı noktası işlemleri sonlandırma için tesis içinde uygulanan `IDebugPortEx2` arabirimi.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)
- [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)