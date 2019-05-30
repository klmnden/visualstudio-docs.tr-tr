---
title: IDebugEngine2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine2
helpviewer_keywords:
- IDebugEngine2 interface
ms.assetid: 1f0e9ac0-6dfb-461a-976c-888d82144cdb
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ce60ffb1143dd763ea14390b0b55e105f74d1b53
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66352563"
---
# <a name="idebugengine2"></a>IDebugEngine2
Bu arabirim, hata ayıklama altyapısı (DE) temsil eder. Oluşturmasını ayarlama ve özel durumlar temizlemek için kesme noktaları hata ayıklama oturumu, çeşitli yönlerini yönetmek için kullanılır.

## <a name="syntax"></a>Sözdizimi

```
IDebugEngine2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirim programlarında hata ayıklama yönetmek için özel bir DE tarafından uygulanır. Bu arabirim tarafından DE uygulanmalıdır.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim, oturum hata ayıklama Yöneticisi (SDM) özel durumları yönetme, kesme noktaları oluşturma ve DE tarafından gönderilen zaman uyumlu olaylara yanıt vermek dahil olmak üzere hata ayıklama oturumu, yönetilecek tarafından çağrılır.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugEngine2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[EnumPrograms](../../../extensibility/debugger/reference/idebugengine2-enumprograms.md)|Bir DE tarafından ayıklanan bütün programların için bir numaralandırıcı oluşturur.|
|[Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)|Bir DE, bir programa ekler.|
|[CreatePendingBreakpoint](../../../extensibility/debugger/reference/idebugengine2-creatependingbreakpoint.md)|Bir bekleyen kesme noktasının içinde DE oluşturur.|
|[SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md)|Belirli bir özel durum DE nasıl işleyeceğini belirtir.|
|[RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md)|Belirtilen özel durum artık hata ayıklama altyapısı tarafından işlenecek şekilde kaldırır.|
|[RemoveAllSetExceptions](../../../extensibility/debugger/reference/idebugengine2-removeallsetexceptions.md)|IDE'nin belirli çalışma zamanı mimarisi veya dil için ayarlanmış özel durumlar listesindeki kaldırır.|
|[GetEngineID](../../../extensibility/debugger/reference/idebugengine2-getengineid.md)|GUID DE değerini alır.|
|[DestroyProgram](../../../extensibility/debugger/reference/idebugengine2-destroyprogram.md)|Belirtilen program beklenmedik şekilde sona erdi ve DE program için tüm başvuruları temizlemek ve bir programını DE bir olay yok bildirir.|
|[ContinueFromSynchronousEvent](../../../extensibility/debugger/reference/idebugengine2-continuefromsynchronousevent.md)|Daha önce DE tarafından SDM için gönderilen bir zaman uyumlu hata ayıklama olayı alınıp işlendiğini olduğunu belirtmek için SDM tarafından çağrılır.|
|[SetLocale](../../../extensibility/debugger/reference/idebugengine2-setlocale.md)|DE yerel ayarlar.|
|[SetRegistryRoot](../../../extensibility/debugger/reference/idebugengine2-setregistryroot.md)|Kayıt defteri kökü DE kullandığı şu anda ayarlar.|
|[SetMetric](../../../extensibility/debugger/reference/idebugengine2-setmetric.md)|Bir ölçüm ayarlar.|
|[CauseBreak](../../../extensibility/debugger/reference/idebugengine2-causebreak.md)|İstek tarafından bu DE ayıklanan bütün programların yürütme, iş parçacıkları birini çalıştırmayı denediğinde durdur.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)
- [GetEngine](../../../extensibility/debugger/reference/idebugenginecreateevent2-getengine.md)