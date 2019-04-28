---
title: Oluşturma ve SharePoint çözümlerinde hata ayıklama | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, building and debugging
- SharePoint development in Visual Studio, debugging
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: e91c1433fde85a9ec828a6a018bee986fdc7aa5c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62988132"
---
# <a name="build-and-debug-sharepoint-solutions"></a>Derleme ve SharePoint çözümlerinde hata ayıklama
  Genel olarak, derleme ve hata ayıklama SharePoint çözümleri derleme ve hata ayıklama proje türlerinde aynıdır [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. Bu bölümdeki konular, mevcut farkları açıklamaktadır.

## <a name="project-output-for-sharepoint-solutions"></a>SharePoint çözümleri için proje çıktısı
 SharePoint çözümleri oluşturmak oluşturur derlemeler ve çözüm paketine (*.wsp*) dosyası. Aşağıdaki tabloda, bir yapı sırasında bu dosyaları konumlarını gösterir.

|Öğe oluştur|Çıktı klasörü|
|----------------|-------------------|
|Derleme, program veritabanı (*.pdb*), ve *.wsp* dosyaları.|*\<ProjectName > \bin\debug* veya  *\<ProjectName > \bin\release*|
|SharePoint proje öğesi dosyaları.|*\<ProjectName > \pkg\debug* veya  *\<ProjectName > \pkg\release*|
|Ara dosya oluşturun.|*\<ProjectName > \obj\debug* veya  *\<ProjectName > \obj\release*|
|Paket Ara dosyaları.|*\<ProjectName > \pkgobj\debug* veya  *\<ProjectName > \pkgobj\release*|

## <a name="build-sharepoint-solutions"></a>SharePoint çözümleri derleme
 SharePoint çözümleri oluşturmak için SharePoint server'ın doğru sürümü geliştirme bilgisayarında olmalıdır. Aksi halde SharePoint çözümleri oluşturmak diğer proje türleri oluşturma aynıdır [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. Daha fazla bilgi için [nasıl yapılır: SharePoint çözümleri derleme](../sharepoint/how-to-build-sharepoint-solutions.md).

## <a name="debug-and-test-sharepoint-solutions"></a>SharePoint çözümlerini test etmek ve hata ayıklama
 Hata ayıklama önce [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] kopyaları *.wsp* paket SharePoint sunucusuna Site ve Web kapsamlı özelliklerini etkinleştirir ve bazı durumlarda, projeyi başlatır. Diğer durumlarda, projeyi el ile açmanız gerekebilir. Daha fazla bilgi için [sorun giderme SharePoint çözümleri](../sharepoint/troubleshooting-sharepoint-solutions.md) ve [hata ayıklama SharePoint çözümleri](../sharepoint/debugging-sharepoint-solutions.md).

## <a name="debug-and-verify-sharepoint-solutions-by-using-azure-devops-services-features"></a>Azure DevOps Hizmetleri özelliklerini kullanarak SharePoint çözümleri doğrulayın ve hata ayıklama
 Azure DevOps Hizmetleri özellikleri birim testi ve IntelliTrace gibi SharePoint çözümlerinizi daha doğru bir şekilde belirlemenize sorunları için etkinleştirin. Profil oluşturma, bulun ve SharePoint Çözümlerinizdeki performans sorunlu alanları tanımlayın sağlar. Daha fazla bilgi için [doğrulanıyor ve SharePoint kodda hata ayıklama](../sharepoint/verifying-and-debugging-sharepoint-code.md) ve [SharePoint uygulamalarını performans profil oluşturma](../sharepoint/profiling-the-performance-of-sharepoint-applications.md).

## <a name="security-during-the-build-process"></a>Derleme işlemi sırasında güvenlik
 Paket veya SharePoint çözümlerini dağıtmak için [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] dosyaları SharePoint sunucusuna kopyalamak için izninizin olması gerekir. Çalıştırmalısınız [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] yükseltilmiş bir işlem ve kullanıcı hesabı SharePoint sunucusundaki bir Site koleksiyonu yöneticisi olması gerekir. Ayrıca, projenin Korumalı çözüm veya Grup çözümü olup olmadığını belirtmeniz gerekir. Daha fazla bilgi için [korumalı arasındaki farklar ve Grup çözümlerine](../sharepoint/differences-between-sandboxed-and-farm-solutions.md).

## <a name="using-the-clean-command"></a>Temizle komutunu kullanma
 Bir SharePoint server, hata ayıklama için bir SharePoint çözüm yüklendiğinde **temiz** komut çözüm kaldırmaz. Bunun yerine, SharePoint yapılandırma özellikleri devre dışı bırakmanız gerekir.

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint çözümleri geliştirme](../sharepoint/developing-sharepoint-solutions.md)
- [Sunucu Gezgini kullanarak SharePoint bağlantılarına göz atın](../sharepoint/browsing-sharepoint-connections-using-server-explorer.md)
- [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)
