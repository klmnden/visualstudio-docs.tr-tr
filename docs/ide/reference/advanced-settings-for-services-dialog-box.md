---
title: Hizmetler İçin Gelişmiş Ayarlar İletişim Kutusu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- vb.ProjectPropertiesAdvancedServices
helpviewer_keywords:
- Advanced Settings for Services dialog box
ms.assetid: 6dde4a2d-85e1-4275-aa55-24b84111be91
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 490f7fcbe1a63fee9b44844de94e58cd0823aa46
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55023164"
---
# <a name="advanced-settings-for-services-dialog-box"></a>Hizmetler İçin Gelişmiş Ayarlar İletişim Kutusu
İstemci uygulama hizmetleri için Basitleştirilmiş erişim sağlayan [!INCLUDE[ajax_current_short](../../ide/reference/includes/ajax_current_short_md.md)] oturum açma, roller ve profil hizmetlerinden Windows Forms ve Windows Presentation Foundation (WPF) uygulamaları. Kullanabileceğiniz **Hizmetleri** sayfasını **Proje Tasarımcısı** istemci uygulama hizmetleri yapılandırmak için. Hakkında daha fazla bilgi için **Hizmetleri** sayfasında, bkz: [Hizmetler Sayfası, Proje Tasarımcısı](../../ide/reference/services-page-project-designer.md).

 Kullanım **Hizmetleri için Gelişmiş ayarları** iletişim kutusunun **Hizmetleri** sayfasını **Proje Tasarımcısı** istemci uygulama hizmetleri için Gelişmiş ayarları yapılandırmak için. Bu ayarları kullanarak, daha az yaygın senaryoları etkinleştirmek için bazı varsayılan hizmet davranışı geçersiz kılabilirsiniz. Daha fazla bilgi için [istemci uygulama hizmetleri](/dotnet/framework/common-client-technologies/client-application-services).

 Erişim için **hizmetler için Gelişmiş ayarları** iletişim kutusunda, içinde bir proje düğümü seçin **Çözüm Gezgini**ve ardından **özellikleri** üzerinde **proje**  menüsü. Zaman **Proje Tasarımcısı** görünen tıklayın **Hizmetleri** sekmesine ve ardından **Gelişmiş** düğmesi. İstemci uygulama Hizmetleri'ı etkinleştirene kadar bu düğmeyi devre dışı bırakılacak.

## <a name="task-list"></a>Görev Listesi

- [Nasıl yapılır: İstemci uygulama servislerini yapılandırma](/dotnet/framework/common-client-technologies/how-to-configure-client-application-services)

## <a name="uielement-list"></a>UIElement Listesi

 **Çevrimdışı oturum açma yerel olarak etkinleştirmek için parola karması Kaydet** şifrelenmiş bir kullanıcının parolasını yerel uygulama çevrimdışı modda olduğunda oturum açmak kullanıcının etkinleştirmek için önbelleğe alınacaktır olup olmadığını belirtir. Bu seçenek varsayılan olarak seçilidir.

 **Sunucu tanımlama bilgisi süresi her yeniden oturum açmasını gerektiren** uygulamanız rolleri veya profili hizmeti ve sunucu kimlik doğrulaması eriştiğinde daha önceden kimliği doğrulanmış kullanıcılara otomatik olarak yeniden kimlik doğrulaması olup olmadığını belirtir tanımlama bilgisi süresi doldu. Uygulama Hizmetleri erişimini ve açık yeniden kimlik doğrulaması tanımlama bilgisinin zaman aşımına uğradıktan gerektiren için bu seçeneği belirleyin. Bu, kullanım kalmaz sonra uygulamasını çalışır durumda bırakın kullanıcılar süresiz olarak kimliğinin emin olmak genel konumda dağıtılan uygulamalar için yararlıdır. Bu seçenek varsayılan olarak işaretli değildir.

 **Rol hizmeti önbellek zaman aşımı** istemci rol sağlayıcıyı kullanacak süreyi önbelleğe rol hizmetine erişim yerine rol değerleri belirtir. Rolleri seyrek güncelleştirildiğinde rolleri sık veya daha büyük bir değere güncelleştirildiğinde bu zaman aralığı için küçük bir değere ayarlayın. Varsayılan değer bir gündür.

 Çağırdığınızda, önbelleğe alınmış rol değerlerinin veya rol hizmeti rol sağlayıcısı erişen <xref:System.Web.Security.RolePrincipal.IsInRole%2A> yöntemi. Program aracılığıyla önbelleği temizlemek ve uzak hizmete erişmek için bu yöntem zorlamak için çağrı <xref:System.Web.ClientServices.Providers.ClientRoleProvider.ResetCache%2A> yöntemi.

 **Özel bağlantı dizesini kullanmak** istemci hizmeti sağlayıcıları için yerel önbelleği özel bir veri deposu kullanıp kullanmayacağını belirtir. Varsayılan olarak, hizmet sağlayıcıları, önbellek için yerel dosya sistemi kullanır. Bu seçeneğin seçilmesi varsayılan bağlantı dizesi metin kutusunda otomatik olarak doldurur. Varsayılan bağlantı dizesini otomatik olarak oluşturmak ve bir SQL Server Compact Edition veritabanını kullanmak için tutabilirsiniz veya mevcut bir SQL Server veritabanına bir bağlantı dizesi belirtebilirsiniz. Daha fazla bilgi için [nasıl yapılır: İstemci uygulama servislerini yapılandırma](/dotnet/framework/common-client-technologies/how-to-configure-client-application-services). Bu seçenek varsayılan olarak işaretli değildir.

## <a name="see-also"></a>Ayrıca bkz.

- [İstemci Uygulama Servisleri](/dotnet/framework/common-client-technologies/client-application-services)
- [Hizmetler Sayfası, Proje Tasarımcısı](../../ide/reference/services-page-project-designer.md)
- [Nasıl yapılır: İstemci uygulama servislerini yapılandırma](/dotnet/framework/common-client-technologies/how-to-configure-client-application-services)