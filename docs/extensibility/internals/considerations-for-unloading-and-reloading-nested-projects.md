---
title: Kaldırma ve yeniden yüklemeyi konuları iç içe projeleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- nested projects, unloading and reloading
- projects [Visual Studio SDK], unloading and reloading nested
ms.assetid: 06c3427e-c874-45b1-b9af-f68610ed016c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b0b5738a5e8cf01466dd632797c3f92ffd135a44
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62861341"
---
# <a name="considerations-for-unloading-and-reloading-nested-projects"></a>Konuları kaldırma ve iç içe projeler yeniden yükleniyor

İç içe proje türleri uyguladığınızda, kaldırma ve projeleri yeniden ek adımları gerçekleştirmeniz gerekir. Doğru dinleyicileri çözüm olayları bildirmek için doğru şekilde yükseltmeniz gerekir `OnBeforeUnloadProject` ve `OnAfterLoadProject` olayları.

Bu olay bir kaynak kodu denetimi (SCC) nedenidir. Sunucudan öğelerini silin ve sonra eklemek için SCC istemediğiniz olarak geri *yeni* varsa bir `Get` SCC işlemi. Bu durumda, yeni bir dosya SCC dışında yüklenir. Kaldırma ve bunlar farklı durumunda tüm dosyaları yeniden etmesi gerekir.

Kaynak kodu denetim çağrıları `ReloadItem`. Uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsFireSolutionEvents> çağrılacak arabirimi `OnBeforeUnloadProject` ve `OnAfterLoadProject` projeyi silin ve yeniden oluşturun. Bu şekilde arabirimi uyguladığınızda, SCC proje geçici olarak silindi ve tekrar eklenmelidir, bilgisi verilir. Bu nedenle, proje olarak ise SCC proje üzerinde çalışmaz *gerçekten* silinmesi ve yeniden eklenir.

## <a name="reload-projects"></a>Projeleri yeniden yükle

İç içe projeler yeniden yükleniyor desteklemek için uygulamanız <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem2.ReloadItem%2A> yöntemi. Uygulamanızda `ReloadItem`, iç içe projeler kapatın ve sonra yeniden oluşturun.

Genellikle bir proje yeniden yüklendiğinde, IDE başlatır <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3.OnBeforeUnloadProject%2A> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3.OnAfterLoadProject%2A> olayları. Ancak, silinmesi ve yeniden iç içe projeler için ana proje işlemi, IDE başlatır. Ana proje çözüm olayları başlatmaz ve IDE başlatma işleminin hakkında bir bilgi bulunmaz çünkü tetiklenen olayları değil.

Bu işlem, ana proje aramaları işlenecek `QueryInterface` üzerinde <xref:Microsoft.VisualStudio.Shell.Interop.IVsFireSolutionEvents> arabirimi. `IVsFireSolutionEvents` yükseltmek için IDE bildiren bir işleve sahiptir `OnBeforeUnloadProject` iç içe geçmiş projeyi kaldırmak ve ardından yükseltmek için olay `OnAfterLoadProject` olayı aynı projeyi yeniden yükleyin.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3>
- [İç içe projeler](../../extensibility/internals/nesting-projects.md)