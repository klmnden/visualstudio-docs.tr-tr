---
title: İmzalama sayfası, Proje Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- vs.AddNewStrongNameKey
- ResolveKeySource.KeyFileForSignAssemblyNotImported
- vb.ProjectPropertiesSigning.ChangePasswordDialog
- ResolveKeySource.KeyFileForManifestNotImported
- vb.ProjectPropertiesSigning
- vb.ProjectPropertiesSigning.PasswordNeededDialog
- vb.ProjectPropertiesSigning.PfxPasswordDialog
helpviewer_keywords:
- Project Designer, Signing page
- Signing page in Project Designer
ms.assetid: dab3ba13-2f92-4827-92bd-1be3c35bc48b
caps.latest.revision: 39
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 59f8cb15db6f93c76275fd1d8318ae04df998cf7
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54788732"
---
# <a name="signing-page-project-designer"></a>İmzalama Sayfası, Proje Tasarımcısı
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Kullanım **imzalama** sayfasının **Proje Tasarımcısı** uygulama ve dağıtım bildirimlerini imzalamak için ve ayrıca (tanımlayıcı ad imzalama) derlemeyi imzalamak için.  
  
 Her iki görevleri gerçekleştirilir olsa da uygulama ve dağıtım bildirimlerini imzalama imzalama bir derlemenin farklı bir işlem olduğunu fark **imzalama** sayfası.  
  
 Ayrıca, anahtar dosyası bilgilerinin depolanması, bildirim imzalama ve bütünleştirilmiş kod imzalama için farklıdır. Bildirim imzalamak için anahtar bilgileri bilgisayarınızın şifreleme depolama veritabanı ve geçerli kullanıcının Windows sertifika deposunda depolanır. Derleme imzalama için anahtar bilgileri yalnızca, bilgisayarınızın şifreleme depolama veritabanında depolanır.  
  
 Erişim için **imzalama** sayfasında, içinde bir proje düğümü seçin **Çözüm Gezgini**ve ardından **proje** menüsünde tıklatın **özellikleri**. Zaman **Proje Tasarımcısı** görünen tıklayın **imzalama** sekmesi.  
  
## <a name="application-and-deployment-manifest-signing"></a>Uygulama ve dağıtım bildirimlerini imzalama  
 **ClickOnce bildirimlerini imzala** onay kutusu  
 Uygulama ve dağıtım bildirimlerinin ortak/özel anahtar çifti ile oturum açmak için bu onay kutusunu seçin. Bunun nasıl yapılacağı hakkında daha fazla bilgi için bkz. [nasıl yapılır: Uygulama ve dağıtım bildirimlerini imzalama](../../ide/how-to-sign-application-and-deployment-manifests.md).  
  
 **Store arasından seçim** düğmesi  
 Mevcut bir sertifikayı geçerli kullanıcının kişisel sertifika depolama alanından seçmenizi sağlar. Bu sertifikalar, uygulama ve dağıtım bildirimlerini imzalamak için birini seçebilirsiniz.  
  
 Tıklayarak **Store ' seçin** açılır **bir sertifika seçin** iletişim kutusunda (dolmamışsa) şu anda geçerli olan, kişisel sertifika deposundaki sertifikalar listeler ve özel anahtarları sahip. Seçtiğiniz sertifikanın amacı kod imzalamayı içermelidir.  
  
 Tıklarsanız **sertifika özelliklerini görüntüleme**, **sertifika ayrıntıları** iletişim kutusu görüntülenir. Bu iletişim kutusu sertifika ile ilgili ayrıntılı bilgiler içerir ve ek seçenekler içerir. Tıklayabilirsiniz **sertifikaları hakkında daha fazla bilgi** Ek Yardım bilgilerini görüntülemek için.  
  
 **Dosyadan Seç** düğmesi  
 Var olan bir anahtar dosyasından bir sertifika seçmenize izin verir.  
  
 Tıklayarak **dosyadan Seç** açılır **Dosya Seç** iletişim kutusunda, bir sertifika anahtarı (.pfx) dosyası seçmenizi sağlar. Dosya, parola korumalı ve kişisel sertifika deponuzda zaten yer almamalıdır olmalıdır.  
  
 İçinde **dosyasını açmak için parola gir** iletişim kutusunda, sertifika anahtarı (.pfx) dosyasını açmak için parola girin. Parola bilgisi kişisel anahtar kapsayıcısı listenizi ve kişisel sertifika depolama alanınızda depolanır.  
  
 **Test sertifikası Oluştur** düğmesi  
 Test etmek için bir sertifika oluşturmanıza olanak sağlar. Test sertifikası ClickOnce Uygulama ve dağıtım bildirimlerini imzalamak için kullanılır.  
  
 Tıklayarak **Test sertifikası Oluştur** açılır **Test sertifikası Oluştur** iletişim kutusu, hangi yazabilirsiniz test sertifikası için tanımlayıcı ad anahtar dosyası için bir parola. Dosyanın nasıl adlandırıldığı *projectname*_TemporaryKey.pfx. Tıklarsanız **Tamam** parola yazmadan .pfx dosyasını şifreli bir parola değil.  
  
 **Zaman damgası sunucu URL'si** kutusu  
 Bu zaman damgaları bir sunucunun adresini belirten imza. Bir sertifika sağladığınızda, bu dış bir siteye uygulamanın imzalandığı zamanı doğrular.  
  
