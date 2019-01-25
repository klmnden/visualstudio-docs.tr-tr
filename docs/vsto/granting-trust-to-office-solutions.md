---
title: Office çözümlerine güven verme
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- security [Office development in Visual Studio], trust
- inclusion lists [Office development in Visual Studio], about inclusion lists
- trust [Office development in Visual Studio], 2007 Office system
- granting trust [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: b07aea10d2b1d55e98239d6dd804a506390f1974
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54871383"
---
# <a name="grant-trust-to-office-solutions"></a>Office çözümlerine güven verme
  Kazandırmanız çözüm derlemesini, uygulama bildirimi, dağıtım bildirimini ve belge güvenmeyi her hedef bilgisayarın güvenlik ilkesini değiştirmek Office çözümleri anlamına gelir. Güven Office çözümü için siz veya son kullanıcı tarafından verilebilir.

 Uygulama ve dağıtım bildirimlerini imzalayarak Office çözümü için tam güven verebilirsiniz.

 Son kullanıcılar verme Office çözümlerine güven bir güven karar yaparak [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] güven istemi.

 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]

##  <a name="Signing"></a> Uygulama ve dağıtım bildirimlerini imzalayarak çözüme güvenin
 Tüm uygulama ve dağıtım bildirimlerini Office çözümleri yayımcıyı tanımlayan bir sertifika ile imzalanmalıdır. Sertifika güven kararları için bir temel sunar.

 Geçici bir sertifika için oluşturduğunuz ve siz hata ayıklarken çözümü çalıştıracak şekilde güven oluşturma zamanında verilir. Geçici bir sertifikayla imzalanan bir çözüm yayımlarsanız, son kullanıcı güveni kararı vermeniz istenir.

 Çözüm bilinen ve güvenilen bir sertifika ile oturum açarsanız, çözümün güven karar vermek için son kullanıcıya sormadan otomatik olarak yüklenir. İmzalama için bir sertifikanın nasıl alınacağı hakkında daha fazla bilgi için bkz. [ClickOnce ve Authenticode](../deployment/clickonce-and-authenticode.md). Bir sertifika alındıktan sonra sertifikayı güvenilen yayımcılar listesine ekleyerek açıkça güvenilmelidir. Daha fazla bilgi için [nasıl yapılır: ClickOnce uygulamaları için bir istemci bilgisayara güvenilir yayımcı ekleme](../deployment/how-to-add-a-trusted-publisher-to-a-client-computer-for-clickonce-applications.md).

 Geliştirici çözümü geçici bir sertifika ile imzalar, yöneticinin özelleştirme bilinen ve güvenilen bir sertifika ile bildirim oluşturma ve düzenleme aracı kullanarak yeniden oturum açabilir (*mage.exe*), birinde Microsoft .NET Framework Araçları. Çözümleri imzalama hakkında daha fazla bilgi için bkz. [nasıl yapılır: Office çözümlerini imzalama](../vsto/how-to-sign-office-solutions.md) ve [nasıl yapılır: Uygulama ve dağıtım bildirimlerini imzalama](../ide/how-to-sign-application-and-deployment-manifests.md).

##  <a name="TrustPrompt"></a>Çözümü ClickOnce güven istemi kullanarak güven
 [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] çözümün sertifika güvenleri hiçbir kuruluş genelinde bir ilke varsa güven kararı son kullanıcının ister. Son kullanıcı çözüme güven verirse, bu güven karar depolamak için bir URL ve ortak anahtar içeren bir ekleme listesi girişi oluşturulur. Daha sonra güvenilir özelleştirme çalıştırıldığında, son kullanıcının yeniden sorulmaz.

 Yöneticiler devre dışı bırakabilirsiniz [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] güven istemi veya istemi Authenticode sertifikası ile imzalanmış çözümleri için gerçekleşmesini gerektirir. Bilgisayarım LocalIntranet Internet TrustedSites ve UntrustedSites bölgeler için bu ayarları değiştirme hakkında daha fazla bilgi için bkz. [nasıl yapılır: ClickOnce güven istemi davranışını yapılandırma](../deployment/how-to-configure-the-clickonce-trust-prompt-behavior.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümleri güvenliğini sağlama](../vsto/securing-office-solutions.md)
- [Belgelere güven verme](../vsto/granting-trust-to-documents.md)
- [Office çözüm güvenliğinde sorunlarını giderme](../vsto/troubleshooting-office-solution-security.md)
- [Office çözümleriyle ilgili belirli güvenlik konuları](../vsto/specific-security-considerations-for-office-solutions.md)