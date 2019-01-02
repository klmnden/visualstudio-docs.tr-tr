---
title: Hata ayıklayıcı kavramları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK]
ms.assetid: 2d371d38-f1a0-4a9a-8ea3-100e8c0149b7
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 99ecd5d685592a252a185feaedc75a5566f1c5ea
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53857497"
---
# <a name="debugger-concepts"></a>Hata ayıklayıcı kavramları
Visual Studio hata ayıklama paketi oluşturmak için kullanılan paket tasarlamada mimari kavramlarını tanımanız gerekir.  
  
## <a name="in-this-section"></a>Bu bölümde  
 [Oturum hatalarını ayıklama](../../extensibility/debugger/debug-session.md)  
 Rol oturumunun hata ayıklama mimarisi açıklanmaktadır.  
  
 [Sunucular](../../extensibility/debugger/servers-visual-studio-sdk.md)  
 Tanımlar hangi bir mimari, hata ayıklama açısından hem soyut hem de fiziksel koşullarını sunucusudur.  
  
 [Bağlantı noktası sağlayıcıları](../../extensibility/debugger/port-suppliers.md)  
 Tanımlar mimarisi hata ayıklama açısından bağlantı noktası sağlayıcısı değildir.  
  
 [Bağlantı Noktaları](../../extensibility/debugger/ports.md)  
 Tanımlar hata ayıklama mimarisi bakımından hangi bağlantı noktasıdır.  
  
 [İşlemler](../../extensibility/debugger/processes.md)  
 Tanımlar hata ayıklama mimarisi bakımından, hangi bir işlemdir.  
  
 [Program düğümleri](../../extensibility/debugger/program-nodes.md)  
 Mimari, kendisi ve onu çalıştıran işlemin nasıl tanımlamak de dahil olmak üzere hata ayıklama açısından bir program düğümü tanımlar.  
  
 [Programlar](../../extensibility/debugger/programs.md)  
 Bir programı hata ayıklama mimarisi bakımından tanımlar.  
  
 [İş Parçacıkları](../../extensibility/debugger/threads.md)  
 İş parçacığı hata ayıklama mimarisi bakımından özelliklerini tanımlar.  
  
 [Yığın çerçeveleri](../../extensibility/debugger/stack-frames.md)  
 Hata ayıklama mimarisi bakımından bir yığın çerçevesini tanımlar. Bir yığın çerçevesi, bir iş parçacığı yürütme bağlamı sağlayan bir yığının bir soyutlamadır.  
  
 [Modüller](../../extensibility/debugger/modules.md)  
 Mimari, fiziksel bir yürütülebilir dosya veya bir DLL gibi bir kod kapsayıcısı olarak hata ayıklama açısından bir modül tanımlar.  
  
 [Kesme Noktaları](../../extensibility/debugger/breakpoints-visual-studio-sdk.md)  
 Kesme noktaları üç tür tanımlar — beklemede, bağlama ve hata — hata ayıklama mimarisi bakımından.  
  
## <a name="related-sections"></a>İlgili bölümler  
 [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md)  
 Nasıl hata ayıklama altyapısı (DE) aynı anda kod, belgeler ve ifade değerlendirme bağlamı içinde çalıştığı açıklanmaktadır. , Her üç bağlamları, konumu, konum veya değerlendirme için ilgili açıklar.  
  
 [Hata ayıklayıcı bileşenleri](../../extensibility/debugger/debugger-components.md)  
 Hata ayıklama altyapısı (DE) ifade değerlendiricisi (EE) ve sembol işleyici (SH) Visual Studio hata ayıklama Bileşenleri'ne genel bakış sağlar.  
  
 [Hata ayıklama görevleri](../../extensibility/debugger/debugging-tasks.md)  
 Program başlatma ve ifadeleri değerlendirme gibi çeşitli hata ayıklama görevlerini bağlantılar içerir.