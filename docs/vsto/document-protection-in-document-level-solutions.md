---
title: Belge düzeyi çözümlerde belge koruması
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- restricted permissions [Office development in Visual Studio]
- permissions [Office development in Visual Studio]
- workbooks [Office development in Visual Studio], restricted permissions
- Office documents [Office development in Visual Studio], restricted permissions
- documents [Office development in Visual Studio], restricted permissions
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: b6cc01c6506c4a3fca85029a8dcaf08607427ea4
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596717"
---
# <a name="document-protection-in-document-level-solutions"></a>Belge düzeyi çözümlerde belge koruması
  Microsoft Office Word ve Microsoft Office Excel belge düzeyi projelere koruma özellikleri kullanabilirsiniz. Bu özellikler, korumalı bir belge bölümlerine değişiklik yapmasını yetkisiz kullanıcıları engeller.

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

 Çalışma kitabını tasarımcıda açık durumdayken Excel kullanarak, koruma açıp kapatabilirsiniz. Word'ü kullanarak, koruma yalnızca Tasarımcısı dışında etkinleştirebilirsiniz. Çalışma zamanında etkinleştirebilir veya program aracılığıyla Word ve Excel için korumayı devre dışı bırakın.

 Tasarımcıda açık bir belgede belge koruması etkin olduğunda, tüm denetimler çıkarılır **araç kutusu** veya kullanılamaz yapılan ve herhangi bir şeyin sürükleyemezsiniz **veri kaynakları** Belge penceresi.

## <a name="serverdocument-and-protected-documents"></a>ServerDocument ve korumalı belgeleri
 Bir belge korumalıysa veri önbelleğini belgenin dışında erişilemez. Kullanamazsınız <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> almak veya Korumalı belgede önbelleğe alınmış verileri işlemek için sınıf ya da diğer yöntemlerini <xref:Microsoft.VisualStudio.Tools.Applications.Runtime.ServerDocument> sınıfı.

## <a name="word-document-protection-in-the-designer"></a>Tasarımcıda Word belge koruması
 Visual Studio'da açıkken koruma bir Word belgesi veya şablonu eklerseniz, Tasarımcı koruma başlayamazsınız. Visual Studio'da açık olduğundan ve koruma uygulanması başlamadan önce çalışma modunda gerekir, belge tasarım modda değil.

 Ancak, koruması etkinleştirilmiş olan mevcut bir Word belgesi kullanan bir proje oluşturursanız, açıkken tasarımcıda belge korunuyor. Korumalı belge parçalarını düzenleyemezsiniz, ancak yine de belge otomatik hale getirmek için Kod Düzenleyicisi'nde kod yazabilirsiniz. Belge, Visual Studio'da açıkken protection etkinleştirildiyse, ayrıca projesi derlenemiyor.

 Belgeyi düzenleyin ve projeyi derleyin, belgeyi tasarımcıda açıkken korumayı kapatabilirsiniz. Hata ayıklama sırasında tasarımcıda kopya için korumayı devre dışı bırakamazsınız; hata ayıklama sırasında açılan belge bir açık Tasarımcı içinde ayrı bir kopyasıdır (çıkış kopya depolanır *\bin* Visual Basic'te dizin ve *\bin\debug* dizinini C# ).

 Visual Studio'da proje kapatıldığında, proje dizininde belgeyi kopyasını açıp korumayı etkinleştirme tasarımcıda açılır. belgenin kopyasında korumayı etkinleştirebilirsiniz.

## <a name="enforce-word-document-protection-on-build"></a>Word Belge Korumasını zorla
 Koruma etkin hata ayıklama için bir belge açıldığında, böylece visual Studio derleme işlemi sırasında koruma Word belgelerini ve şablonlar için zorlama başlatır. Belge boş bir parolayla korunuyor.

 Koruma belgede kod varsa derleme sırasında etkindir <xref:Microsoft.Office.Tools.Word.Document.Startup> özel durumlarına neden veya uygulamanın davranışını değiştirme olay bu kod hata ayıklaması yapılması doğru. Belge açıldıktan sonra korumayı etkinleştirin, başlatma kodu hata ayıklama veya test.

## <a name="setting-the-password"></a>Parola ayarlama
 Visual Studio otomatik olarak koruma sağlar, ancak varsayılan olarak parola sağlar. Çözümünüzü dağıtmadan önce bir parola sağlamak için belge koruması istiyorsanız eklemelisiniz. Bir parola eklemek, yetkili kullanıcıların belgeden korumayı kaldırmalarına olanak sağlar; bir parola olmadan koruma bir kolayca kaldırılamaz. Bir parola ayarlama hakkında daha fazla bilgi için belirli Office uygulamasında yardımına bakın.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Program aracılığıyla belgeleri ve belge parçalarını koruma](../vsto/how-to-programmatically-protect-documents-and-parts-of-documents.md)
- [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)
- [Bilgi Hakları Yönetimine ve yönetilen kod uzantılarına genel bakış](../vsto/information-rights-management-and-managed-code-extensions-overview.md)
- [Office belgelerinde parola koruması](../vsto/password-protection-on-office-documents.md)
- [Nasıl yapılır: Kodun kısıtlı izinle belgelerin arkasında çalışmasına izin](../vsto/how-to-permit-code-to-run-behind-documents-with-restricted-permissions.md)
- [Office çözümleri oluşturma ve tasarlama](../vsto/designing-and-creating-office-solutions.md)
