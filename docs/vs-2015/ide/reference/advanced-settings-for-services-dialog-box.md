---
title: Hizmetleri iletişim kutusu için Gelişmiş ayarları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- vb.ProjectPropertiesAdvancedServices
helpviewer_keywords:
- Advanced Settings for Services dialog box
ms.assetid: 6dde4a2d-85e1-4275-aa55-24b84111be91
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 2565b3b8fd84714693661fcf0cf04961a70d10f9
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59652949"
---
# <a name="advanced-settings-for-services-dialog-box"></a>Hizmetler İçin Gelişmiş Ayarlar İletişim Kutusu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

İstemci uygulama hizmetleri için Basitleştirilmiş erişim sağlayan [!INCLUDE[ajax_current_short](../../includes/ajax-current-short-md.md)] oturum açma, roller ve profil hizmetlerinden Windows Forms ve Windows Presentation Foundation (WPF) uygulamaları. Kullanabileceğiniz **Hizmetleri** sayfasını **Proje Tasarımcısı** istemci uygulama hizmetleri yapılandırmak için. Hakkında daha fazla bilgi için **Hizmetleri** sayfasında, bkz: [Hizmetler Sayfası, Proje Tasarımcısı](../../ide/reference/services-page-project-designer.md).  
  
 Kullanım **Hizmetleri için Gelişmiş ayarları** iletişim kutusunun **Hizmetleri** sayfasını **Proje Tasarımcısı** istemci uygulama hizmetleri için Gelişmiş ayarları yapılandırmak için. Bu ayarları kullanarak, daha az yaygın senaryoları etkinleştirmek için bazı varsayılan hizmet davranışı geçersiz kılabilirsiniz. Daha fazla bilgi için [istemci uygulama hizmetleri](http://msdn.microsoft.com/library/1487d8df-089e-4f21-abfb-a791a652b58e).  
  
 Erişim için **hizmetler için Gelişmiş ayarları** iletişim kutusunda, içinde bir proje düğümü seçin **Çözüm Gezgini**ve ardından **özellikleri** üzerinde **proje**  menüsü. Zaman **Proje Tasarımcısı** görünen tıklayın **Hizmetleri** sekmesine ve ardından **Gelişmiş** düğmesi. İstemci uygulama Hizmetleri'ı etkinleştirene kadar bu düğmeyi devre dışı bırakılacak.  
  
## <a name="task-list"></a>Görev Listesi  
 [Nasıl yapılır: İstemci uygulama servislerini yapılandırma](http://msdn.microsoft.com/library/34a8688a-a32c-40d3-94be-c8e610c6a4e8)  
  
 [Nasıl yapılır: İstemci uygulama hizmetleri ile Çevrimdışı Çalış](http://msdn.microsoft.com/f792cb16-8520-4a0f-9dc9-07bfbc454e38)  
  
## <a name="uielement-list"></a>UIElement Listesi  
 **Çevrimdışı oturum açma yerel olarak etkinleştirmek için parola karması Kaydet**  
 Bir kullanıcının parolasını şifrelenmiş yerel olarak uygulama çevrimdışı modda olduğunda oturum açmak kullanıcının etkinleştirmek için önbelleğe alınacaktır olup olmadığını belirtir. Daha fazla bilgi için [nasıl yapılır: İstemci uygulama hizmetleri ile çevrimdışı çalışma](http://msdn.microsoft.com/f792cb16-8520-4a0f-9dc9-07bfbc454e38). Bu seçenek varsayılan olarak seçilidir.  
  
 **Sunucu tanımlama bilgisi süresi her yeniden oturum açmasını iste**  
 Daha önceden kimliği doğrulanmış kullanıcılara otomatik olarak uygulama rolleri veya profili hizmeti erişir ve sunucu kimlik doğrulama tanımlama doldu yeniden kimlik doğrulaması olup olmadığını belirtir. Uygulama Hizmetleri erişimini ve açık yeniden kimlik doğrulaması tanımlama bilgisinin zaman aşımına uğradıktan gerektiren için bu seçeneği belirleyin. Bu, kullanım kalmaz sonra uygulamasını çalışır durumda bırakın kullanıcılar süresiz olarak kimliğinin emin olmak genel konumda dağıtılan uygulamalar için yararlıdır. Bu seçenek varsayılan olarak işaretli değildir.  
  
 **Rol hizmeti önbellek zaman aşımı**  
 İstemci rol sağlayıcısı rolleri hizmete erişim yerine önbelleğe alınmış rol değerleri kullanacaksınız süreyi belirtir. Rolleri seyrek güncelleştirildiğinde rolleri sık veya daha büyük bir değere güncelleştirildiğinde bu zaman aralığı için küçük bir değere ayarlayın. Varsayılan değer bir gündür.  
  
 Çağırdığınızda, önbelleğe alınmış rol değerlerinin veya rol hizmeti rol sağlayıcısı erişen <xref:System.Web.Security.RolePrincipal.IsInRole%2A> yöntemi. Program aracılığıyla önbelleği temizlemek ve uzak hizmete erişmek için bu yöntem zorlamak için çağrı <xref:System.Web.ClientServices.Providers.ClientRoleProvider.ResetCache%2A> yöntemi.  
  
 **Özel bağlantı dizesini kullanın**  
 İstemci hizmet sağlayıcıları için yerel önbelleği özel bir veri deposu kullanıp kullanmayacağını belirtir. Varsayılan olarak, hizmet sağlayıcıları, önbellek için yerel dosya sistemi kullanır. Bu seçeneğin seçilmesi varsayılan bağlantı dizesi metin kutusunda otomatik olarak doldurur. Varsayılan bağlantı dizesini otomatik olarak oluşturmak ve bir SQL Server Compact Edition veritabanını kullanmak için tutabilirsiniz veya mevcut bir SQL Server veritabanına bir bağlantı dizesi belirtebilirsiniz. Daha fazla bilgi için [nasıl yapılır: İstemci uygulama servislerini yapılandırma](http://msdn.microsoft.com/library/34a8688a-a32c-40d3-94be-c8e610c6a4e8). Bu seçenek varsayılan olarak işaretli değildir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İstemci uygulama hizmetleri](http://msdn.microsoft.com/library/1487d8df-089e-4f21-abfb-a791a652b58e)   
 [Hizmetler Sayfası, Proje Tasarımcısı](../../ide/reference/services-page-project-designer.md)   
 [Nasıl yapılır: İstemci uygulama servislerini yapılandırma](http://msdn.microsoft.com/library/34a8688a-a32c-40d3-94be-c8e610c6a4e8)   
 [Nasıl yapılır: İstemci uygulama hizmetleri ile Çevrimdışı Çalış](http://msdn.microsoft.com/f792cb16-8520-4a0f-9dc9-07bfbc454e38)