## <a name="assembly-signing"></a>Derleme imzalama  
 **Derlemeyi imzalamayı** onay kutusu  
 Derlemeyi imzalamak ve kesin adlandırılmış bir anahtar dosyası oluşturmak için bu onay kutusunu seçin. Derlemeyi kullanarak imzalama hakkında daha fazla bilgi için **Proje Tasarımcısı**, bkz: [nasıl yapılır: Bir derleme (Visual Studio) oturum](http://msdn.microsoft.com/f468a7d3-234c-4353-924d-8e0ae5896564).  
  
 Bu seçenek, Al.exe araç tarafından sağlanan kullanır [!INCLUDE[winsdklong](../../includes/winsdklong-md.md)] derlemeyi imzalamak için. Al.exe hakkında daha fazla bilgi için bkz: [nasıl yapılır: Bir derlemeyi katı bir adla imzalamak](http://msdn.microsoft.com/library/2c30799a-a826-46b4-a25d-c584027a6c67).  
  
 **Tanımlayıcı ad anahtar dosyası seç** listesi  
 Derleme imzalamak için kullanılan bir yeni veya mevcut kesin adlandırılmış anahtar dosyası belirtmenize olanak sağlar. Seçin  **\<Gözat … >** var olan bir anahtar dosyası seçin.  
  
 Seçin  **\<yeni … >** derlemeyi imzalamak kullanılacak yeni bir anahtar dosyası oluşturmak için. **Katı ad anahtarı oluştur** iletişim kutusu görüntülenirse, hangi anahtar dosya adı belirtin ve bir parolayla anahtarı dosyasını korumak için kullanabilirsiniz. Parola en az 6 karakter uzunluğunda olmalıdır. Parola belirtirseniz, bir kişisel bilgi değişimi (.pfx) dosyası oluşturulur. bir parolayı belirtmezseniz (.snk) kesin adlandırılmış bir anahtar dosyası oluşturulur.  
  
 **Parola Değiştir** düğmesi  
 Derlemeyi imzalamak için kullanılan anahtar kişisel bilgi değişimi (.pfx) dosyası için parolayı değiştirir.  
  
 Tıklayarak **parolasını değiştirme** açılır **anahtar parolasını değiştirme** iletişim kutusu. Bu iletişim kutusunda **eski parola** anahtar dosyası için geçerli parola. **Yeni parola** en az 6 karakterden uzun olmalıdır. Parola bilgisi, geçerli kullanıcının Windows sertifika depolama alanında depolanır.  
  
 **Yalnızca oturum gecikme** onay kutusu  
 Gecikmeli imzalamayı etkinleştirmek için bu onay kutusunu seçin.  
  
 Gecikmeli imzalanmış bir proje çalışmaz ve hata ayıklaması yapılamaz unutmayın. Ancak, kullanabileceğiniz [Sn.exe (tanımlayıcı ad aracı)](http://msdn.microsoft.com/library/c1d2b532-1b8e-4c7a-8ac5-53b801135ec6) ile `-Vr` seçeneği doğrulama geliştirme sırasında atlanacak.  
  
> [!NOTE]
>  Bir derleme için kaydolduğunuzda, bir özel anahtara erişim her zaman olmayabilir. Örneğin, bir kuruluş geliştiricileri her gün için erişime sahip olmadığından yakından korumalı bir anahtar çifti olabilir. Ortak anahtar kullanılabilir, ancak özel anahtar erişimi birkaç kişilerle sınırlıdır. Böyle bir durumda, kullandığınız *Gecikmeli* veya *kısmi imzalama* derleme kapalı devredildiği kadar ek özel anahtarın erteleniyor ortak anahtar sağlamak için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Proje Özellikleri başvurusu](../../ide/reference/project-properties-reference.md)   
 [Derleme ve bildirim imzalamayı yönetme](../../ide/managing-assembly-and-manifest-signing.md)   
 [Tanımlayıcı ad imzalama için yönetilen uygulamalar](http://msdn.microsoft.com/5fef3490-c519-4363-94fd-8b1ad260dab5)   
 [Nasıl yapılır: Oturum uygulama ve dağıtım bildirimlerini](../../ide/how-to-sign-application-and-deployment-manifests.md)   
 [Nasıl yapılır: Bir derleme (Visual Studio) oturum açın](http://msdn.microsoft.com/f468a7d3-234c-4353-924d-8e0ae5896564)   
 [Nasıl yapılır: Derlemeyi tanımlayıcı bir adla imzalama](http://msdn.microsoft.com/library/2c30799a-a826-46b4-a25d-c584027a6c67)   
 [Kesin Adlandırılmış Bütünleştirilmiş Kodlar](http://msdn.microsoft.com/library/d4a80263-f3e0-4d81-9b61-f0cbeae3797b)
