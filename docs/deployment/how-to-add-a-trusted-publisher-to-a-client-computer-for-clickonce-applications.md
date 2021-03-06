---
title: ClickOnce uygulamaları için istemci bilgisayara güvenilir yayımcı ekleme
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, install without prompting
- trusted application deployment, Trusted Publishers
ms.assetid: 35fe324c-45a1-4509-b7be-5c18b4b1b4ab
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 426096670df1099568cadc2af68ae0ff50ca71e5
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66263159"
---
# <a name="how-to-add-a-trusted-publisher-to-a-client-computer-for-clickonce-applications"></a>Nasıl yapılır: ClickOnce uygulamaları için bir istemci bilgisayara güvenilir yayımcı ekleme
Güvenilir uygulama dağıtımı ile istemci bilgisayarları yapılandırabilirsiniz. böylece, [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulamaları, kullanıcıya sormadan daha yüksek bir güven düzeyi ile çalışır. Aşağıdaki yordamlar, bir yayımcının sertifika istemci bilgisayarındaki Güvenilen Yayımcılar deposuna eklemek için komut satırı aracı CertMgr.exe kullanmayı gösterir.

 Kullandığınız komutlar, sertifikayı veren sertifika yetkilisi (CA) bir istemcinin güvenilir kök bir parçası olmasına bağlı olarak biraz farklılık gösterir. Bir Windows istemci bilgisayarı bir etki alanının parçasıysa, bu, bir listede Güvenilen Kökleri değerlendirilir CA'ları içerir. Bu liste, genellikle sistem yöneticisi tarafından yapılandırılır. Sertifikanızı bu Güvenilen Kökleri biri tarafından ya da bir CA tarafından zincirlenen bu Güvenilen Kökleri birine verildiyse, istemcinin güvenilir kök deposuna sertifika ekleyebilirsiniz. Öte yandan, sertifikanızı bu Güvenilen Kökleri biri tarafından verilmemiş, istemcinin güvenilir kök deposuna hem güvenilir yayımcı deposu için sertifika eklemeniz gerekir.

> [!NOTE]
> Bu şekilde dağıtmayı planladığınız her bir istemci bilgisayar sertifikaları eklemelisiniz bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] yükseltilmiş izinler gerektiren uygulama. Sertifikaları el ile ya da istemcilerinize dağıttığınız bir uygulamanın üzerinden ekleyin. Yalnızca herhangi bir sayıda sonra dağıtabileceğiniz bu bilgisayarların bu kez, yapılandırmanız gereken [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulamalar aynı sertifika ile imzalanmış.

 Bir sertifika kullanarak program aracılığıyla bir depoya ekleyebilir <xref:System.Security.Cryptography.X509Certificates.X509Store> sınıfı.

 Güvenilir uygulama dağıtımı genel bakış için bkz. [güvenilir uygulama dağıtımına genel bakış](../deployment/trusted-application-deployment-overview.md).

### <a name="to-add-a-certificate-to-the-trusted-publishers-store-under-the-trusted-root"></a>Güvenilen Yayımcılar deposuna altında güvenilen kök sertifika eklemek için

1. Bir CA'dan bir bir dijital sertifika alacaktır.

2. Base64 X.509 sertifikasını dışarı aktarma (*.cer*) biçimi. Sertifika biçimleri hakkında daha fazla bilgi için bkz. [sertifika verme](http://go.microsoft.com/fwlink/?LinkId=164793).

3. İstemci bilgisayarlarda komut isteminden aşağıdaki komutu çalıştırın:

     **certmgr.exe-certificate.cer - c -s - r localMachine TrustedPublisher Ekle**

### <a name="to-add-a-certificate-to-the-trusted-publishers-store-under-a-different-root"></a>Güvenilen Yayımcılar deposuna altında farklı bir kök sertifika eklemek için

1. Bir CA'dan bir bir dijital sertifika alacaktır.

2. Base64 X.509 sertifikasını dışarı aktarma (*.cer*) biçimi. Sertifika biçimleri hakkında daha fazla bilgi için bkz. [sertifika verme](http://go.microsoft.com/fwlink/?LinkId=164793).

3. İstemci bilgisayarlarda komut isteminden aşağıdaki komutu çalıştırın:

     **certmgr.exe-good.cer - c -s - r localMachine kök Ekle**

     **certmgr.exe-good.cer - c -s - r localMachine TrustedPublisher Ekle**

## <a name="see-also"></a>Ayrıca bkz.
- [İzlenecek yol: Bir ClickOnce uygulamasını el ile dağıtma](../deployment/walkthrough-manually-deploying-a-clickonce-application.md)
- [ClickOnce uygulamalarının güvenliğini sağlama](../deployment/securing-clickonce-applications.md)
- [ClickOnce uygulamaları için kod erişimi güvenliği](../deployment/code-access-security-for-clickonce-applications.md)
- [ClickOnce ve Authenticode](../deployment/clickonce-and-authenticode.md)
- [Güvenilir Uygulama dağıtımına genel bakış](../deployment/trusted-application-deployment-overview.md)
- [Nasıl yapılır: ClickOnce güvenlik ayarlarını etkinleştirme](../deployment/how-to-enable-clickonce-security-settings.md)
- [Nasıl yapılır: ClickOnce uygulaması için bir güvenlik bölgesi ayarlama](../deployment/how-to-set-a-security-zone-for-a-clickonce-application.md)
- [Nasıl yapılır: ClickOnce uygulaması için özel izinleri ayarlama](../deployment/how-to-set-custom-permissions-for-a-clickonce-application.md)
- [Nasıl yapılır: Sınırlı izinler ile ClickOnce uygulamasında hata ayıklama](../deployment/how-to-debug-a-clickonce-application-with-restricted-permissions.md)
- [Nasıl yapılır: ClickOnce uygulamaları için bir istemci bilgisayara güvenilir yayımcı ekleme](../deployment/how-to-add-a-trusted-publisher-to-a-client-computer-for-clickonce-applications.md)
- [Nasıl yapılır: Uygulama ve dağıtım bildirimlerini yeniden imzalama](../deployment/how-to-re-sign-application-and-deployment-manifests.md)
- [Nasıl yapılır: ClickOnce güven istemi davranışını yapılandırma](../deployment/how-to-configure-the-clickonce-trust-prompt-behavior.md)