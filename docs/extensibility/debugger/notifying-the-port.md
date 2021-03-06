---
title: Bağlantı noktasına bildirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- ports, notification
ms.assetid: f9fce48e-7d4e-4627-a0fb-77b75428146a
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9e7ccb4ab9fc36e08f4094baaf1e6b6eee30b2f8
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351512"
---
# <a name="notify-the-port"></a>Bağlantı noktası bildir
Bir programın tanıtımından sonra bağlantı noktası, şu şekilde bildirilmesi gerekir:

1. Bir bağlantı noktası, yeni bir programı düğüm aldığında, bir program oluşturma olayı hata ayıklama oturumu için geri gönderir. Olay ile program temsil eden bir arabirim taşır.

2. Hata ayıklama oturumu program ekleyebilirsiniz hata ayıklama altyapısı (DE) tanımlayıcısı için sorgular.

3. Hata ayıklama oturumunu DE Bu program için izin verilen DEs listesinde olup olmadığını denetler. Hata ayıklama oturumu ilk olarak hata ayıklama paketi tarafından geçirilen, çözümün etkin programı ayarlar bu listeyi alır.

    İzin verilen listede DE olması gerekir, aksi takdirde DE programa bağlı değil.

   Programlama yoluyla bir bağlantı noktası yeni bir programı düğümü ilk kez aldığında, oluşturduğu bir [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md) program temsil eden arabirim.

> [!NOTE]
> Bu ile karıştırılmamalıdır `IDebugProgram2` arabirimi daha sonra hata ayıklama altyapısı (DE) tarafından oluşturuldu.

 Bağlantı noktası gönderen bir [IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md) oturum hata ayıklama Yöneticisi (SDM) yoluyla bir COM program oluşturma olayına geri `IConnectionPoint` arabirimi.

> [!NOTE]
> Bu ile karıştırılmamalıdır `IDebugProgramCreateEvent2` arabirimi, tarafından DE daha sonra gönderilir.

 Olay arabirimi yanı sıra kendisini, bağlantı noktası gönderir [IDebugPort2](../../extensibility/debugger/reference/idebugport2.md), [IDebugProcess2](../../extensibility/debugger/reference/idebugprocess2.md), ve [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md) bağlantı noktasını temsil eder ve arabirimler, işlemek ve , sırasıyla program. SDM çağrıları [IDebugProgram2::GetEngineInfo](../../extensibility/debugger/reference/idebugprogram2-getengineinfo.md) programda hata ayıklamak DE GUID alınamıyor. GUID başlangıçta elde edildiği [IDebugProgramNode2](../../extensibility/debugger/reference/idebugprogramnode2.md) arabirimi.

 SDM DE izin verilen DEs Listesi penceresinde olup olmadığını denetler. SDM çözümün etkin programı ayarlar, ilk olarak hata ayıklama paketi tarafından geçirilen bu listeyi alır. İzin verilen listede DE olması gerekir, aksi takdirde, programın da bağlı değil.

 Kimliğini DE tanındıktan sonra SDM programa eklemek hazırdır.

## <a name="see-also"></a>Ayrıca bkz.
- [Program başlatma](../../extensibility/debugger/launching-a-program.md)
- [Başlatmadan sonra ekleme](../../extensibility/debugger/attaching-after-a-launch.md)
- [Hata ayıklama görevleri](../../extensibility/debugger/debugging-tasks.md)