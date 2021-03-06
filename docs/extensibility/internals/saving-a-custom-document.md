---
title: Özel belge kaydetme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- persistence, saving custom documents
- projects [Visual Studio SDK], saving custom documents
- editors [Visual Studio SDK], saving custom documents
ms.assetid: 040b36d6-1f0a-4579-971c-40fbb46ade1d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b90938e44b4227f8aad43542fc99136745a8af4e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66318739"
---
# <a name="saving-a-custom-document"></a>Özel Belge Kaydetme
Ortam tutamaçları **Kaydet**, **Kaydet**, ve **Tümünü Kaydet** komutları. Kullanıcı tıkladığında **Kaydet**, **Kaydet**, **veya Tümünü Kaydet** üzerinde **dosya** menüsü veya bir Tümünü Kaydet içinde aşağıdaki kaynaklanan çözümü kapatır işlem gerçekleşir.

 ![Müşteri Düzenleyicisini Kaydetme](../../extensibility/internals/media/private.gif "özel") kaydetme, Farklı Kaydet ve Tümünü Kaydet komutunu işlemek için özel bir düzenleyici

 Bu işlem aşağıdaki adımları ayrıntılı olarak verilmiştir:

1. İçin **Kaydet** ve **Kaydet** komutlar, ortamı kullanır <xref:Microsoft.VisualStudio.Shell.Interop.SVsShellMonitorSelection> etkin belge penceresini belirlemek için hizmet ve böylece hangi öğeler kaydedilmelidir. Etkin belge penceresini tanındıktan sonra ortam öğe tanımlayıcısı (öğe kimliği) ve hiyerarşi işaretçi çalıştırılan Belge tablosu belgede bulur. Daha fazla bilgi için [çalıştırılan Belge tablosu](../../extensibility/internals/running-document-table.md).

     Tümünü Kaydet komut için ortamı kaydetmek için tüm öğelerin listesini derlemek için çalışan belge tablosunda bilgileri kullanır.

2. Çözüm aldığında bir <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus%2A> çağrı, seçilen öğeleri dizi aracılığıyla yinelenir (diğer bir deyişle, tarafından kullanıma sunulan birden çok seçimin <xref:Microsoft.VisualStudio.Shell.Interop.SVsShellMonitorSelection> hizmeti).

3. Seçimdeki her bir öğede çözüm çağırmak için hiyerarşi işaretçi kullanır <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem2.IsItemDirty%2A> Kaydet menü komutunu etkinleştirilmesi gerekip gerekmediğini belirlemek için yöntemi. Ardından bir veya daha fazla öğe kirli, Kaydet komutunu etkinleştirilir. Hiyerarşi Standart Düzenleyici kullanıyorsa, ardından sorgulama hiyerarşi temsilcileri Düzenleyicisi durumuna çağırarak kirli <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2.IsDocDataDirty%2A> yöntemi.

4. Kirli her seçili öğe üzerinde çözüm çağırmak için hiyerarşi işaretçi kullanır <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem2.SaveItem%2A> uygun hiyerarşilerindeki yöntemi.

     Özel bir düzenleyici söz konusu olduğunda belge veri nesnesi ile proje arasındaki iletişimi özeldir. Bu nedenle, bu iki nesne herhangi bir özel Kalıcılık konuları ele alınır.

    > [!NOTE]
    > Kendi Kalıcılık uygularsanız, çağırdığınızdan emin olun <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QuerySaveFiles%2A> zaman kazanmak için yöntemi. Dosyayı kaydetmek güvenli olduğundan emin olmak için bu yöntem denetler (örneğin, dosyayı salt okunur değildir).

## <a name="see-also"></a>Ayrıca Bkz.
- <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>
- [Proje Öğelerini Açma ve Kaydetme](../../extensibility/internals/opening-and-saving-project-items.md)