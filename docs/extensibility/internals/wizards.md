---
title: Sihirbazlar | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], providing wizard support
ms.assetid: 59d9a77f-ee80-474b-a14f-90f477ab717b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ad90c1ec332c2f214514e660b27dc5a915485f99
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62856726"
---
# <a name="wizards"></a>Sihirbazlar
Bir sihirbaz oluşturduktan sonra genellikle eklemek istediğiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] başkalarının da kullanabilmesi için tümleşik geliştirme ortamı (IDE). Eklenen Sihirbazı ardından görünür **Yeni Proje Ekle** veya **Yeni Öğe Ekle** iletişim kutuları. Görmek için **Yeni Proje Ekle** veya **Yeni Öğe Ekle** iletişim kutuları, sağ tıklayın, açık bir çözümde **Çözüm Gezgini**, işaret **Ekle**, ve ardından **yeni proje** veya **yeni öğe**.

 Sihirbazlar uygulanabilir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] kullanıcıların bir ağaç görünümünü açtıklarında kullanılabilir değerler arasından seçim **Yeni Proje Ekle** iletişim kutusu veya **Yeni Öğe Ekle** iletişim kutusu veya ne zaman sağ bir öğeyi **Çözüm Gezgini**.

 Sihirbazı, yeni bir proje veya ites adını yerelleştirme seçeneği sağlar ve bunlar Sihirbazı'nı seçtiğinizde, kullanıcıların göreceği simgesi belirleyebilirsiniz. Ayrıca yeni öğeler kullanılabilir diğer öğeleri göre görünme sırasını denetleyebilirsiniz: Öğeleri alfabetik olarak düzenlenmiş gerekmez.

 Açıldığında, sihirbaza geçirilir özel parametrelere göre farklı şekilde başlayan bir Sihirbazı da sağlayabilirsiniz.

 Bu bölümdeki konular, neden kullanan dosyalarının tartışmak [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] **Yeni Proje Ekle** ve **Yeni Öğe Ekle** kullanılabilir sihirbazları ve şablonlar arasındaki Sihirbazı'nı listelemek için iletişim kutuları ve Sihirbazı IDE'de düzgün çalışması için karşılaması gereken gereksinimleri.

## <a name="in-this-section"></a>Bu Bölümde
- [Şablon Dizin Açıklaması (.Vsdir) Dosyaları](../../extensibility/internals/template-directory-description-dot-vsdir-files.md)

 Dizin tanımı dosyaları şablonu genel bir bakış sağlar ve bunların klasörleri, sihirbaz .vsz dosyasına ve iletişim kutularında bir proje ile ilişkili şablon dosyaları görüntülemek için IDE içindeki işlevleri açıklanmaktadır.

- [Sihirbaz (.Vsz) Dosyası](../../extensibility/internals/wizard-dot-vsz-file.md)

 Nasıl sihirbazları IDE başlatıldığında açıklar ve üç .vsz dosyasının bölümlerini listeler.

- [Sihirbaz Arabirimi (IDTWizard)](../../extensibility/internals/wizard-interface-idtwizard.md)

 Açıklar `IDTWizard` sihirbazlar IDE içinde çalışacak şekilde uygulamalıdır arabirimi.

- [Bağlam Parametreleri](../../extensibility/internals/context-parameters.md)

 Sihirbazlar nasıl uygulandığını ve IDE, uygulama için bağlam parametreleri başarılı olduğunda ne olacağını açıklar.

- [Özel Parametreler](../../extensibility/internals/custom-parameters.md)

 Özel Parametreler sihirbaz başlatıldıktan sonra sihirbazın işlemi denetlemek için kullanmayı açıklar.

## <a name="related-sections"></a>İlgili Bölümler
- [Proje Türleri](../../extensibility/internals/project-types.md)

 Yeni proje türleri tasarımı hakkında bilgi sağlayan ek konulara bağlantılar sağlar.

- [Projeleri Genişletme](../../extensibility/extending-projects.md)

 Nasıl kullanılacağını açıklar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] projeler ve çözümler, kod dosyaları ve kaynak dosyalarını ve kaynak denetimi uygulamak nasıl düzenlemek için.