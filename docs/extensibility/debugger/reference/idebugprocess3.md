---
title: IDebugProcess3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcess3
helpviewer_keywords:
- IDebugProcess3 interface
ms.assetid: 7bd6b952-cf34-4e66-b8f6-d472dac3748f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8db169a06864fad24ef7e6ce4c2d188e2a88ef1d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66313854"
---
# <a name="idebugprocess3"></a>IDebugProcess3
Bu arabirim, çalışan bir işleme ve programları temsil eder. Bu arabirim için çeşitli yöntemlerin yerine mevcut [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) arabirimi. Bu işlemdeki tüm programlar üzerinde denetim sağlar.

> [!NOTE]
> [Devam](../../../extensibility/debugger/reference/idebugprogram2-continue.md), [yürütme](../../../extensibility/debugger/reference/idebugprogram2-execute.md), ve [adım](../../../extensibility/debugger/reference/idebugprogram2-step.md) yöntemleri kullanım dışı ve artık kullanılmamalıdır. Karşılık gelen yöntemler kullanır `IDebugProcess3` bunun yerine arabirimi.

## <a name="syntax"></a>Sözdizimi

```
IDebugProcess3 : IDebugProcess2
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirim, programlar, grup olarak yönetmek için özel bağlantı noktası sağlayıcısı tarafından uygulanır. Programlar bir grup olarak yönetilen, bunların yürütme kontrol edebilir ve ifade değerlendiricisi için bir dil oluşturmak. Bu arabirim bağlantı sağlayıcı tarafından uygulanmalıdır.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim, bu işlemde tanıtılan programlar bir grup ile etkileşim kurmak için öncelikle oturum hata ayıklama Yöneticisi tarafından (SDM) adı verilir.

 Çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde bir [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) arabirimi bu arabirim elde edilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Devralınan yöntemleri yanı sıra [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md), `IDebugProcess3` aşağıdaki yöntemleri uygular.

|Yöntem|Açıklama|
|------------|-----------------|
|[Continue](../../../extensibility/debugger/reference/idebugprocess3-continue.md)|Yürütülmesini veya bir işlem üzerinden Adımlama devam eder.|
|[Execute](../../../extensibility/debugger/reference/idebugprocess3-execute.md)|Yürütme işlemi başlar.|
|[Step](../../../extensibility/debugger/reference/idebugprocess3-step.md)|Bir yönerge veya deyimi işlemindeki adımları iletin.|
|[GetDebugReason](../../../extensibility/debugger/reference/idebugprocess3-getdebugreason.md)|Hata ayıklama işlemi başlatıldı nedenini alır.|
|[SetHostingProcessLanguage](../../../extensibility/debugger/reference/idebugprocess3-sethostingprocesslanguage.md)|Hata ayıklama altyapısı yükleyebilir ve uygun ifade değerlendiricisi barındırma dili ayarlar.|
|[GetHostingProcessLanguage](../../../extensibility/debugger/reference/idebugprocess3-gethostingprocesslanguage.md)|Bu işlem için ayarlanmış dili alır.|
|[DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md)|Düzenle ve devam et (ENC) Bu işlem için devre dışı bırakır.<br /><br /> Bu yöntem bir özel bağlantı noktası sağlayıcısı uygulamaz (her zaman döndürmelidir `E_NOTIMPL`).|
|[GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md)|Bu işlem için ENC durumunu alın.<br /><br /> Bu yöntem bir özel bağlantı noktası sağlayıcısı uygulamaz (her zaman döndürmelidir `E_NOTIMPL`).|
|[GetEngineFilter](../../../extensibility/debugger/reference/idebugprocess3-getenginefilter.md)|Kullanılabilir hata ayıklama altyapıları için benzersiz tanımlayıcıları dizisini alır.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)