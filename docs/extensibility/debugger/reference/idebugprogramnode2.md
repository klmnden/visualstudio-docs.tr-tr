---
title: IDebugProgramNode2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramNode2
helpviewer_keywords:
- IDebugProgramNode2 interface
ms.assetid: 80e511d8-9b40-4a85-aa5d-952fa5ee6ae7
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a6a48f660302d39c9cfa75503ac7ca4a8c526a7f
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351077"
---
# <a name="idebugprogramnode2"></a>IDebugProgramNode2
Bu arabirim, hata ayıklaması yapılabilir bir program temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugProgramNode2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE) veya özel bağlantı noktası sağlayıcısı hata ayıklaması yapılabilir bir program temsil etmek için bu arabirimi uygular. Bu arabirimi uygulayan aynı nesne üzerinde uygulanan genellikle [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) arabirimi. Bu arabirim kayıtlı [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] çağırarak [PublishProgramNode](../../../extensibility/debugger/reference/idebugprogrampublisher2-publishprogramnode.md).

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Çağrı [GetProviderProgramNode](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprogramnode.md) bu arabirimi dönün. Bu arabirim yapılan bir çağrıyla özel bağlantı noktası sağlayıcısı alır [AddProgramNode](../../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md). Bu arabirim için bir çağrı yoluyla bir DE alır [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProgramNode2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetProgramName](../../../extensibility/debugger/reference/idebugprogramnode2-getprogramname.md)|Bir programın adını alır.|
|[GetHostName](../../../extensibility/debugger/reference/idebugprogramnode2-gethostname.md)|Bir program barındıran işlem adını alır.|
|[GetHostPid](../../../extensibility/debugger/reference/idebugprogramnode2-gethostpid.md)|Bir program barındırma işlemi için sistem işlemi tanımlayıcısını alır.|
|[GetHostMachineName_V7](../../../extensibility/debugger/reference/idebugprogramnode2-gethostmachinename-v7.md)|KULLANIM DIŞI. KULLANMAYIN.|
|[Attach_V7](../../../extensibility/debugger/reference/idebugprogramnode2-attach-v7.md)|KULLANIM DIŞI. KULLANMAYIN. Bkz: [IDebugProgramNodeAttach2](../../../extensibility/debugger/reference/idebugprogramnodeattach2.md) alternatif bir yaklaşım için arabirim.|
|[GetEngineInfo](../../../extensibility/debugger/reference/idebugprogramnode2-getengineinfo.md)|Bu programı çalıştırmayı DE tanıtıcısı ve adını alır.|
|[DetachDebugger_V7](../../../extensibility/debugger/reference/idebugprogramnode2-detachdebugger-v7.md)|KULLANIM DIŞI. KULLANMAYIN.|

## <a name="remarks"></a>Açıklamalar
 Oturum hata ayıklama Yöneticisi (SDM) genellikle çağrıları [GetProviderProgramNode](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprogramnode.md) bu arabirimi elde edilir.

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProgramNodeAttach2](../../../extensibility/debugger/reference/idebugprogramnodeattach2.md)
- [AddProgramNode](../../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md)
- [RemoveProgramNode](../../../extensibility/debugger/reference/idebugportnotify2-removeprogramnode.md)
- [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)
- [GetProviderProgramNode](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprogramnode.md)
- [PublishProgramNode](../../../extensibility/debugger/reference/idebugprogrampublisher2-publishprogramnode.md)