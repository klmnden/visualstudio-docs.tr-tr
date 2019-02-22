---
title: Proje alt türleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], subtypes
- project subtypes [Visual Studio SDK]
ms.assetid: d235b47b-cf11-4d47-a63f-e33d9d16105d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 027dc559c33b5b8f10a4555985e8b2a5a5a416c5
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56604944"
---
# <a name="project-subtypes"></a>Proje Alt Türleri
Proje alt türleri özelleştirebilirsiniz veya proje sistemleri davranışını flavor izin [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Özelleştirmeleri içeren proje dosyasında ekleme veya öğeleri filtreleme ek veri kaydetme **Yeni Öğe Ekle** iletişim kutusunda, derlemeleri nasıl hata ayıklama ve dağıtılan, denetleme ve proje genişletme **özelliği Sayfaları** iletişim kutusu. VSPackage proje alt türleri COM toplama kullanarak uygulayın.

> [!NOTE]
>  Visual C++ proje sistemi proje alt türleri desteklemez. [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Proje alt türleri kendi SQL Server ve akıllı cihaz projeleri uygulamak için kullanır.

## <a name="in-this-section"></a>Bu Bölümde
- [Proje Alt Türleri Tasarımı](../../extensibility/internals/project-subtypes-design.md)

 Proje alt türleri kavramını açıklar.

- [Proje Alt Türlerinin Başlatılma Sırası](../../extensibility/internals/initialization-sequence-of-project-subtypes.md)

 Programlı proje alt başlatma sırası tarafından açıklar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ortam.

- [Proje Alt Türleri Tarafından Genişletilen Özellikler ve Metotlar](../../extensibility/internals/properties-and-methods-extended-by-project-subtypes.md)

 Proje alt türleri kullanarak en sık genişletilmiş yöntemleri ve özellikleri ayrıntılı açıklamalar sağlar.

- [MSBuild Proje Dosyasında Verileri Kalıcı Hale Getirme](../../extensibility/internals/persisting-data-in-the-msbuild-project-file.md)

 Bir proje dosyasında verileri kalıcı hale getirmenize nasıl ve nasıl kullanılacağını açıklar <xref:Microsoft.VisualStudio.Shell.Interop.IPersistXMLFragment> proje alt toplama düzeyleri arasında proje dosyasındaki verileri koruma.

- [Proje Özelliği Kullanıcı Arabirimi](../../extensibility/internals/project-property-user-interface.md)

 Proje alt türleri proje nasıl değiştireceğinizi açıklar **özellik sayfaları** iletişim kutusu.

- [Temel Projenin Nesne Modelini Genişletme](../../extensibility/internals/extending-the-object-model-of-the-base-project.md)

 Proje alt türleri Otomasyon nesne modeli genişletmek için Otomasyon Genişleticileri nasıl kullanabileceğiniz hakkında bilgi sağlar.

- [Yeni Öğe Ekleme İletişim Kutusuna Katkıda Bulunma](../../extensibility/internals/contributing-to-the-add-new-item-dialog-box.md)

 Öğeler ekleneceğini açıklar **Yeni Öğe Ekle** iletişim kutusu.

- [Proje Dosyalarında Verileri Kaydetme](../../extensibility/saving-data-in-project-files.md)

 Proje alt kaydedebilir ve yönetilen paket Framework (MPF) kullanarak proje dosyasındaki alt özgü verileri almak nasıl açıklar.

- [Özelleştirilmiş Dağıtım İşleme](../../extensibility/internals/handling-specialized-deployment.md)

 Proje alt türleri özelleştirilmiş dağıtım davranışı uygulayarak nasıl sağlayabilirsiniz açıklar <xref:Microsoft.VisualStudio.Shell.Interop.IVsDeployableProjectCfg> arabirimi.

- [Özellik Sayfaları Ekleme ve Kaldırma](../../extensibility/adding-and-removing-property-pages.md)

 Ekleme ve özellik sayfaları, Proje Tasarımcısı'nda kaldırma açıklar.

## <a name="related-sections"></a>İlgili Bölümler
- [Proje Türleri](../../extensibility/internals/project-types.md)

 Gerçekleşen konulara bağlantılar sağlar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] projeleri.