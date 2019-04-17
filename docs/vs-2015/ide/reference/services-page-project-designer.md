---
title: Hizmetler Sayfası, Proje Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- vb.ProjectPropertiesServices
helpviewer_keywords:
- Services page in Project Designer
- Project Designer, Services page
ms.assetid: 6dd9e0fa-acba-4d7d-b081-705b0fc86ff5
caps.latest.revision: 30
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 8b089cd468b9b4a69a22a3be31059be51e05ee24
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59648360"
---
# <a name="services-page-project-designer"></a>Hizmetler Sayfası, Proje Tasarımcısı
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

İstemci uygulama hizmetleri için Basitleştirilmiş erişim sağlayan [!INCLUDE[ajax_current_short](../../includes/ajax-current-short-md.md)] oturum açma, roller ve profil hizmetlerinden Windows Forms ve Windows Presentation Foundation (WPF) uygulamaları. Kullanabileceğiniz **Hizmetleri** sayfasının **Proje Tasarımcısı** etkinleştirme ve istemci uygulama hizmetleri, projeniz için yapılandırma.  
  
 İstemci uygulama hizmetleri ile kullanıcıların kimliğini doğrulama, her kullanıcının atanan rolü veya rolleri belirlemek ve ağ üzerinden paylaşabilirsiniz kullanıcı başına uygulama ayarlarını depolamak için merkezi bir sunucu kullanabilirsiniz. Daha fazla bilgi için [istemci uygulama hizmetleri](http://msdn.microsoft.com/library/1487d8df-089e-4f21-abfb-a791a652b58e).  
  
 Erişim için **Hizmetleri** sayfasında, içinde bir proje düğümü seçin **Çözüm Gezgini**ve ardından **özellikleri** üzerinde **proje** menüsü. Zaman **Proje Tasarımcısı** görünen tıklayın **Hizmetleri** sekmesi.  
  
> [!NOTE]
>  İstemci uygulama hizmetleri, .NET Framework'ün tam sürümünü gerektirir ve .NET Framework istemci profili içinde desteklenmez. Varsa **istemci uygulama hizmetlerini etkinleştirmek** onay kutusunu devre dışı bırakıldı, doğrulayın **hedef Framework'ü** .NET Framework 3.5 veya sonraki bir sürüme ayarlayın. Görüntülenecek **hedef Framework'ü** C# ' de ayarı, Proje Tasarımcısı'nı açın ve ardından **uygulama** sayfası. Görüntülenecek **hedef Framework'ü** Visual Basic'te ayarlama, Proje Tasarımcısı'nı açın, **derleme** sayfasında ve ardından **Gelişmiş derleme seçenekleri**.  
  
## <a name="task-list"></a>Görev Listesi  
 [Nasıl yapılır: İstemci uygulama servislerini yapılandırma](http://msdn.microsoft.com/library/34a8688a-a32c-40d3-94be-c8e610c6a4e8)  
  
## <a name="uielement-list"></a>UIElement Listesi  
 **Yapılandırma**  
 Bu sayfada bu denetim düzenlenemez. Bu denetimin açıklaması için bkz [derleme sayfası, Proje Tasarımcısı (Visual Basic)](../../ide/reference/compile-page-project-designer-visual-basic.md) veya [derleme sayfası, Proje Tasarımcısı (C#)](../../ide/reference/build-page-project-designer-csharp.md).  
  
 **Platform**  
 Bu sayfada bu denetim düzenlenemez. Bu denetimin açıklaması için bkz [derleme sayfası, Proje Tasarımcısı (Visual Basic)](../../ide/reference/compile-page-project-designer-visual-basic.md) veya [derleme sayfası, Proje Tasarımcısı (C#)](../../ide/reference/build-page-project-designer-csharp.md).  
  
 **İstemci uygulama hizmetlerini etkinleştirmek**  
 İstemci uygulama hizmetlerini etkinleştirmek için bu seçeneği seçin. Servis yerlerini belirtmeniz gerekir **Hizmetleri** sayfasına istemci uygulama hizmetleri kullanın.  
  
 **Windows kimlik doğrulaması kullan**  
 Kimlik doğrulama sağlayıcısı Windows tabanlı kimlik doğrulaması, diğer bir deyişle, Windows işletim sistemi tarafından sağlanan kimlik kullanacağını gösterir.  
  
 **Forms kimlik doğrulaması kullan**  
 Kimlik doğrulama sağlayıcısı form kimlik doğrulaması kullandığını gösterir. Başka bir deyişle, uygulamanız için oturum açma kullanıcı arabirimi sağlamanız gerekir. Daha fazla bilgi için [nasıl yapılır: İstemci uygulama hizmetleri ile kullanıcı oturum açma adını](http://msdn.microsoft.com/library/5431a671-eb02-4e18-a651-24764fccec9a).  
  
 **Kimlik doğrulama hizmet konumu**  
 Yalnızca form kimlik doğrulaması ile kullanılır. Kimlik doğrulama hizmetinin konumunu belirtir.  
  
 **İsteğe bağlı: Kimlik bilgileri sağlayıcısı**  
 Yalnızca form kimlik doğrulaması ile kullanılır. Gösterir <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider> uygulamanız çağırdığında bir oturum açma iletişim kutusunu görüntülemek için kimlik doğrulama hizmetinin kullanacağı uygulama `static` <xref:System.Web.Security.Membership.ValidateUser%2A?displayProperty=fullName> yöntemi ve geçişleri boş dizeler veya `null` parametre. Bu kutuyu boş bırakırsanız, geçerli kullanıcı adı ve parola geçmelidir <xref:System.Web.Security.Membership.ValidateUser%2A?displayProperty=fullName> yöntemi. Kimlik bilgileri sağlayıcısı bir derleme nitelikli tür adı olarak belirtmeniz gerekir. Daha fazla bilgi için <xref:System.Type.AssemblyQualifiedName%2A?displayProperty=fullName> ve [derleme adları](http://msdn.microsoft.com/library/8f8c2c90-f15d-400e-87e7-a757e4f04d0e). En basit şekliyle, bir derleme nitelikli tür adı, aşağıdaki örneğe benzer: `MyNamespace.MyLoginClass, MyAssembly`  
  
 **Rol hizmet konumu**  
 Rol hizmetinin konumunu belirtir.  
  
 **Web ayarları hizmet konumu**  
 Profil (Web Ayarları) hizmetinin konumunu belirtir.  
  
 **Gelişmiş**  
 Açılır [Hizmetleri iletişim kutusu için Gelişmiş ayarları](../../ide/reference/advanced-settings-for-services-dialog-box.md), bu varsayılan davranışı geçersiz kılmak için kullanabilirsiniz. Örneğin, bir veritabanı yerine yerel dosya sistemi kullanılarak çevrimdışı depolama belirtmek için bu iletişim kutusunu kullanabilirsiniz. Daha fazla bilgi için [Hizmetleri iletişim kutusu için Gelişmiş ayarları](../../ide/reference/advanced-settings-for-services-dialog-box.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İstemci uygulama hizmetleri](http://msdn.microsoft.com/library/1487d8df-089e-4f21-abfb-a791a652b58e)   
 [Hizmetleri iletişim kutusu için Gelişmiş ayarları](../../ide/reference/advanced-settings-for-services-dialog-box.md)   
 [Nasıl yapılır: İstemci uygulama servislerini yapılandırma](http://msdn.microsoft.com/library/34a8688a-a32c-40d3-94be-c8e610c6a4e8)   
 [Derleme sayfası, Proje Tasarımcısı (Visual Basic)](../../ide/reference/compile-page-project-designer-visual-basic.md)   
 [Derleme sayfası, Proje Tasarımcısı (C#)](../../ide/reference/build-page-project-designer-csharp.md)   
 [Proje Tasarımcısı giriş](http://msdn.microsoft.com/898dd854-c98d-430c-ba1b-a913ce3c73d7)
