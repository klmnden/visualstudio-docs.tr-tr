---
title: Proje özelliği kullanıcı arabirimi | Microsoft Docs
ms.date: 03/22/2018
ms.topic: conceptual
helpviewer_keywords:
- project properties [Visual Studio], user interface
- projects [Visual Studio SDK], properties UI
- project properties UI
ms.assetid: b6aec634-8533-476c-9ebd-36536a2288e2
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a83e5c9fb633322da536e62f1ba03484b965b162
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71252349"
---
# <a name="project-property-user-interface"></a>Proje Özelliği Kullanıcı Arabirimi

Proje alt türü, proje **Özellik sayfaları** iletişim kutusundaki öğeleri temel proje tarafından sağlandıklarında kullanabilir, yalnızca salt okuma denetimlerini ve tüm sayfaları gizler veya **Özellik sayfaları** iletişim kutusuna özgü sayfalar ekleyebilir. Kutudaki.

## <a name="extending-the-project-property-dialog-box"></a>Proje özelliği Iletişim kutusunu genişletme

Proje alt türü Otomasyon Genişleticilerini ve proje yapılandırma nesneleri 'ni uygular. Bu Extender 'lar, <xref:EnvDTE.IFilterProperties> belirli özellikleri gizli veya salt okunurdur hale getirmek için arabirimini uygular. Temel proje tarafından uygulanan temel projenin **Özellik sayfaları** iletişim kutusu, Otomasyon Genişleticileri tarafından gerçekleştirilen filtrelemeyi geliştirir.

**Proje özelliği** iletişim kutusunu genişletme işlemi aşağıda özetlenmiştir:

- Temel proje, <xref:EnvDTE80.IInternalExtenderProvider> arabirimini uygulayarak proje alt türünden Extender 'lar alır. Bu arabirimi Uygula ' ya kadar, Proje Otomasyonu ve temel projenin proje yapılandırma nesnelerine Gözat edin.

- Proje <xref:EnvDTE80.IInternalExtenderProvider> için uygulama, nesne ve Proje Otomasyonu nesne temsilcisine <xref:EnvDTE80.IInternalExtenderProvider> proje alt türü toplayıcısı `QueryInterface` ( <xref:EnvDTE80.IInternalExtenderProvider> <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> Yani, Proje nesnesi).

- Temel proje yapılandırması gezinme nesnesi Ayrıca, proje <xref:EnvDTE80.IInternalExtenderProvider> alt türü yapılandırma nesnesinden Otomasyon genişleticisini doğrudan bağlamak için de uygular. Uygulama, proje alt türü <xref:EnvDTE80.IInternalExtenderProvider> toplayıcısı tarafından uygulanan arabirime temsilciler.

- <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgBrowseObject.GetProjectItem%2A>Proje yapılandırması nesnesine göre uygulanan nesnesi, <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> nesnesini döndürür.

- <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgBrowseObject.GetCfg%2A>Ayrıca, proje yapılandırması nesnesi tarafından uygulanan <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfg> nesne, nesnesini döndürür.

- Proje alt türü, aşağıdaki <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2> değerleri alarak, çalışma zamanında temel projenin farklı Genişletilebilir nesnelerinin uygun kasalarını belirleyebilir:

  - <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2.VSHPROPID_ExtObjectCATID>

  - <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2.VSHPROPID_BrowseObjectCATID>

  - <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2.VSHPROPID_CfgBrowseObjectCATID>

Proje kapsamı için CATIDs 'yi belirlemekte, proje alt türü [Vsitemıd için yukarıdaki özellikleri alır. ](<xref:Microsoft.VisualStudio.VSConstants.VSITEMID#Microsoft_VisualStudio_VSConstants_VSITEMID_Root>) Kaynağından`VSITEMID typedef`kök. Proje alt türü Ayrıca, yapılandırma bağımlı ve yapılandırmaya bağımsız olarak proje için hangi **Özellik sayfaları** iletişim kutusu sayfalarının görüntülendiğini denetlemek isteyebilir. Bazı proje alt türleri, yerleşik sayfaları kaldırmak ve Project Subtype 'a özgü sayfaları eklemek zorunda kalabilir. Bunu etkinleştirmek için, yönetilen istemci projesi aşağıdaki özellikler için <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.GetProperty%2A> yöntemini çağırır:

- `VSHPROPID_PropertyPagesCLSIDList`— yapılandırma bağımsız özellik sayfalarının CLSID 'leri için noktalı virgülle ayrılmış bir liste.

- `VSHPROPID_CfgPropertyPagesCLSIDList —`yapılandırmaya bağlı özellik sayfalarının CLSID 'lerin noktalı virgülle ayrılmış listesi.

Proje alt türü <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> nesneyi topladığından, hangi **Özellik sayfaları** iletişim kutularının görüntülendiğini denetlemek için bu özelliklerin tanımını geçersiz kılabilir. Proje alt türü, bu özellikleri iç temel projeden alabilir ve ardından gerekirse CLSID 'leri ekleyebilir veya kaldırabilir.

Bir proje alt türü tarafından eklenen yeni özellik sayfaları, temel proje uygulamasından bir proje yapılandırması nesnesine sahiptir. Bu proje yapılandırma nesnesi Otomasyon Genişleticilerini destekler. Automationextender 'Lar hakkında daha fazla bilgi için bkz. [Otomasyon Genişleticilerini uygulama ve kullanma](https://msdn.microsoft.com/Library/0d5c218c-f412-4b28-ab0c-33a611f62356). Proje alt türü <xref:EnvDTE.Project.Extender%2A> tarafından uygulanan Özellik sayfaları, temel projenin yapılandırma Gözat nesnesini genişleten kendi proje alt tür yapılandırması nesnesine gözatabiliyor.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:EnvDTE.IFilterProperties>
- [Özellik sayfaları Iletişim kutusu](/previous-versions/visualstudio/visual-studio-2010/as5chysf(v=vs.100))
