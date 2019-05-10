---
title: IDebugStackFrame3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugStackFrame3
helpviewer_keywords:
- IDebugStackFrame3 interface
ms.assetid: 39af2f57-0a01-42b8-b093-b7fbc61e2909
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b54e6ee8321d58046ec0beb372a14495b614db0c
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65458508"
---
# <a name="idebugstackframe3"></a>IDebugStackFrame3
Bu arabirim genişletir [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md) ilerlemesinden özel durumları işlemek için.

## <a name="syntax"></a>Sözdizimi

```
IDebugStackFrame3 : IDebugStackFrame2
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE) bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md) ilerlemesinden özel durumları desteklemek için arabirim.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde bir `IDebugStackFrame2` arabirimi bu arabirim elde edilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Devralınan yöntemleri yanı sıra [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md), `IDebugStackFrame3` aşağıdaki yöntemi kullanıma sunar.

|Yöntem|Açıklama|
|------------|-----------------|
|[InterceptCurrentException](../../../extensibility/debugger/reference/idebugstackframe3-interceptcurrentexception.md)|Geçerli yığın çerçevesi önce herhangi bir normal bir özel durum işleme için bir özel durum işleme.|
|[GetUnwindCodeContext](../../../extensibility/debugger/reference/idebugstackframe3-getunwindcodecontext.md)|Yığın geriye doğru izleme ortaya çıkacaksa kod bağlamı döndürür.|

## <a name="remarks"></a>Açıklamalar
 Ele geçirilen bir özel durum, çalışma zamanı tarafından herhangi bir normal bir özel durum işleme rutinleri çağrılmadan önce bir hata ayıklayıcı bir özel durum işleyebileceği anlamına gelir. Bir özel durum esas olarak kesintiye bile eşleşme olmadığında mevcut bir özel durum işleyicisi olduğunu anlatabilirsiniz çalıştırma yapma anlamına gelir.

- [Interceptcurrentexception](../../../extensibility/debugger/reference/idebugstackframe3-interceptcurrentexception.md) tüm normal bir özel durum geri çağırma olayları sırasında çağrılır (tek özel durumu (yönetilen ve yönetilmeyen kod), karma mod kod bu durumda özel durum kullanılamaz engelledik sırasında hata ayıklama durumunda olduğundan Son şans geri çağırma). Değil DE uygularsanız `IDebugStackFrame3`, veya DE IDebugStackFrame3 bir hata verir::`InterceptCurrentException` (gibi `E_NOTIMPL`), sonra hata ayıklayıcı özel durum normal olarak işler.

 Hata ayıklayıcı bir özel durum uğratarak ayıklanan programın durumunu değişiklikleri yapın ve ardından burada özel durumun oluştuğu noktada yürütmeyi devam etmesi izin verebilirsiniz.

> [!NOTE]
> Ele geçirilen özel durumlar yalnızca yönetilen kodda, diğer bir deyişle, ortak dil çalışma zamanı (CLR) altında çalışan bir program verilir.

 Hata ayıklama altyapısı "metricExceptions" ayarlayarak araya giren özel durumları desteklediğini değerini 1 olarak çalışma zamanında gösterir `SetMetric` işlevi. Daha fazla bilgi için [hata ayıklama için SDK Yardımcıları](../../../extensibility/debugger/reference/sdk-helpers-for-debugging.md).

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)
- [Hata Ayıklama için SDK Yardımcıları](../../../extensibility/debugger/reference/sdk-helpers-for-debugging.md)
