---
title: Tasarımcıyı başlatma ve meta verileri yapılandırma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- designers [Visual Studio SDK], initializing
- designers [Visual Studio SDK], configuring metadata
ms.assetid: f7fe9a7e-f669-4642-ad5d-186b2e6e6ec9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4ed1852780e8045f298ed30f10ace5d971776294
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62864091"
---
# <a name="designer-initialization-and-metadata-configuration"></a>Tasarımcı başlatma ve meta verileri yapılandırma

Bir tasarımcı veya Tasarımcısı bileşen ile ilişkili meta verileri ve filtre özniteliklerini işleme uygulamalarının farklı işlemek için kullanılan araçlar tarafından belirli bir tasarımcı tanımlamak bir mekanizma sağlar <xref:System.Type> nesne (örneğin, veri yapıları sınıflar, veya grafik varlıkları) Tasarımcı kullanılabilir olduğunda ve Visual Studio IDE Tasarımcı destekleyecek şekilde nasıl yapılandırıldığını (örnek, **araç kutusu** kategori veya sekme bulunur).

[!INCLUDE[vsipsdk](../extensibility/includes/vsipsdk_md.md)] Denetim Tasarımcısı veya tasarımcı bileşenin başlatma ve meta verilerini bir VSPackage'ı tarafından işlenmesini kolaylaştırmak için çeşitli mekanizmalar sağlar.

## <a name="initialize-metadata-and-configuration-information"></a>Meta verileri ve yapılandırma bilgileri Başlat
 İsteğe bağlı olarak yüklenen olduklarından, VSPackages bir tasarımcı örneğinin önce Visual Studio ortamı tarafından yüklenmiş olabilir değil. VSPackage standart mekanizması bir tasarımcı veya tasarımcı bileşeni işlemek için olan oluşturma özelliğini yapılandırmak için bu nedenle, kullanamazsınız bir <xref:System.ComponentModel.Design.IDesignerEventService.DesignerCreated> olay. Bunun yerine, örneği bir VSPackage'ı uygulayan <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtension> arabirim ve kendi tasarım yüzeyi uzantıları başvurulan özelleştirmeleri sağlamak için kaydeder.

### <a name="customize-initialization"></a>Başlatma özelleştirme

Bir tasarımcı, bir bileşen veya bir tasarımcı yüzeyine özelleştirme içerir:

1. Tasarımcı meta verileri değiştirme ve belirli bir nasıl etkili bir şekilde değiştirme <xref:System.Type> erişilen veya dönüştürülür.

    Bu genellikle aracılığıyla yapılır <xref:System.Drawing.Design.UITypeEditor> veya <xref:System.ComponentModel.TypeConverter> mekanizmaları.

    Örneğin, <xref:System.Windows.Forms>-tabanlı tasarımcıları başlatılır, Visual Studio ortamını değiştirir <xref:System.Drawing.Design.UITypeEditor> için <xref:System.Web.UI.WebControls.Image> tasarımcı ile dosya sistemi yerine bit eşlemler almak için Kaynak Yöneticisi'ni kullanmak için kullanılan nesneleri.

2. Bir ortam gibi olaylara abone olma ya da proje yapılandırma bilgilerini elde etmeyi tümleştirme. Proje yapılandırma bilgilerini edinmek ve elde ederek olaylara abone <xref:System.ComponentModel.Design.ITypeResolutionService> arabirimi.

3. Uygun etkinleştirme tarafından kullanıcı ortamını değiştirilmesini **araç kutusu** kategorileri veya örneği uygulayarak tasarımcının Uygulanabilirlik kısıtlayarak <xref:System.ComponentModel.ToolboxItemFilterAttribute> sınıfı için tasarımcı.

### <a name="designer-initialization-by-a-vspackage"></a>VSPackage tarafından tasarımcıyı başlatma

VSPackage tarafından tasarımcıyı başlatma işlemesi gerekir:

1. Bir nesneyi uygulama oluşturma <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtension> sınıfı.

   > [!NOTE]
   > <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtension> Sınıfı hiçbir zaman uygulanmasını aynı nesne üzerinde <xref:Microsoft.VisualStudio.Shell.Package> sınıfı.

2. Uygulayan sınıfa kaydetme <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtension> olarak VSPackage'nın Tasarımcı uzantıları için destek sağlar. Sınıf örneklerini uygulayarak kaydetme <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtensionAttribute>, <xref:Microsoft.VisualStudio.Shell.ProvideObjectAttribute>, ve <xref:Microsoft.VisualStudio.Shell.ProvideServiceAttribute> VSPackage'nın uygulamasını sağlar sınıfını için <xref:Microsoft.VisualStudio.Shell.Package>.

Her bir tasarımcı veya Tasarımcısı bileşen oluşturulur, Visual Studio ortamı:

- Her kayıtlı tasarım yüzeyi uzantısı Sağlayıcısı'na erişir.

- Oluşturur ve her tasarım yüzeyi uzantısı sağlayıcısının bir örneğini başlatır <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtension> nesne.

