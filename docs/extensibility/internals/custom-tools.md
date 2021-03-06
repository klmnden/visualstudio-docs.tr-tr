---
title: Özel Araçlar | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSPackages, custom tools
- tools [Visual Studio], custom
- custom tools
ms.assetid: d669f154-9b23-48b6-b9f6-7419c8dd61a6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f9bad62d071fd7c2ef6e0a7c1f5500a5fccb18e0
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66312259"
---
# <a name="custom-tools"></a>Özel Araçlar
*Özel Araçlar* bir aracı bir projede bir öğe ile ilişkilendirmek ve dosyanın kaydedildiği zaman bu aracı sağlar. Bazı özel araçları, bazen olarak adlandırılan *tek dosya oluşturucular*, verilerden ve kod oluşturma çevirmenler uygulamak için sıkça kullanılır. Örneğin, tek dosya oluşturucular oluşturma [!INCLUDE[csprcs](../../data-tools/includes/csprcs_md.md)] ve [!INCLUDE[vbprvb](../../code-quality/includes/vbprvb_md.md)] kaynak kodunun dışında *.settings* ve *.resx* dosyaları. Oluşturulan kaynak kod verilere erişim türü kesin belirlenmiş sağlar *.settings* ve *.resx* dosyaları. [!INCLUDE[csprcs](../../data-tools/includes/csprcs_md.md)] Ve [!INCLUDE[vbprvb](../../code-quality/includes/vbprvb_md.md)] özel araçlar; proje türleri desteği [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] proje türleri yapın. Özel Araçlar kendi proje türleri de destekler.

 Özel Araçlar, uygulama kayıtlı bileşenleridir `IVsSingleFileGenerator` arabirimi.

 Özel araçlar ile ilişkili bir `ProjectItem` arabirimi nesnesi ve tasarımcılar ve düzenleyiciler gibi. Özel bir araç tarafından temsil edilen dosya alan bir `ProjectItem` olarak giriş ve dosya adı tarafından sağlanır, yeni bir dosya Yazar `DefaultExtension` yöntemi.

## <a name="in-this-section"></a>Bu bölümde
- [Tek dosya oluşturucuları uygulayın](../../extensibility/internals/implementing-single-file-generators.md)

 Nasıl kullanılacağını açıklar <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator> özel araç uygulamak için arabirim.

- [Tek dosya oluşturucuları kaydetme](../../extensibility/internals/registering-single-file-generators.md)

 Tüm kayıt defteri girdilerini açıklamaları için özel bir araç sağlar.

- [Türleri görsel tasarımcıların kullanıma sunma](../../extensibility/internals/exposing-types-to-visual-designers.md)

 Nasıl proje sistemleri görsel tasarımcılar erişim üretilen sınıfları ve türleri için geçici taşınabilir yürütülebilir (PE) dosyaları desteği açıklanmaktadır.

- [Proje öğesinin özelliğini kalıcı](../../extensibility/persisting-the-property-of-a-project-item.md)

 Proje dosyasındaki bir kaynak dosyasının yazar gibi bir proje öğesi özelliği kalıcı hale getirmek gösterilmektedir.

## <a name="reference"></a>Başvuru
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator> Hakkında ayrıntılar sağlar <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator>, hangi dönüştüren tek bir giriş dosyası derlenmiş veya bir projeye eklenen bir tek çıkış dosyasına.

 <xref:EnvDTE.ProjectItem> Açıklar `ProjectItem` bir projedeki bir öğeyi temsil eden arabirim.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator.DefaultExtension%2A> Hakkında ayrıntılar sağlar `DefaultExtension` yöntemi için çıkış dosyası adı verilen dosya adı uzantısını alır.

## <a name="related-sections"></a>İlgili bölümler
- [Projeleri genişletme](../../extensibility/extending-projects.md)

 Nasıl kullanılacağını açıklar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] projeler ve çözümler, kod dosyaları ve kaynak dosyalarını ve kaynak denetimi uygulamak nasıl düzenlemek için.