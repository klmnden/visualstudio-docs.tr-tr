---
title: Hata ayıklayıcı kavramları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK]
ms.assetid: 2d371d38-f1a0-4a9a-8ea3-100e8c0149b7
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7e3a9043215c5242246e54dc3e1eb2e85cd26c91
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62925899"
---
# <a name="debugger-concepts"></a>Hata ayıklayıcı kavramları
Visual Studio hata ayıklama paketi oluşturmak için kullanılan paket tasarlamada mimari kavramlarını tanımanız gerekir.

## <a name="in-this-section"></a>Bu bölümde
 [Hata ayıklama oturumu](../../extensibility/debugger/debug-session.md) rolünde oturumunun hata ayıklama mimarisi açıklanmaktadır.

 [Sunucuları](../../extensibility/debugger/servers-visual-studio-sdk.md) hangi bir sunucudur mimarisi, hata ayıklama açısından hem soyut hem de fiziksel koşullarını tanımlar.

 [Bağlantı noktası tedarikçileri](../../extensibility/debugger/port-suppliers.md) hangi bağlantı noktası sağlayıcısı olan hata ayıklama mimarisi bakımından tanımlar.

 [Bağlantı noktaları](../../extensibility/debugger/ports.md) hangi bağlantı noktası olan hata ayıklama mimarisi bakımından tanımlar.

 [İşlemler](../../extensibility/debugger/processes.md) hangi bir işlem olan hata ayıklama mimarisi bakımından tanımlar.

 [Program düğümleri](../../extensibility/debugger/program-nodes.md) mimarisi kendisi ve içinde çalıştığı işlemin nasıl tanımlamak de dahil olmak üzere, hata ayıklama açısından bir program düğümü tanımlar.

 [Programları](../../extensibility/debugger/programs.md) bir programı hata ayıklama mimarisi bakımından tanımlar.

 [İş parçacığı](../../extensibility/debugger/threads.md) hata ayıklama mimarisi bakımından iş parçacığı özelliklerini tanımlar.

 [Yığın çerçevesi](../../extensibility/debugger/stack-frames.md) hata ayıklama mimarisi bakımından bir yığın çerçevesini tanımlar. Bir yığın çerçevesi, bir iş parçacığı yürütme bağlamı sağlayan bir yığının bir soyutlamadır.

 [Modüller](../../extensibility/debugger/modules.md) mimarisi, bir yürütülebilir dosya veya bir DLL gibi kod fiziksel bir kapsayıcı olarak hata ayıklama açısından bir modül tanımlar.

 [Kesme noktaları](../../extensibility/debugger/breakpoints-visual-studio-sdk.md) kesme noktaları üç tür tanımlar — beklemede, bağlama ve hata — hata ayıklama mimarisi bakımından.

## <a name="related-sections"></a>İlgili bölümler
 [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md) hata ayıklama altyapısı (DE) kod, belgeler ve ifade değerlendirme bağlamı içinde aynı anda nasıl çalıştığı açıklanmaktadır. , Her üç bağlamları, konumu, konum veya değerlendirme için ilgili açıklar.

 [Hata ayıklayıcı bileşenleri](../../extensibility/debugger/debugger-components.md) hata ayıklama altyapısı (DE) ifade değerlendiricisi (EE) ve sembol işleyici (SH) Visual Studio hata ayıklama Bileşenleri'ne genel bakış sağlar.

 [Hata ayıklama görevleri](../../extensibility/debugger/debugging-tasks.md) çeşitli program başlatma ve ifadeleri değerlendirme gibi hata ayıklama görevleri bağlantılar içerir.