- Her tasarım yüzeyi uzantısı sağlayıcısının çağırır <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtension.OnDesignerCreated%2A> yöntemi veya <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtension.OnComponentCreated%2A> yöntemi (hangisi uygunsa).

Uygularken <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtension> nesnesi bir VSPackage'ı bir üyesi olarak anlamak önemlidir:

- Visual Studio ortamında hangi meta verileri herhangi bir denetime sağlamaz veya belirli bir diğer yapılandırma ayarlarını `DesignSurfaceExtension` sağlayıcısının değiştirir. İki veya daha fazla mümkündür `DesignSurfaceExtension` aynı Tasarımcısı özelliğiyle kesin olan son değişikliği ile çakışan yollarla değiştirme sağlayıcıları. Hangi değişiklik son uygulanan da belirsiz.

- Açıkça uygulaması kısıtlamak mümkündür <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtension> nesne örneklerini uygulayarak belirli tasarımcılarına <xref:System.ComponentModel.ToolboxItemFilterAttribute> bu uygulama için. Daha fazla bilgi için **araç kutusu** öğesi filtreleme için bkz: <xref:System.ComponentModel.ToolboxItemFilterAttribute> ve <xref:System.ComponentModel.ToolboxItemFilterType>.

## <a name="additional-metadata-provisioning"></a>Ek meta veri sağlama

VSPackage tasarım zamanında bir tasarımcı veya dışında Tasarımcısı bileşen yapılandırmasını değiştirebilirsiniz.

<xref:Microsoft.VisualStudio.Shell.Design.ProvideDesignerMetadataAttribute> Sınıfı kullanılan program aracılığıyla ya da bir tasarımcı sağlayan bir Vspackage'e uygulanır.

Örneği <xref:Microsoft.VisualStudio.Shell.Design.ProvideDesignerMetadataAttribute> sınıfı, bir tasarım yüzeyi üzerinde oluşturulan bileşenleri meta verilerini değiştirmek için kullanılır. Örneğin, biri tarafından kullanılan varsayılan özellik tarayıcısını yerini alabilir <xref:System.Windows.Forms.CommonDialog> bir özel özellik tarayıcısı nesneleri.

Örneği tarafından sağlanan değişiklikleri <xref:Microsoft.VisualStudio.Shell.Design.ProvideDesignerMetadataAttribute> uygulanmasına VSPackage'nın uygulanan <xref:Microsoft.VisualStudio.Shell.Package> iki kapsamların biri olabilir:

- Genel--için belirli bir bileşenin tüm yeni örnekleri

- Yerel--yalnızca geçerli VSPackage'ı tarafından sağlanan bir tasarım yüzeyi üzerinde oluşturulan bileşeninin örneği tıklarsınız.

`IsGlobal` Özelliği <xref:Microsoft.VisualStudio.Shell.Design.ProvideDesignerMetadataAttribute> uygulanmasına VSPackage'nın uygulanan örneği <xref:Microsoft.VisualStudio.Shell.Package> bu kapsamı belirler.

Öznitelik bir uygulama için uygulama <xref:Microsoft.VisualStudio.Shell.Package> ile <xref:Microsoft.VisualStudio.Shell.Design.ProvideDesignerMetadataAttribute.IsGlobal%2A> özelliği <xref:Microsoft.VisualStudio.Shell.Design.ProvideDesignerMetadataAttribute> nesne kümesine `true`, aşağıda, tüm Visual Studio ortamı için tarayıcı değiştirir:

`[ProvideDesignerMetadata(typeof(Color), typeof(CustomBrowser),`   `IsGlobal=true`  `)]`

`internal class MyPackage : Package {}`

Genel Bayrak olarak ayarlandı, `false`, meta veri değişikliği geçerli VSPackage'ı tarafından desteklenen geçerli Tasarımcı için yerel ise:

`[ProvideDesignerMetadata(typeof(Color), typeof(CustomBrowser),`   `IsGlobal=false`  `)]`

`internal class MyPackage : Package {}`

> [!NOTE]
> Tasarım yüzeyine bileşenler oluşturma yalnızca destekler ve bu nedenle yalnızca bileşenleri yerel meta verilerine de sahip. Yukarıdaki örnekte, biz bir özelliği değiştirmek çalıştığınız `Color` özelliği bir nesne. Varsa `false` genel bayrak için geçirilen `CustomBrowser` Tasarımcı örneği asla gerçekten oluşturur çünkü hiçbir zaman görüneceği `Color`. Genel Bayrak ayarlayarak `false` denetimleri, zamanlayıcılar ve iletişim kutuları gibi bileşenleri için kullanışlıdır.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtension>
- <xref:Microsoft.VisualStudio.Shell.Design.DesignSurfaceExtensionAttribute>
- <xref:System.ComponentModel.ToolboxItemFilterType>
- [Tasarım zamanı desteğini genişletmek](https://msdn.microsoft.com/Library/d6ac8a6a-42fd-4bc8-bf33-b212811297e2)