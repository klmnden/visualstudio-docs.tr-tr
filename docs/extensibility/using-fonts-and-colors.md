---
title: Yazı tipleri ve renkler kullanarak | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- fonts, controlling in IDE
- IDE, controlling text color and fonts
- Fonts and Colors property page
- font and color control [Visual Studio SDK]
- text, IDE
ms.assetid: d1a9b99f-fbdc-45ed-920a-e08c3d931ac9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 96abe68838d028c5de9d6d9418e94ba5b46c0f76
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62432305"
---
# <a name="using-fonts-and-colors"></a>Yazı tipleri ve renkler kullanma
[!INCLUDE[vsipsdk](../extensibility/includes/vsipsdk_md.md)] Metni görüntülemek için yazı tiplerini ve renklerini kullanma desteği sağlar.

## <a name="in-this-section"></a>Bu Bölümde
- [Yazı tipi ve renk genel bakış](../extensibility/font-and-color-overview.md) metin yazı tipi ve renk ayarları açıklanır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı (IDE). Ayrıca kategorileri ve görüntü öğeleri kavramlar tanıtılır ve VSPackages ve çekirdek düzenleyici metin özniteliklerini kullanımını açıklar.

- [Metin renklendirmesi için yazı tipi ve renk bilgilerini alma](../extensibility/getting-font-and-color-information-for-text-colorization.md) metin renklendirmesi yönetme Vspackage'larda uygulamak için kılavuz bilgiler verilmektedir **kategorileri** dışında **metin düzenleyici**.

- [Depolanan yazı tipi ve renk ayarlarını erişme](../extensibility/accessing-stored-font-and-color-settings.md) açıklanmaktadır geçerli yazı tipi ve renk ayarlarını depolanabilir nasıl alınır ve uygulanır.

- [Uygulama özel kategoriler ve öğeleri görüntüle](../extensibility/implementing-custom-categories-and-display-items.md) kullandığı bir pencere oluşturabilir ve kullanmak, kendi temel adımlar açıklanmıştır **öğeleri görüntüle** ve **kategorileri** metin görüntülenmesini desteklemek için.

 VSPackage'ı uygulamak bu yaklaşım gerektirir <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaultsProvider> ve ilgili arabirim.

- [Nasıl yapılır: Yerleşik yazı tipi ve renk şeması erişim](../extensibility/how-to-access-the-built-in-fonts-and-color-scheme.md) tanımlayın ve bir kategori yerleşik yazı tipleri ve renkler kullanarak kaydetmek ve sistem tarafından sağlanan yazı tipleri ve renkler kullanımı başlatmak nasıl ele alınmaktadır.

## <a name="reference"></a>Başvuru
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaultsProvider> Bir örneğini sağlar `IVsFontAndColorDefaults` veya <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorGroup> listelenen belirli bir öğe için karşılık gelen arabirimi **ayarları için Göster** listesinde **yazı tipleri ve renkler** sayfasının**Seçenekleri** iletişim kutusu.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults> IDE desteklemek bir VSPackage sağlayan **yazı tipleri ve renkler** varsayılan yazı tipleri ve renkler penceresi veya kullanıcı Arabirimi bileşeninin tanımlayarak sayfası.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorGroup> Kullandığı bir mekanizma sağlar, yazı tipi ve renk desteği, bir görüntü öğesi grubu - iki veya daha fazla kategori birleşimi temsil eden bir süper kategorisi belirtebilirsiniz sağlayan bir VSPackage'ı.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorStorage> Yazı tipi ve renk verileri almak veya kayıt defterine kaydetmek bir VSPackage sağlar.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorEvents> Değişiklikler hakkında bilgi yazı tipi ve renk yazı tipi ve renk ayarlarını kullanan VSPackages bildirir.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorUtilities> Yöntemleri tarafından kullanılan giriş ve çıkış verilerle çalışmaya yönelik araçlar sağlar [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] **yazı tipi ve renk** mekanizması.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorCacheManager> Önbelleğe alma yazı tipi ve renk ayarlarını denetler.

## <a name="related-sections"></a>İlgili Bölümler
- [Eski dil hizmeti geliştirme](../extensibility/internals/developing-a-legacy-language-service.md) VSPackages özelleştirmek için dil hizmetleri nasıl kullanabileceğinizi anlatır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Düzenleyici.

- [Özel düzenleyicilerde söz dizimi renklendirmesi](../extensibility/syntax-coloring-in-custom-editors.md) Descries nasıl [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Düzenleyicisi söz dizimi renklendirmesi uygulamak için dil Hizmetleri kullanır.

- [Visual Studio'nun diğer bölümlerini genişletme](../extensibility/extending-other-parts-of-visual-studio.md) nasıl kullanılacağını açıklar [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] geri kalanını eşleşen kullanıcı Arabirimi öğeleri oluşturmak için Sertifika Hizmetleri'ni [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].