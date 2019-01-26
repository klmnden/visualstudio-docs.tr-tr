---
title: 'Nasıl yapılır: ClickOnce çevrimdışı belirtin veya çevrimiçi yükleme modunu | Microsoft Docs'
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ef19b966bb9d934975eebd00399b401e768922d1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55011682"
---
# <a name="how-to-specify-the-clickonce-offline-or-online-install-mode"></a>Nasıl yapılır: ClickOnce çevrimdışı veya çevrimiçi yükleme modunu belirtme
`Install Mode` İçin bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama, uygulama çevrimiçi veya çevrimdışı kullanılabilir olup olmayacağını belirler. Seçeneğini belirlediğinizde **uygulama yalnızca çevrimiçi kullanılabilir**, kullanıcı erişiminiz olmalıdır [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] konumu (bir Web sayfası veya bir dosya paylaşımı) uygulamayı çalıştırmak için yayımlama. Seçtiğinizde **uygulamayı çevrimdışı olarak da kullanılabilir**, uygulama için girdileri ekler **Başlat** menü ve **Program Ekle veya Kaldır** iletişim kutusu; kullanıcı olduğu bağlı değil, uygulamayı çalıştırmak kullanabilirsiniz.  
  
 `Install Mode` Ayarlanabilir **Yayımla** sayfasının **Proje Tasarımcısı**.  
  
 **Not** `Install Mode` Yayımla Sihirbazı'nı kullanarak da ayarlanabilir. Daha fazla bilgi için [nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md).  
  
### <a name="to-make-a-clickonce-application-available-online-only"></a>ClickOnce uygulaması sadece çevrimiçi kullanılabilir yapmak için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2.  Tıklayın **Yayımla** sekmesi.  
  
3.  İçinde **yükleme modu ve ayarları** alanı tıklayın **uygulama yalnızca çevrimiçi kullanılabilir** seçenek düğmesini.  
  
### <a name="to-make-a-clickonce-application-available-online-or-offline"></a>Bir ClickOnce uygulamasını çevrimiçi veya çevrimdışı yapmak için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2.  Tıklayın **Yayımla** sekmesi.  
  
3.  İçinde **yükleme modu ve ayarları** alanı tıklayın **uygulamayı çevrimdışı olarak da kullanılabilir** seçenek düğmesini.  
  
     Yüklendiğinde uygulama için girdileri ekler **Başlat** menü ve **Program Ekle veya Kaldır** Denetim Masası'nda.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)   
 [ClickOnce dağıtım stratejisini seçin](../deployment/choosing-a-clickonce-deployment-strategy.md)