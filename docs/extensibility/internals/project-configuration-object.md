---
title: Proje yapılandırması nesnesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- project configurations, object
- objects, project configuration
ms.assetid: 877756c9-4261-43d9-9f32-51bf06b4219f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9460a30e63a7d2c282bf537517016dfa5f790a1e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66328432"
---
# <a name="project-configuration-object"></a>Proje Yapılandırması Nesnesi
Proje yapılandırması nesnesi yapılandırma bilgileri için kullanıcı Arabiriminde görünen yönetir.

 ![Visual Studio Proje yapılandırması](../../extensibility/internals/media/vsprojectcfg.gif "vsProjectCfg") proje yapılandırma özelliği sayfaları

 Proje yapılandırma sağlayıcısı, proje yapılandırmalarını yönetir. Ortamı ve ve bir projenin yapılandırmalar hakkında bilgi almak için proje yapılandırma sağlayıcısı nesnesine bağlı arabirimler çağrı erişim elde etmek için diğer paketleri.

> [!NOTE]
> Oluşturamaz veya program aracılığıyla çözüm yapılandırma dosyalarını düzenleyebilirsiniz. Kullanmalısınız `DTE.SolutionBuilder`. Bkz: [çözüm yapılandırması](../../extensibility/internals/solution-configuration.md) daha fazla bilgi için.

 Kullanıcı Arabirimi yapılandırmasında kullanılacak bir görünen ad yayımlamak için projenizi uygulamalıdır <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfg.get_DisplayName%2A>. Ortam çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2.GetCfgs%2A>, listesini döndürür `IVsCfg` ortamın kullanıcı Arabiriminde listelenecek yapılandırma ve Platform bilgileri için görünen adları almak için kullanabileceğiniz işaretçileri. Etkin yapılandırma ve platform etkin çözüm yapılandırmasındaki, depolanan projenin yapılandırması tarafından belirlenir. <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionBuildManager.FindActiveProjectCfg%2A> Yöntemi, etkin proje yapılandırmasını almak için kullanılabilir.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectCfgProvider> Nesne isteğe bağlı olarak uygulanabilir üzerinde <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2> nesnesi ile <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProviderEventsHelper> nesne almanızı sağlayacak bir `IVsProjectCfg2` nesne kurallı proje yapılandırma adına bağlı.

 Bir uygulamasını sağlamak üzere, projeler için ortam ve diğer projeler için proje yapılandırmalarını erişmesini sağlamak için başka bir yolu ise `IVsCfgProvider2::GetCfgs` bir veya daha fazla yapılandırma nesneleri döndürmek için yöntemi. Projeleri de uygulayabilir <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectCfg2>, işlevinden devralan `IVsProjectCfg` ve böylece `IVsCfg`, yapılandırmaya özgü bilgileri sağlamak için. <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2> platformlar ve işlevselliği ekleme, silme ve yeniden adlandırma proje yapılandırmaları destekler.

> [!NOTE]
> Visual Studio için iki yapılandırma türü sınırlı artık yapılandırmaları işleyen kodu değil yazılması varsayımlar ile yapılandırmaları sayısı hakkında ya da varsayımıyla yazılmalıdır bu yana, tek sahip bir proje yapılandırma, hata ayıklama veya perakende mutlaka olması. Bu kullanımını kolaylaştırır <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfg.get_IsReleaseOnly%2A> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfg.get_IsDebugOnly%2A> artık kullanılmıyor.

 Çağırma `QueryInterface` yönteminden döndürülen nesne üzerinde`IVsGetCfgProvider::GetCfgProvider` alır `IVsCfgProvider2`. Varsa `IVsGetCfgProvider` çağırarak bulunamadı `QueryInterface` üzerinde `IVsProject3` proje nesne, çağırarak yapılandırma sağlayıcısı nesnesi erişebilir `QueryInterface` için döndürülen nesne hiyerarşisi kök tarayıcı nesnede `IVsHierarchy::GetProperty(VSITEM_ROOT, VSHPROPID_BrowseObject)`, aracılığıyla veya bir yapılandırma sağlayıcısı için döndürülen işaretçiye `IVsHierarchy::GetProperty(VSITEM_ROOT, VSHPROPID_ConfigurationProvider)`.

 `IVsProjectCfg2` öncelikli olarak dağıtım yönetim nesneleri ve derleme, hata ayıklama erişim sağlar ve projeleri grup çıkışları özgürlüğü sağlar. Yöntemlerinin `IVsProjectCfg` ve `IVsProjectCfg2` uygulamak için kullanılan <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildableProjectCfg> derleme işlemini yönetmek için ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputGroup> yapılandırmasının çıktı grupları için işaretçiler.

 Proje grupları yapılandırma yapılandırması bir grup içinde bulunan çıktı sayısı değişebilir olsa bile desteklediği her bir yapılandırma için aynı sayıda döndürmesi gerekir. Grupları da aynı tanımlayıcı bilgileri (kurallı ad, görünen ad ve grup bilgilerini) yapılandırma yapılandırması bir proje içinde olmalıdır. Daha fazla bilgi için [çıkış için proje yapılandırması](../../extensibility/internals/project-configuration-for-output.md).

 Hata ayıklamayı etkinleştirmek için yapılandırmalarınızı uygulamalıdır <xref:Microsoft.VisualStudio.Shell.Interop.IVsDebuggableProjectCfg>. `IVsDebuggableProjectCfg` bir yapılandırma başlatmak için hata ayıklayıcı izin vermek için projeleri tarafından uygulanan isteğe bağlı bir arabirim ve ile yapılandırma nesne üzerinde uygulanan `IVsCfg` ve `IVsProjectCfg`. F5 tuşuna basarak hata ayıklayıcıyı başlatmak seçtiğinde ortam onu çağırır.

 `ISpecifyPropertyPages` ve `IDispatch` özellik sayfaları ile birlikte alma ve yapılandırma bağımlı bilgileri kullanıcıya göstermek için kullanılır. Daha fazla bilgi için [özellik sayfaları](../../extensibility/internals/property-pages.md).

## <a name="see-also"></a>Ayrıca Bkz.
- [Yapılandırma Seçeneklerini Yönetme](../../extensibility/internals/managing-configuration-options.md)
- [Derleme için Proje Yapılandırması](../../extensibility/internals/project-configuration-for-building.md)
- [Çıkış için Proje Yapılandırması](../../extensibility/internals/project-configuration-for-output.md)
- [Özellik Sayfaları](../../extensibility/internals/property-pages.md)
- [Çözüm Yapılandırması](../../extensibility/internals/solution-configuration.md)