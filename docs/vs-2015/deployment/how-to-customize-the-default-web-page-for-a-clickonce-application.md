---
title: 'Nasıl yapılır: ClickOnce uygulaması için varsayılan Web sayfasını özelleştirme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Publish.htm Web page
- ClickOnce deployment default Web page
- deploying applications [ClickOnce], publishing
- publishing, ClickOnce
ms.assetid: 418de18c-bee9-4f24-9cd9-0252d175070d
caps.latest.revision: 16
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 4ec63fe5ae4b99252321b86b44066c46842a0851
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63433902"
---
# <a name="how-to-customize-the-default-web-page-for-a-clickonce-application"></a>Nasıl yapılır: ClickOnce Uygulaması için Varsayılan Web Sayfasını Özelleştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

ClickOnce uygulaması için Web yayımlama sırasında bir Web sayfası otomatik olarak oluşturulur ve birlikte uygulamayı yayınladınız. Varsayılan sayfa adı uygulama ve uygulama yükleme, önkoşulları yükleyin veya MSDN Yardımı'na erişmek için bağlantılar içerir.  
  
> [!NOTE]
> Sayfada gördüğünüz gerçek bağlantıları burada sayfası görüntülendiğinde bilgisayar ve hangi bağlıdır Önkoşullar dahil.  
  
 Publish.htm Web sayfası için varsayılan adıdır; adı değiştirebilirsiniz **Proje Tasarımcısı**. Daha fazla bilgi için [nasıl yapılır: ClickOnce uygulaması için bir yayımlama sayfası belirtme](../deployment/how-to-specify-a-publish-page-for-a-clickonce-application.md).  
  
 Publish.htm Web sayfası, yalnızca daha yeni bir sürümü algılanırsa yayımlanır.  
  
> [!NOTE]
> Yaptığınız değişiklikler, **Yayımla** Publish.htm sayfası, bir özel durum ayarlarını etkilemez: başlangıçta yayımladıktan sonra önkoşulları ekleyip, Önkoşullar listesinde artık doğru olacaktır. Değişiklikleri yansıtacak şekilde önkoşul bağlantı metnini düzenlemek gerekir.  
  
### <a name="to-customize-the-publish-web-page"></a>Yayımla Web sayfasını özelleştirme  
  
1. Bir Web konumuna ClickOnce uygulamanızı yayımlayın. Daha fazla bilgi için [nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md).  
  
2. Visual Web Designer veya başka bir HTML düzenleyicisi, Web sunucusunda Publish.htm dosyasını açın.  
  
3. İstediğiniz gibi sayfayı özelleştirmek ve kaydedin.  
  
4. İsteğe bağlı. Visual Studio özelleştirilmiş Yayımla Web sayfanızın üzerine yazmasını engellemek için işareti kaldırın **sonra dağıtım web sayfasını otomatik olarak üretmek her yayımlama** Yayımlama Seçenekleri iletişim kutusundaki.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce güvenliği ve dağıtımı](../deployment/clickonce-security-and-deployment.md)   
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: ClickOnce uygulamasıyla Önkoşulları Yükleme](../deployment/how-to-install-prerequisites-with-a-clickonce-application.md)   
 [Nasıl yapılır: ClickOnce Uygulaması için Bir Yayımlama Sayfası Belirtme](../deployment/how-to-specify-a-publish-page-for-a-clickonce-application.md)
