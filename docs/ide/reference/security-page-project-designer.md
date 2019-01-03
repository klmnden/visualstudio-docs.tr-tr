---
title: Güvenlik Sayfası, Proje Tasarımcısı
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- vb.ProjectPropertiesSecurity
- vb.XBAPProjectPropertiesSecurity
helpviewer_keywords:
- Project Designer, Security page
- Security page in Project Designer
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 30b09fee21dd7f028615612c27c3aab468a22055
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53987959"
---
# <a name="security-page-project-designer"></a>Güvenlik Sayfası, Proje Tasarımcısı

**Güvenlik** sayfasının **Proje Tasarımcısı** kullanılarak dağıtılan uygulamalar için kod erişim güvenlik ayarlarını yapılandırmak için kullanılan [!INCLUDE[ndptecclick](../../deployment/includes/ndptecclick_md.md)] dağıtım. Daha fazla bilgi için [ClickOnce uygulamaları için kod erişimi güvenliği](../../deployment/code-access-security-for-clickonce-applications.md).

 Erişim için **güvenlik** sayfasında, bir proje düğümünde **Çözüm Gezgini**ve ardından **proje** menüsünde tıklayın **özellikleri**. Zaman **Proje Tasarımcısı** görünen tıklayın **güvenlik** sekmesi.

## <a name="security-settings"></a>Güvenlik ayarları

 **ClickOnce güvenlik ayarlarını etkinleştirme**

 Güvenlik ayarları tasarım zamanında etkin olup olmadığını belirler. Ne zaman bu seçenek işaretli değilse, diğer tüm seçenekler üzerinde **güvenlik** sayfası kullanılamıyor.

> [!NOTE]
> Kullanarak bir uygulama yayımladığınızda **Yayımla** sihirbazında, bu seçenek otomatik olarak etkinleştirilir.


 Bu seçeneği belirlediğinizde, iki radyo düğmelerinden birini seçme seçeneğiniz vardır: **Tam güven uygulamasıdır** veya **kısmi güven uygulamasıdır**.

 WPF Web tarayıcı uygulaması projeleri için varsayılan olarak bu seçenek seçilidir.

 Varsayılan olarak, diğer proje türleri için bu seçeneği temizlenir.

 **Tam güven uygulamasıdır**

 Bu seçeneği belirlerseniz, uygulama yüklendiğinde veya bir istemci bilgisayarda çalışması tam güven izinleri ister. Önlemek uygulamanızı verilir çünkü tam güven mümkünse kullanarak sınırsız erişim dosya sistemini ve kayıt defteri gibi kaynaklara bağlayabilirsiniz.

 WPF Web tarayıcı uygulaması projeleri için varsayılan olarak bu seçenek, kısmi güven için ayarlanır.

 Varsayılan olarak, diğer proje türleri için tam güven için bu seçeneği ayarlanır.

 **Kısmi güven uygulamasıdır**

 Bu seçeneği belirlerseniz, uygulama yüklendiğinde veya bir istemci bilgisayarda çalışması kısmi güven izinleri ister. *Kısmi güven* istenen kod erişimi güvenliği izinleri altında izin verilen eylemleri anlamına gelir. Güvenlik izinlerini yapılandırma hakkında daha fazla bilgi için bkz. [ClickOnce uygulamaları için kod erişimi güvenliği](../../deployment/code-access-security-for-clickonce-applications.md).

 Kısmi güven güvenliği ayarları seçenekleri yapılandırarak belirtebilirsiniz **ClickOnce güvenlik izinleri** alan.

## <a name="clickonce-security-permissions"></a>ClickOnce güvenlik izinleri

 **Bölge, uygulama yüklenir**

 Kod erişimi güvenliği izinleri varsayılan kümesini belirtir. Seçin **Internet** veya **yerel Intranet** sınırlı bir izin kümesi veya seçin **(özel)** özel izin yapılandırmak için ayarlayın. Uygulama bir bölgede verilen çok daha fazla izne isterse, ek izinler vermek son kullanıcı için bir ClickOnce güven istemi görünür. Güvenlik izinlerini yapılandırma hakkında daha fazla bilgi için bkz. [ClickOnce uygulamaları için kod erişimi güvenliği](../../deployment/code-access-security-for-clickonce-applications.md).

 Varsayılan olarak WPF Web tarayıcı uygulaması projeleri için bu seçeneği ayarlanır **Internet**.

 **XML izinleri Düzenle**

 İzinleri yapılandırmak için uygulama bildirim şablonu (app.manifest) için açılır **(özel)** izin kümesi.

 **Gelişmiş**

 Açılır [Gelişmiş Güvenlik Ayarları iletişim kutusu](../../ide/reference/advanced-security-settings-dialog-box.md), sınırlı izinler ile uygulamasında hata ayıklama için ayarları yapılandırmak için kullanılır. Bu ayarlar, hata ayıklama sırasında denetlenir ve uygulamanızı bir bölge içinde tanımlanan daha fazla izin gerekebilir izni özel durumları gösterir.

## <a name="see-also"></a>Ayrıca Bkz.

- <xref:System.Security.Permissions.WebBrowserPermission>
- <xref:System.Security.Permissions.MediaPermission>
- [ClickOnce Uygulamaları İçin Kod Erişimi Güvenliği](../../deployment/code-access-security-for-clickonce-applications.md)
- [Nasıl yapılır: ClickOnce güvenlik ayarlarını etkinleştirme](../../deployment/how-to-enable-clickonce-security-settings.md)
- [Nasıl yapılır: ClickOnce uygulaması için bir güvenlik bölgesi ayarlama](../../deployment/how-to-set-a-security-zone-for-a-clickonce-application.md)
- [Nasıl yapılır: ClickOnce uygulaması için özel izinleri ayarlama](../../deployment/how-to-set-custom-permissions-for-a-clickonce-application.md)
- [Nasıl yapılır: Sınırlı izinler ile ClickOnce uygulamasında hata ayıklama](../../deployment/how-to-debug-a-clickonce-application-with-restricted-permissions.md)
- [ClickOnce Güvenliği ve Dağıtımı](../../deployment/clickonce-security-and-deployment.md)
- [Proje Özellikleri Başvurusu](../../ide/reference/project-properties-reference.md)
- [Gelişmiş Güvenlik Ayarları İletişim Kutusu](../../ide/reference/advanced-security-settings-dialog-box.md)