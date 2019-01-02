---
title: 'Nasıl Yapılır: ClickOnce uygulaması için varsayılan Web sayfasını özelleştirme | Microsoft Docs'
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 97ab1335b846ecccf31addfa134fc63396dc841b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53861283"
---
# <a name="how-to-customize-the-default-web-page-for-a-clickonce-application"></a>Nasıl Yapılır: ClickOnce uygulaması için varsayılan Web sayfasını özelleştirme
ClickOnce uygulaması için Web yayımlama sırasında bir Web sayfası otomatik olarak oluşturulur ve birlikte uygulamayı yayınladınız. Varsayılan sayfa adı uygulama ve uygulama yükleme, önkoşulları yükleyin veya MSDN Yardımı'na erişmek için bağlantılar içerir.  
  
> [!NOTE]
>  Sayfada gördüğünüz gerçek bağlantıları burada sayfası görüntülendiğinde bilgisayar ve hangi bağlıdır Önkoşullar dahil.  
  
 Web sayfası için varsayılan ad *Publish.htm*; adı değiştirebilirsiniz **Proje Tasarımcısı**. Daha fazla bilgi için [nasıl yapılır: ClickOnce uygulaması için bir yayımlama sayfası belirtme](../deployment/how-to-specify-a-publish-page-for-a-clickonce-application.md).  
  
 *Publish.htm* Web sayfası, yalnızca daha yeni bir sürümü algılanırsa yayımlanır.  
  
> [!NOTE]
>  Yaptığınız değişiklikler, **Yayımla** ayarlarını etkilemez *Publish.htm* sayfası, bir özel durum: başlangıçta yayımladıktan sonra önkoşulları ekleyip, önkoşullarının listesi olur. artık doğru olmayabilir. Değişiklikleri yansıtacak şekilde önkoşul bağlantı metnini düzenlemek gerekir.  
  
### <a name="to-customize-the-publish-web-page"></a>Yayımla Web sayfasını özelleştirme  
  
1.  Bir Web konumuna ClickOnce uygulamanızı yayımlayın. Daha fazla bilgi için [nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md).  
  
2.  Web sunucusunda açık *Publish.htm* dosyasında Visual Web Designer'ı veya başka bir HTML düzenleyicisi.  
  
3.  İstediğiniz gibi sayfayı özelleştirmek ve kaydedin.  
  
4.  İsteğe bağlı. Visual Studio özelleştirilmiş Yayımla Web sayfanızın üzerine yazmasını engellemek için işareti kaldırın **sonra dağıtım Web sayfasını otomatik olarak üretmek her yayımlama** içinde **yayımlama seçeneği** iletişim kutusu.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [ClickOnce güvenliği ve dağıtımı](../deployment/clickonce-security-and-deployment.md)   
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: ClickOnce uygulamasıyla Önkoşulları Yükleme](../deployment/how-to-install-prerequisites-with-a-clickonce-application.md)   
 [Nasıl yapılır: ClickOnce uygulaması için bir yayımlama sayfası belirtme](../deployment/how-to-specify-a-publish-page-for-a-clickonce-application.md)