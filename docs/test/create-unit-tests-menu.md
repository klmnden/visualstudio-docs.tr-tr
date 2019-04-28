---
title: Birim test yöntemini saplamalar oluşturma
ms.date: 04/01/2019
ms.topic: conceptual
helpviewer_keywords:
- unit testing, create unit tests
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e7eb72f104560991f1bb191e62641041879df071
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62965492"
---
# <a name="create-unit-test-method-stubs-with-the-create-unit-tests-command"></a>Birim test yöntemini saptamalar ile birim testleri Oluştur komutu oluşturun.

**Birim testleri Oluştur** komut, birim test yöntemini saptamalar oluşturur. Bu özellik, bir test projesi ve test sınıfı içindeki test metodu saptaması kolayca yapılandırmasını sağlar.

> [!NOTE]
> **Birim testleri Oluştur** menü komutu, yalnızca .NET Framework (ancak .NET Core) hedefleyen yönetilen kod için kullanılabilir.

**Birim testleri Oluştur** menü komutu genişletilebilir ve MSTest, MSTest V2, NUnit ve xUnit testleri oluşturmak için kullanılabilir.

## <a name="get-started"></a>Kullanmaya başlayın

Başlamak için Kod Düzenleyicisi'nde, test etmek istediğiniz projeye bir yöntem, bir tür veya ad alanı seçin, sağ tıklatın ve ardından **birim testleri Oluştur**. **Birim testleri Oluştur** yapılandırabileceğiniz oluşturulması için testleri nasıl istediğinizi iletişim kutusu açılır.

![Birim Testleri Oluştur komutunu kullanarak](media/createunittestcommand.png)

## <a name="set-unit-test-traits"></a>Birim testi Özellikleri Ayarla

Test Otomasyonu işleminin bir parçası olarak bu testleri çalıştırmayı planlıyorsanız, başka bir test projesi (yukarıdaki iletişim ikinci seçenek) oluşturulan test sahip düşünebilirsiniz ve nitelikler, birim testi için test ayarı birimi. Bu, daha kolay dahil etmek veya sürekli tümleştirme veya sürekli dağıtım işlem hattı bir parçası olarak bu belirli testleri dışlamak sağlar. Nitelikler aşağıda gösterildiği gibi meta veriler için birim testi doğrudan ekleyerek ayarlanır.

![Birim testi özellikleri ayarlama](media/createunittest.png)

## <a name="use-third-party-unit-test-frameworks"></a>Üçüncü taraf birim test çerçeveleri kullanma

NUnit veya xUnit birim testleri otomatik olarak oluşturmak için bu test framework uzantılara Visual Studio Market'ten yükleyin:

* [NUnit test oluşturucuları uzantısı](https://marketplace.visualstudio.com/items?itemName=NUnitDevelopers.TestGeneratorNUnitextension)
* [test oluşturucuları için ise xUnit.net uzantısı](https://marketplace.visualstudio.com/items?itemName=BradWilson.xUnitnetTestExtensions)

## <a name="when-should-i-use-this-feature"></a>Bu özellik ne zaman kullanmalıyım?

Bu özelliği kullanmak için birim testleri oluşturmak için ihtiyacınız olduğunda, ancak özellikle mevcut kodunuzu sınarken çok az kayıpla veya hiç test kapsamı ve hiçbir belge sahip. Diğer bir deyişle, burada sınırlı veya var olmayan kod belirtimi. Etkili bir şekilde benzer bir yaklaşım uygular [akıllı birim testleri](https://devblogs.microsoft.com/devops/introducing-smart-unit-tests/) , kod gözlemlenen davranışını belirtir.

Ancak, bir geliştirici bazı kodlar yazarak başlar ve ardından birim testleri önyüklemenizi kullanan bu özellik eşit oranda geçerlidir. Kodlama, akış içinde Geliştirici hızlı bir şekilde bir birim test metodu saptaması (ile uygun test sınıfı ve uygun bir test projesi) için belirli bir kod parçasını oluşturmak isteyebilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

- [Birim testi "Birim Testleri Oluştur ile" yöntemi saplamalar oluşturma](https://devblogs.microsoft.com/devops/creating-unit-test-method-stubs-with-create-unit-tests/)
- [Birim testi blog gönderileri](https://devblogs.microsoft.com/devops/?s=unit+testing)
