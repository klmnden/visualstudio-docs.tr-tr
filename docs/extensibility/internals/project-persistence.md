---
title: Proje kalıcılığı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- persistence, projects
- projects [Visual Studio SDK], persistance
ms.assetid: 42907bcf-4e27-46bd-a8cb-01c2ccd2bde5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5c0f81d3cb4cc1e3404087f6ad4b8ecac34b9ec0
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66328331"
---
# <a name="project-persistence"></a>Proje Kalıcılığı
Kalıcılık, projeniz için bir temel tasarım noktadır. Çoğu proje dosyaları temsil edecek proje öğeleri kullanın. [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] verisini dosya tabanlı olmayan projeleri de destekler. Proje ve proje dosyası tarafından sahip olunan dosyaları, her iki kalıcı gerekir. IDE kendisi veya bir proje öğesi kaydetmek için projeyi bildirir.

 Şablonları projeleri için proje fabrikasına geçirilir. Şablonları, belirli bir proje türünü gereksinimlerine göre tüm proje öğelerinin başlatma desteklemelidir. Bu şablonları daha sonra proje dosyaları olarak kaydedilen ve IDE çözüm aracılığıyla yönetilir. Daha fazla bilgi için [oluşturma proje örnekleri tarafından kullanarak proje Fabrikalarını](../../extensibility/internals/creating-project-instances-by-using-project-factories.md) ve [çözümleri](../../extensibility/internals/solutions-overview.md).

 Proje öğeleri, dosya tabanlı veya dosya tabanlı olmayan olabilir:

- Yerel veya uzak dosya tabanlı öğeleri olabilir. Uzak sistemde dosyaların kalıcı ise C# Web projelerinde, örneğin, uzak bir sistem dosyalarına yönelik bağlantıları yerel olarak kalıcı hale getirin.

- Dosya tabanlı olmayan öğeler için bir veritabanı veya havuz öğeleri kaydedebilirsiniz.

## <a name="commit-models"></a>Yürütme modelleri
 Proje öğeleri bulunduğu yere karar verdikten sonra uygun bir yürütme modeli seçmeniz gerekir. Örneğin, bir dosya tabanlı model ile yerel dosyaları, her proje otonom olarak kaydedilebilir. Bir depo modelde bir işlemde birden çok öğe kaydedebilirsiniz. Daha fazla bilgi için [proje türü tasarım kararları](../../extensibility/internals/project-type-design-decisions.md).

 Dosya adı uzantıları belirlemek için Projeler uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat> uygulamak bir nesnenin istemci etkinleştirme bilgi sağlayan bir arabirimi **Kaydet** iletişim kutusu — diğer bir deyişle, doldurmak için **Kaydet**  aşağı açılan listesinde ve ilk dosya adı uzantısı yönetin.

 IDE çağrıları `IPersistFileFormat` arabirimde proje, proje kalıcı olması belirtmek için proje öğelerini uygun şekilde. Bu nedenle, dosya ve biçim tüm yönlerini nesnenin sahibi. Bu nesnenin biçim adını içerir.

 Öğe olmadığı dosyaları durumda `IPersistFileFormat` nasıl dosya tabanlı olmayan hala geçerli olduğunu öğeleri kalıcı olarak tutulur. Proje için .vbp dosyaları gibi dosyalar [!INCLUDE[vbprvb](../../code-quality/includes/vbprvb_md.md)] projeleri veya .vcproj dosyaları [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] projeleri gerekir ayrıca kalıcı.

 Eylemler için çalıştırılan Belge tablosu (RDT) IDE inceler ve hiyerarşi komutları geçirir <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem2> arabirimleri. <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem.IsItemDirty%2A> Yöntemi öğesi değiştirilmiş olup olmadığını belirlemek için uygulanır. Öğe varsa, <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem.SaveItem%2A> yöntemi değiştirilmiş öğesini kaydetmek için uygulanır.

 Yöntemlerde `IVsPersistHierarchyItem2` arabirimi, öğeyi yeniden olup olmadığını ve öğeyi yeniden yüklemek olabilir, belirlemek için kullanılır. Ayrıca, <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem2.IgnoreItemFileChanges%2A> yöntemi neden olmadan kaydedilmesini atılması değiştirilen öğeleri için uygulanabilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [Yapılacaklar listesi: Yeni Proje Türleri Oluşturma](../../extensibility/internals/checklist-creating-new-project-types.md)
- [Proje Üreteçlerini Kullanarak Proje Örnekleri Oluşturma](../../extensibility/internals/creating-project-instances-by-using-project-factories.md)