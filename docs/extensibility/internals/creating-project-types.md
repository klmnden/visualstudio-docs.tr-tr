---
title: Proje türleri oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- project types, new
- projects [Visual Studio SDK], new project types
ms.assetid: bdb2d22e-d622-450c-bb2d-98152a745fcf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2c3d983da91fadbb0eb78eab6d0fa5bb02cca193
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62910013"
---
# <a name="create-project-types"></a>Proje türleri oluşturma
Genişletebileceğiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] oluşturarak yeni bir proje türü. Yeni bir proje türü oluşturmak için birkaç kavramları anlamanıza ve birkaç adımı tamamlamanız gerekir. Aşağıdaki konular, proje türleri oluşturma konusunda genel bir bakış sağlar.

## <a name="in-this-section"></a>Bu bölümde
- [Proje türü tasarım kararları](../../extensibility/internals/project-type-design-decisions.md)

 Öğesi, proje dosya kalıcılığına ve yeni bir proje türü oluşturmadan önce yapmanız taahhüt teknisyenin tasarım kararları açıklar.

- [Yapılacaklar listesi: Yeni proje türleri oluşturma](../../extensibility/internals/checklist-creating-new-project-types.md)

 Kod düzenleme ve derleme, derleme, hata ayıklama ve projenizdeki uygulamalarını dağıtma gibi programlama görevleri destekleyen yeni bir proje türü oluşturmak için izlemeniz gereken adımlara genel bir bakış sağlar.

- [Proje üreteçlerini kullanarak proje örnekleri oluşturma](../../extensibility/internals/creating-project-instances-by-using-project-factories.md)

 Sağlayın ve yeni bir proje örneklerini oluşturmak için bir proje fabrikası kullanma hakkında bilgi sağlar.

- [Bir proje türü kaydetme](../../extensibility/internals/registering-a-project-type.md)

 Kayıt betiği for each deyimi girişlerinden içeren varsayılan yolları ve verileri bir tablo sağlayan deyimler kayıt defterinden kod örneği sağlanmıştır.

- [Proje kalıcılığı](../../extensibility/internals/project-persistence.md)

 Kullanımı anlatılmaktadır `IPersistFileFormat` hem dosya hem de dosya tabanlı olmayan proje nesnelerini kalıcı hale getirmek için.

- [MSBuild kullanma](../../extensibility/internals/using-msbuild.md)

 Proje türüne nasıl kullanabileceğinizi açıklar [!INCLUDE[vstecmsbuild](../../extensibility/internals/includes/vstecmsbuild_md.md)] yapıdan kullanıcıların altyapısının yapı [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ve komut satırına.

## <a name="related-sections"></a>İlgili bölümler
- [Sembol tarama araçlarını destekler](../../extensibility/internals/supporting-symbol-browsing-tools.md)

 Kod araçları gibi görüntüleme mimarisini açıklar **Nesne Tarayıcısı** ve **sınıf görünümü** penceresi. VSPackage'ı nesne tarama uygulamak için kullanılan yöntemleri ve arabirimleri açıklar.

- [Proje ve proje öğesi şablonları ekleme](../../extensibility/internals/adding-project-and-project-item-templates.md)

 Bir proje öğesi açıldığında hangi Düzenleyicisi kullanılabilir saptanırken projeleri play önemi açıklanır ve proje kaynaklarını nasıl yönetilebilir.

- [Windows Installer ile VSPackage yükleme](../../extensibility/internals/installing-vspackages-with-windows-installer.md)

 Benzersiz kimliğini, VSPackage vermek ve bir Windows yükleyici paketinde, VSPackage DLL'ler ve diğer bilgileri sarmalama gösterir (*. MSI* dosyası) dağıtım müşterileriniz için.

- [Visual Studio’da Hiyerarşiler](../../extensibility/internals/hierarchies-in-visual-studio.md)

 Açıklayan nasıl [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] görünümleri ve adreslerini hiyerarşisi.

- [VSPackage’lar](../../extensibility/internals/vspackages.md)

 VSPackage, genişleten yüklenebilir bir COM nesnesi için genel bir bakış sağlar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ortam ve kendi VSPackage'ı uygulamak nasıl ele alınmaktadır.

- [Proje türleri](../../extensibility/internals/project-types.md)

 Projeleri kodu değiştirmek, derleme ve kod, derleme ve çalıştırma ve kod hatalarını ayıklamak için nasıl kullanılacağını açıklar ve proje türleri oluşturma konusunda ayrıntılı konulara bağlantılar sağlar.