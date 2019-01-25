---
title: 'Nasıl yapılır: ClickOnce uygulaması için özel izinleri ayarlama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce applications, permissions
- permissions, ClickOnce applications
ms.assetid: 660459ca-ef73-44a8-b323-610001f63b93
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 279dd66ca1f814dbd52593d52040818edf8f408b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54786352"
---
# <a name="how-to-set-custom-permissions-for-a-clickonce-application"></a>Nasıl yapılır: ClickOnce Uygulaması için Özel İzinleri Ayarlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Dağıtabileceğiniz bir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] Internet veya yerel Intranet bölgeleri için varsayılan izinler kullanan bir uygulama. Alternatif olarak, uygulamanız için gereken belirli izinleri için özel bir bölge oluşturabilirsiniz. Bunu şirket güvenlik izinlerini özelleştirerek yapmak **güvenlik** sayfasının **Proje Tasarımcısı**.  
  
### <a name="to-customize-a-permission"></a>Bir izni özelleştirmek için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.  
  
2.  Tıklayın **güvenlik** sekmesi.  
  
3.  Seçin **ClickOnce güvenlik ayarlarını etkinleştirme** onay kutusu.  
  
4.  Seçin **kısmi güven uygulamasıdır** seçenek düğmesini.  
  
     Denetimlerde **ClickOnce güvenlik izinleri** bölüm etkinleştirilir.  
  
5.  Gelen **uygulamanızı yükleneceği kaynak bölge** aşağı açılan listesinde, tıklayın **(özel)**.  
  
6.  Tıklayın **düzenleme izinleri XML**.  
  
     App.manifest dosyası XML düzenleyicisinde açılır.  
  
7.  Önce `</applicationRequestMinimum>` öğesi, uygulamanızın gerektirdiği izinler için XML kodunu ekleyin.  
  
    > [!NOTE]
    >  Kullanabileceğiniz `ToXml` yöntemi bir izin kümesi XML kodunu uygulama bildirimini oluşturmak için. Örneğin, için XML oluşturmak için <xref:System.Security.Permissions.EnvironmentPermission> izin kümesi, çağrı <xref:System.Security.Permissions.EnvironmentPermission.ToXml%2A> yöntemi. XML yapısı hakkında daha fazla bilgi için bkz [NIB: Nasıl yapılır: Bir izin kümesinin bir XML dosyası kullanarak içeri aktarma](http://msdn.microsoft.com/dea16b54-c108-408a-ac36-cdc05f746236).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce uygulamalarının güvenliğini sağlama](../deployment/securing-clickonce-applications.md)   
 [ClickOnce uygulamaları için kod erişimi güvenliği](../deployment/code-access-security-for-clickonce-applications.md)   
 [ClickOnce Uygulamalarının Güvenliğini Sağlama](../deployment/securing-clickonce-applications.md)
