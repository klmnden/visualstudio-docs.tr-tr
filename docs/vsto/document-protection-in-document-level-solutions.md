---
title: Belge düzeyi çözümlerde Belge koruması
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
ms.openlocfilehash: 6c5f019907495c3cad3fddef501455aedf345bb2
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253803"
---
# <a name="document-protection-in-document-level-solutions"></a>Belge düzeyi çözümlerde Belge koruması
  Belge düzeyi projelerinde Microsoft Office Word ve Microsoft Office Excel 'in koruma özelliklerini kullanabilirsiniz. Bu özellikler yetkisiz kullanıcıların bir belgenin korunan bölümlerinde değişiklik yapmasını engeller.

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

 Excel kullanarak, çalışma kitabı tasarımcıda açıkken korumayı açıp kapatabilirsiniz. Word kullanarak korumayı yalnızca Tasarımcı dışında etkinleştirebilirsiniz. Çalışma zamanında, hem Word hem de Excel için korumayı programlı bir şekilde etkinleştirebilir veya devre dışı bırakabilirsiniz.

 Tasarımcıda açık olan bir belge üzerinde belge koruması etkinleştirildiğinde, tüm denetimler **araç kutusundan** kaldırılır veya kullanılamaz hale getirilir ve **veri kaynakları** penceresinden belgeye hiçbir şey sürükleyemezsiniz.

## <a name="serverdocument-and-protected-documents"></a>ServerDocument ve korumalı belgeler
 Bir belge korunuyorsa, veri önbelleğine belge dışından erişilemez. Korumalı bir belgede önbelleğe <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> alınmış verileri almak veya işlemek ya da <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> sınıfının diğer yöntemlerini kullanmak için sınıfını kullanamazsınız.

## <a name="word-document-protection-in-the-designer"></a>Tasarımcıda Word belge koruması
 Visual Studio 'da açıkken bir Word belgesine veya şablonuna koruma eklerseniz, tasarımcıda korumayı zorunlu hale başlatamazsınız. Belge, Visual Studio 'da açıkken Tasarım modundadır ve korumayı zorlamaya başlayabilmeniz için önce çalışma modunda olmalıdır.

 Ancak, koruması etkin olan mevcut bir Word belgesini kullanan bir proje oluşturursanız, belge tasarımcıda açıldığında korunur. Belgenin korunan bölümlerini düzenleyemezsiniz, ancak belgeyi otomatik hale getirmek için kod düzenleyicisinde kod yazmaya devam edebilirsiniz. Ayrıca, belge Visual Studio 'da açıkken koruma etkinleştirildiyse projeyi derlenemez.

 Belgeyi düzenlemek ve projeyi derlemek için belge tasarımcıda açıkken korumayı devre dışı bırakabilirsiniz. Hata ayıklarken tasarımcıda kopyalamaya yönelik korumayı devre dışı bırakabilirsiniz; hata ayıklama sırasında açılan belge, tasarımcıda açık olan ayrı bir kopyadır (çıkış kopyası Visual Basic için *\Bin* dizininde ve için C# *\Bin\Debug* dizini ' nde depolanır).

 Visual Studio 'da projeyi kapatarak, proje dizininde bulunan belgenin kopyasını açarak ve korumayı etkinleştirerek, tasarımcıda açılan belgenin kopyasında korumayı etkinleştirebilirsiniz.

## <a name="enforce-word-document-protection-on-build"></a>Derlemede Word belge korumasını zorla
 Visual Studio, derleme işlemi sırasında Word belgelerinin ve şablonlarının korunmasını zorlamaya başlar. böylece, belge hata ayıklama için açıldığında koruma etkinleştirilir. Belge boş bir parolayla korunuyor.

 Uygulama, özel durumlara neden olabilecek veya uygulamanın davranışını değiştirebilen belge <xref:Microsoft.Office.Tools.Word.Document.Startup> olayında kod varsa, bu kodun doğru şekilde ayıklanamayacağını belirten derleme sırasında koruma etkinleştirilir. Belge açıldıktan sonra korumayı etkinleştirirseniz, başlatma kodunun hataları ayıklanamaz veya test edilemez.

## <a name="setting-the-password"></a>Parolayı ayarlama
 Visual Studio otomatik olarak korumayı sağlar, ancak varsayılan olarak parola sağlamaz. Belge korumasının bir parolası olmasını istiyorsanız çözümünüzü dağıtmadan önce eklemeniz gerekir. Parola eklemek yetkili kullanıcıların belgeden korumayı kaldırmasını sağlar; parola olmadan koruma kolayca kaldırılamaz. Parola ayarlama hakkında daha fazla bilgi için, bkz. ilgili Office uygulamasındaki Yardım.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Belgeleri ve belge parçalarını programlı bir şekilde koruma](../vsto/how-to-programmatically-protect-documents-and-parts-of-documents.md)
- [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)
- [Bilgi hakları yönetimine ve yönetilen kod uzantılarına genel bakış](../vsto/information-rights-management-and-managed-code-extensions-overview.md)
- [Office belgelerinde parola koruması](../vsto/password-protection-on-office-documents.md)
- [Nasıl yapılır: Kodun, kısıtlı izinlerle belgelerin arkasında çalışmasına izin verme](../vsto/how-to-permit-code-to-run-behind-documents-with-restricted-permissions.md)
- [Office çözümleri tasarlama ve oluşturma](../vsto/designing-and-creating-office-solutions.md)
