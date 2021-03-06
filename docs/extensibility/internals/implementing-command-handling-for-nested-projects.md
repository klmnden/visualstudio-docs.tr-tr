---
title: İç içe projeler için işleme komutunu uygulama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- nested projects, implementing command handling
ms.assetid: 48a9d66e-d51c-4376-a95a-15796643a9f2
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 66f89476e6d4a8fa009dbe921113c9e4cac54916
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66313195"
---
# <a name="implementing-command-handling-for-nested-projects"></a>İç içe Projeler için Komut İşlemesi Uygulama
IDE geçirilecek komutları geçirebilirsiniz <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> ve <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> iç içe projeler veya üst projelere arabirimleri filtreleyebilir veya komutları geçersiz kılar.

> [!NOTE]
> Normalde ana proje tarafından işlenen komutları filtrelenebilir. Gibi komutlar **derleme** ve **Dağıt** tarafından işlenen IDE filtrelenemez.

 Aşağıdaki adımlar komut işleme uygulama işlemi açıklanmaktadır.

## <a name="procedures"></a>Yordamlar

#### <a name="to-implement-command-handling"></a>Komut işleme uygulamak için

1. Kullanıcı bir iç içe proje ya da bir düğüm iç içe geçmiş bir projede seçtiğinde:

   1. IDE çağrıları <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus%2A> yöntemi.

      — veya —

   2. Çözüm Gezgini'nde, bir kısayol menü komutu gibi bir hiyerarşi penceresinde komut geldiyse IDE çağırır <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.QueryStatusCommand%2A> projenin üst yöntemi.

2. Ana proje geçirilecek parametreler inceleyebilirsiniz `QueryStatus`, gibi `pguidCmdGroup` ve `prgCmds`, ana proje komutları filtre olup olmadığını belirlemek için. Ana proje komutları filtrelemek için uygulanmışsa ayarlamanız gerekir:

   ```
   prgCmds[0].cmdf = OLECMDF_SUPPORTED;
   // make sure it is disabled
   prgCmds[0].cmdf &= ~MSOCMDF_ENABLED;
   ```

    Ana proje döndürmelidir sonra `S_OK`.

    Ana proje komutu filtrelemez varsa, yalnızca döndürmelidir `S_OK`. Bu durumda, IDE alt projeye komutu otomatik olarak yönlendirir.

    Komut alt projeye yönlendirmek ana proje yok. IDE, bu görevi gerçekleştiren...

## <a name="see-also"></a>Ayrıca Bkz.
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy>
- [Komutlar, Menüler ve Araç Çubukları](../../extensibility/internals/commands-menus-and-toolbars.md)
- [Projeleri İç İçe Geçirme](../../extensibility/internals/nesting-projects.md)