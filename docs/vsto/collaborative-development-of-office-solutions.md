---
title: Office çözümlerinin işbirlikçi geliştirmesi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office applications [Office development in Visual Studio], collaborative development
- Office development in Visual Studio, collaboration
- source control [Office development in Visual Studio]
- collaborative development [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 76c26a110d88d3dee8bf7540647ea0bfde4e7c4f
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56635065"
---
# <a name="collaborative-development-of-office-solutions"></a>Office çözümlerinin işbirlikçi geliştirmesi
  Birden çok geliştirici Office projesinde diğer Visual Studio projelerinde bunlar birlikte aynı şekilde çalışabilir. Farklı konumlarda Office yüklü olsa bile visual Studio her bilgisayara Microsoft Office yükleme doğru şekilde bulur. Ancak, dikkat edilmesi gereken bazı önemli noktalar vardır.

 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]

## <a name="debug-properties-are-not-shared"></a>Hata ayıklama özellikleri paylaşılmaz
 Hata ayıklama özellikleri kaynak denetimi altında birden çok kullanıcı arasında paylaşılan değil. Visual Basic ve Visual C# projeleri, bir kullanıcıya özel dosyada hata ayıklama özelliklerini depolar (*ProjectName*. vbproj.user veya *ProjectName*. csproj.user), ve bu dosya kaynak denetimi altında değil . Her kullanıcı birden fazla kişi hata ayıklama, hata ayıklama özelliklerini el ile girmeniz gerekir.

 Proje kaynak denetiminde yerine bir ağ paylaşımı üzerinde barındırılıyorsa, çözümü açın ve derleme test etmek işbirliği yapan geliştiricilerin için bazı ek adımlar atılmalıdır.

## <a name="source-control-requires-checking-out-all-files"></a>Kaynak Denetimi tüm dosyalar kullanıma alınıyor gerektirir.
 Projeleriniz için kaynak denetimini kullanırsanız, tüm dosyaların altında bir kod dosyasında denetlemelisiniz **Çözüm Gezgini** (gibi *ThisDocument*, *ThisWorkbook*, veya *ThisAddIn* kod dosyaları) her kod dosyasını değiştirdiğinizde, varsayılan olarak gizlidir dosyalar bile. Yalnızca üst düzey kod dosyasını kullanıma işaretlerseniz, değişiklikler kaybolabilir.

 Değişikliklerinizi yaptıktan sonra tüm dosyaları geri denetleyin. Projelerinde, kod dosyaları hakkında daha fazla bilgi için bkz. [Visual Studio ortamında Office projeleri](../vsto/office-projects-in-the-visual-studio-environment.md).

## <a name="security-for-informal-collaboration-on-a-network"></a>Bir ağ üzerinde resmi olmayan işbirliği için güvenlik
 Bir ağ konumuna olan tüm belge düzeyi çözümleri (gibi \\ \\ *Servername*\\*Sharename*), tam olarak belirtilen konumda eklenmelidir çalıştığınız Microsoft Office uygulamasının güvenilen klasör listesi. Ana klasörü altında alt dizinleri içerir veya özellikle hata ayıklama ekleyin ve güvenilir bir klasör listesine klasörleri oluşturmak için bu seçeneği seçin. Bunun nasıl yapılacağı hakkında daha fazla bilgi için bkz. [belgelere güven verme](../vsto/granting-trust-to-documents.md).

 Derleme sırasında otomatik olarak oluşturulan geçici sertifikalar parolaları tarafından sağlanmaz. Sertifikalar, geliştiricilere yönelik oturum açma adı ve diğer kişisel bilgilerini içerir. Geçici sertifikalar tarafından imzalanan özelleştirmeleri dağıtırsanız, başkalarının bu bilgilere erişmek mümkün olabilir.

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümleri güvenliğini sağlama](../vsto/securing-office-solutions.md)
- [Office çözümleri oluşturma ve tasarlama](../vsto/designing-and-creating-office-solutions.md)
- [Office çözümleri oluşturun](../vsto/building-office-solutions.md)
