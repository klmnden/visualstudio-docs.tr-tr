---
title: VSPackage yapısı (kaynak denetimi VSPackage'ı) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSPackages, structure
- source control packages, VSPackage overview
ms.assetid: 92722be7-b397-48c3-a7a7-0b931a341961
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 83e8207ffb52fd41c82eac896611f7454bd7379d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53874686"
---
# <a name="vspackage-structure-source-control-vspackage"></a>VSPackage Yapısı (Kaynak Denetimi VSPackage’ı)

Kaynak denetimi paket SDK kendi kaynak denetimi işlevlerini Visual Studio ortamıyla tümleştirmek bir kaynak denetimi uygulayan bir VSPackage'ı oluşturma yönergeleri olanak sağlar. VSPackage genellikle isteğe bağlı olarak, kayıt defteri girdileri paket tarafından tanıtılan Hizmetleri temel Visual Studio tümleşik geliştirme ortamı (IDE) tarafından yüklenen bir COM bileşenidir. Her VSPackage'ı uygulamalıdır <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage>. VSPackage genellikle Visual Studio IDE tarafından sunulan hizmetler tüketir ve bazı hizmetler kendi proffers.

VSPackage kendi menü öğeleri bildirir ve varsayılan öğe durumu .vsct dosyası aracılığıyla oluşturur. Visual Studio IDE, VSPackage yüklenene kadar bu durumda menü öğelerini görüntüler. Sonuç olarak, VSPackage'nın uygulaması <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus%2A> etkinleştirmek ya da menü öğelerini devre dışı yöntemi çağrılır.

## <a name="source-control-package-characteristics"></a>Kaynak denetimi paket özellikleri

Kaynak denetimi VSPackage'ı Visual Studio'ya derin şekilde tümleşiktir. VSPackage semantiği şunlardır:

-   VSPackage'ı olan da uygulanacak arabirim ( `IVsPackage` arabirimi)

-   Komut kullanıcı Arabirimi uygulama (.vsct dosyası ve uygulaması <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> arabirimi)

-   Visual Studio ile VSPackage kaydı.

Kaynak denetimi VSPackage'ı bu diğer Visual Studio varlıkların ile iletişim kurması gerekir:

-   Projeler

-   Düzenleyiciler

-   Çözümler

-   Windows

-   Çalıştırılan Belge tablosu

### <a name="visual-studio-environment-services-that-may-be-consumed"></a>Tüketilebilir visual Studio ortamını Hizmetleri

<xref:Microsoft.VisualStudio.Shell.Interop.SVsShell>

<xref:Microsoft.VisualStudio.Shell.Interop.SVsUIShell>

<xref:Microsoft.VisualStudio.Shell.Interop.SVsSolution>

SVsRegisterScciProvider hizmeti

<xref:Microsoft.VisualStudio.Shell.Interop.SVsQueryEditQuerySave>

<xref:Microsoft.VisualStudio.Shell.Interop.SVsTrackProjectDocuments>

<xref:Microsoft.VisualStudio.Shell.Interop.SVsSccManager>

### <a name="vsip-interfaces-implemented-and-called"></a>Uygulanan ve adlı VSIP arabirimleri

Kaynak denetimi VSPackage paketidir ve bu nedenle, doğrudan Visual Studio ile kayıtlı diğer VSPackages etkileşim kurabilir. Kaynak denetimi işlevlerini teknolojilerimizden sağlamak için kaynak denetimi VSPackage'ı projeleri veya kabuk tarafından sağlanan arabirimlerle giderebilirsiniz.

Her proje Visual Studio'da uygulamalıdır <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3> Visual Studio IDE içinde bir proje olarak kabul edilecek. Ancak, bu arabirimi değil özel kaynak denetimi için yeterli. Altında bir kaynak olarak beklenen projelerini denetleyecek uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProject2>. Bu arabirim içeriği için bir proje sorgulamak ve karakterleri ve bağlama bilgileri (sunucu konumu ve disk konumu altında olan proje arasında bağlantı kurmak için gereken bilgileri sağlamak için kaynak denetimi VSPackage'ı tarafından kullanılır Kaynak Denetimi).

Kaynak denetimi VSPackage'ı uygulayan <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2>, sırayla sağlayan kendileri için kaynak denetimi kaydedin ve bunların durumunu karakterleri almak proje.

Kaynak denetimi VSPackage'ı dikkate almanız gereken arabirimleri tam bir listesi için bkz. [ilgili hizmetler ve arabirimler](../../extensibility/internals/related-services-and-interfaces-source-control-vspackage.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Tasarım Öğeleri](../../extensibility/internals/source-control-vspackage-design-elements.md)
- [İlgili Hizmetler ve Arabirimler](../../extensibility/internals/related-services-and-interfaces-source-control-vspackage.md)