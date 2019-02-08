---
title: Birim test yöntemini saplamalar oluşturma
ms.date: 05/02/2017
ms.topic: conceptual
helpviewer_keywords:
- unit testing, create unit tests
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 577cb338e7cbf20b23d2d75ad2dfded017b0aacb
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55955147"
---
# <a name="create-unit-test-method-stubs-with-the-create-unit-tests-command"></a>Birim test yöntemini saptamalar ile birim testleri Oluştur komutu oluşturun.

Visual Studio **birim testleri Oluştur** komut, birim test yöntemini saplamalar oluşturma olanağı sağlar. Bu özellik, bir test projesi ve test sınıfı içindeki test metodu saptaması kolayca yapılandırmasını sağlar.

## <a name="availability-and-extensions"></a>Kullanılabilirlik ve uzantıları

**Birim testleri Oluştur** menü komutu:

* Community, Professional ve Enterprise sürümleri, Visual Studio 2015 kullanılabilir ve üzerinde desteklenir.

* .NET Framework'ü hedefleyen yalnızca C# kodunu destekler.

* Genişletilebilir ve yayan testleri, MSTest, MSTest V2, NUnit, xUnit biçimini destekler.

* Henüz .NET Core projelerinde kullanılamaz.

## <a name="get-started"></a>Kullanmaya başlayın

Başlamak için bir yöntem, bir tür veya ad alanı Kod Düzenleyicisi'nde test, kısayol menüsünü açın ve istediğiniz projeyi seçin **birim testleri Oluştur**. **Birim testleri Oluştur** iletişim kutusunu açar, burada yeni birim testleri oluşturma seçeneklerini seçilebilir.

![Birim Testleri Oluştur komutunu kullanarak](media/createunittestcommand.png)

## <a name="setting-unit-test-traits"></a>Birim testi özellikleri ayarlama

Test Otomasyonu işleminin bir parçası olarak bu testleri çalıştırmayı planlıyorsanız, başka bir test projesi (yukarıdaki iletişim ikinci seçenek) oluşturulan test sahip düşünebilirsiniz ve nitelikler, birim testi için test ayarı birimi. Bu, daha kolay dahil etmek veya sürekli tümleştirme veya sürekli dağıtım işlem hattı bir parçası olarak bu belirli testleri dışlamak sağlar. Nitelikler aşağıda gösterildiği gibi meta veriler için birim testi doğrudan ekleyerek ayarlanır.

![Birim testi özellikleri ayarlama](media/createunittest.png)

## <a name="using-third-party-unit-test-frameworks"></a>Üçüncü taraf birim test çerçeveleri kullanma

Visual Studio ile herhangi bir test çerçevesi kullanılarak sizin için oluşturulan birim testlerini kolayca olabilir. Diğer test çerçevelerini yüklemek için:

1. Seçin **Araçları** > **Uzantılar ve güncelleştirmeler**.
2. Genişletin **çevrimiçi** > **Visual Studio Market** > **Araçları**ve ardından **test**.

![Üçüncü taraf test çerçevelerini kullanarak](media/createunittestfx.png)

Test framework uzantıları Visual Studio Marketi'nde mevcuttur:

* [NUnit test oluşturucuları uzantısı](https://marketplace.visualstudio.com/items?itemName=NUnitDevelopers.TestGeneratorNUnitextension)
* [test oluşturucuları için ise xUnit.net uzantısı](https://marketplace.visualstudio.com/items?itemName=BradWilson.xUnitnetTestExtensions)

## <a name="when-should-i-use-this-feature"></a>Bu özellik ne zaman kullanmalıyım?

Bu özelliği kullanmak için birim testleri oluşturmak için ihtiyacınız olduğunda, ancak özellikle mevcut kodunuzu sınarken çok az kayıpla veya hiç test kapsamı ve hiçbir belge sahip. Diğer bir deyişle, burada sınırlı veya var olmayan kod belirtimi. Etkili bir şekilde benzer bir yaklaşım uygular [akıllı birim testleri](https://blogs.msdn.microsoft.com/devops/2014/11/19/introducing-smart-unit-tests/) kod gözlemlenen davranışını özelleştirmek.

Ancak, bu özellik burada Geliştirici bazı kodlar yazarak başlar ve birim uzmanlık alanı testi bootstrap kullanan durumunuza eşit oranda geçerlidir. Kodlama, akış içinde Geliştirici hızlı bir şekilde bir birim test metodu saptaması (ile uygun test sınıfı ve uygun bir test projesi) için belirli bir kod parçasını oluşturmak isteyebilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

- [Birim testi "Birim Testleri Oluştur ile" yöntemi saplamalar oluşturma](https://blogs.msdn.microsoft.com/devops/2015/03/06/creating-unit-test-method-stubs-with-create-unit-tests/)
- [Birim testi blog gönderileri](https://blogs.msdn.microsoft.com/devops/?s=unit+testing)
