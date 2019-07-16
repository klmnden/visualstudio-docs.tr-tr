---
title: 'Nasıl yapılır: ClickOnce çevrimdışı belirtin veya çevrimiçi yükleme modunu | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, specifying install mode
- install mode
- online applications
- offline applications
- ClickOnce install mode
ms.assetid: 0aee5fc1-e966-4bda-9b8f-d9997aeaa779
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: d4111ca5aee4a405a4a797dbfee14a3d4b50435f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68149756"
---
# <a name="how-to-specify-the-clickonce-offline-or-online-install-mode"></a>Nasıl yapılır: ClickOnce Çevrimdışı veya Çevrimiçi Yükleme Modunu Belirtme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

`Install Mode` İçin bir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] uygulama, uygulama çevrimiçi veya çevrimdışı kullanılabilir olup olmayacağını belirler. Seçeneğini belirlediğinizde **uygulama yalnızca çevrimiçi kullanılabilir**, kullanıcı erişiminiz olmalıdır [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] konumu (bir Web sayfası veya bir dosya paylaşımı) uygulamayı çalıştırmak için yayımlama. Seçtiğinizde **uygulamayı çevrimdışı olarak da kullanılabilir**, uygulama için girdileri ekler **Başlat** menü ve **Program Ekle veya Kaldır** iletişim kutusu; kullanıcı olduğu bağlı değil, uygulamayı çalıştırmak kullanabilirsiniz.  
  
 `Install Mode` Ayarlanabilir **Yayımla** sayfasının **Proje Tasarımcısı**.  
  
 **Not** `Install Mode` Yayımla Sihirbazı'nı kullanarak da ayarlanabilir. Daha fazla bilgi için [nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md).  
  
### <a name="to-make-a-clickonce-application-available-online-only"></a>ClickOnce uygulaması sadece çevrimiçi kullanılabilir yapmak için  
  
1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2. Tıklayın **Yayımla** sekmesi.  
  
3. İçinde **yükleme modu ve ayarları** alanı tıklayın **uygulama yalnızca çevrimiçi kullanılabilir** seçenek düğmesini.  
  
### <a name="to-make-a-clickonce-application-available-online-or-offline"></a>Bir ClickOnce uygulamasını çevrimiçi veya çevrimdışı yapmak için  
  
1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2. Tıklayın **Yayımla** sekmesi.  
  
3. İçinde **yükleme modu ve ayarları** alanı tıklayın **uygulamayı çevrimdışı olarak da kullanılabilir** seçenek düğmesini.  
  
     Yüklendiğinde uygulama için girdileri ekler **Başlat** menü ve **Program Ekle veya Kaldır** Denetim Masası'nda.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)   
 [ClickOnce Dağıtım Stratejisini Seçme](../deployment/choosing-a-clickonce-deployment-strategy.md)
