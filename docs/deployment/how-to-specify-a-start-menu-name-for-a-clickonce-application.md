---
title: 'Nasıl Yapılır: ClickOnce uygulaması için Başlat menüsü adı belirtme | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Start menu resource name
- Start menu name
- ClickOnce deployment, Start menu name
ms.assetid: 4b5183b2-2fd4-4433-9310-4a73bb12c4e3
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a7cf4f2b30079a76012acfe972ea0de0b9e0ea78
ms.sourcegitcommit: 34840a954ed3446c789e80ee87da6cbf1203cbb5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/18/2018
ms.locfileid: "53592839"
---
# <a name="how-to-specify-a-start-menu-name-for-a-clickonce-application"></a>Nasıl Yapılır: ClickOnce uygulaması için Başlat menüsü adı belirtme
Olduğunda bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] çevrimiçi ve çevrimdışı kullanım için bir uygulama yüklendiğinde, bir giriş eklenir **Başlat** menü ve **Program Ekle veya Kaldır** listesi. Varsayılan olarak, görünen adı uygulama derlemenin adı ile aynı olduğu halde ayarlayarak görünen adı değiştirebilirsiniz **ürün adı** içinde **yayımlama seçeneği** iletişim kutusu.  
  
 **Ürün adı** gösterileceği *publish.htm* sayfasında; yüklü çevrimdışı bir uygulama için giriş adı olacaktır **Başlat** menü ve bu da olacaktır gösteren adı **Program Ekle veya Kaldır**.  
  
 **Yayımcı adı** görünür *publish.htm* sayfa yukarıdaki **ürün adı**, ve yüklü çevrimdışı bir uygulama için uygulamanın içeren klasörün adını olacaktır simgesini **Başlat** menüsü.  

 Başlangıç menüsünde kısayol veya uygulama başvurusu oluşturulan *%appdata%\Microsoft\Windows\Start Menu\Programs\\< Yayımcı adı\>*. Kısayol veya uygulama başvurusu, ürün adı ile aynı ada sahiptir.
  
 Ayarlayabileceğiniz **ürün adı** ve **Yayımcı adı** özelliklerinde **yayımlama seçeneği** iletişim kutusu, kullanılabilir **Yayımla** sayfası ' ın **Proje Tasarımcısı**.  
  
### <a name="to-specify-a-start-menu-name"></a>Başlat menüsü adı belirtmek için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2.  Tıklayın **Yayımla** sekmesi.  
  
3.  Tıklayın **seçenekleri** açmak için düğmeyi **yayımlama seçeneği** iletişim kutusu.  
  
4.  Tıklayın **açıklama**.  
  
5.  İçinde **yayımlama seçeneği** iletişim kutusunda, görüntülemek için bir ad girin **ürün adı**.  
  
6.  İsteğe bağlı olarak, bir yayımcı adı, girebileceğiniz **Yayımcı adı**.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)