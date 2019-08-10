---
title: Yük testi sonuçlarını yönetme
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, results repository
- results, load test
- load test results, repository
- Load Test Results Repository
ms.assetid: 1cd63c4b-4f74-4133-b675-5e8fbeab25f3
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 37dfd7b0aa8aed1ce94f3d4364c5b61a0957a223
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926617"
---
# <a name="manage-load-test-results-in-the-load-test-results-repository"></a>Yük testi sonuçları deposu içindeki yük testi sonuçlarını yönetme

Yük testlerinizi çalıştırdığınızda, yük testi çalıştırması sırasında toplanan herhangi bir bilgi depolanabilir *Yük Testi Sonuçları Deposu*, SQL veritabanı. Yük testi sonuçları deposu, performans sayacı verileri ve kaydedilmiş hatalar hakkındaki tüm bilgileri içerir. Sonuçlar deposu veritabanı, denetleyiciler için kurulum tarafından oluşturulan veya otomatik olarak yük testinin ilk yerel çalıştırma oluşturulur. Yerel çalıştırma için yük testi şeması yoksa veritabanını otomatik olarak oluşturulur.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

Farklı bir sunucu kullanmak için denetleyicinin sonuç depo bağlantı dizesini değiştirirseniz, yeni sunucuya olmalıdır *loadtestresultsrepository.sql* şema oluşturmak için betiği çalıştırın.

Visual Studio Enterprise teknolojiye dayalı ortak performans sayaçlarını toplayan adlandırılmış sayaç kümeleri sağlar. Bu ayarlar, bir IIS sunucusu, ASP.NET sunucusu veya SQL server analiz edilirken yararlı olur. Tüm sayaç kümeleriyle toplanan veriler yük testi sonuçları deposunda depolanır.

> [!IMPORTANT]
> Performans sayaç verisi ve sayaç kümesi arasında bir fark yoktur. Bir sayaç kümesi meta verisidir. Bu, IIS veya SQL Server gibi belirli bir rol gerçekleştiren bir bilgisayardan toplanması gereken performans sayaçlarının bir grubu tanımlar. Sayaç kümesi yük testi tanımının bir parçasıdır. Sayaç kümeleri üzerinde performans sayacı verilerini dayalı olarak toplanır, belirli bir bilgisayar ve örnek hıza sayaç eşlemesi ayarlayın.

## <a name="sql-server-versions"></a>SQL Server sürümleri

Yük testleri kullanmak için SQL Server Express Visual Studio ile yüklenen LocalDB kullanabilirsiniz. Bu yük testleri (Microsoft Excel tümleştirmesi dahil) için varsayılan veritabanı sunucusudur. SQL Server Express LocalDB, program geliştiricileri hedefleyen SQL Server Express yürütme modudur. SQL Server Express LocalDB yükleme, SQL Server Veritabanı Altyapısı'nı başlatmak için gerekli dosyaları en az sayıda kopyalar.

Ekibinizin ağır veritabanı gereksinimlerini bekliyor ya da projeleriniz SQL Server Express LocalDB aşıyorsa, SQL Express veya tam SQL Server için daha fazla ölçekleme sağlamak için yükseltme düşünmelisiniz. SQL Server yükseltmesi yapıyorsanız, SQL Server Express LocalDB MDF ve LDF dosyaları kullanıcı profili klasöründe depolanır. Bu dosyalar, SQL Server Express veya SQL Server için yük testi veritabanı içeri aktarma için kullanılabilir.

## <a name="load-test-results-store-considerations"></a>Yük testi sonuç deposuyla ilgili hususlar

Visual Studio Enterprise yüklü olduğunda bilgisayarda yüklü olan SQL Express örneği kullanmak için yük testi sonuçları deposu ayarlanır. SQL Express en fazla 4 GB disk alanı kullanmakla sınırlıdır. Uzun bir süre boyunca çok yükleme testi çalıştıracaksanız, yük testi sonuçları deposunu varsa SQL Server ürününün tam sürümünün bir örneğini kullanması için yapılandırmayı düşünmelisiniz.

## <a name="load-test-analyzer-tasks"></a>Yük Testi Çözümleyicisi görevleri

|Görevler|İlişkili konular|
|-|-----------------------|
|**Yük testi sonuçları deposu ayarlama:** Bir SQL veritabanında yük testi sonuçları deposu ayarlayabilirsiniz. **Not:**  Bir test denetleyicisi yüklediğinizde, yük testi deposu da oluşturulabilir. Daha fazla bilgi için [yüklemek ve test denetleyicisilerinin](../test/lab-management/install-configure-test-agents.md).||
|**Bir sonuç deposunu seçme ve görüntüleme:** Belirli bir sonuç deposu seçebilirsiniz. Bir yerel sonuç deposuyla sınırlı değildir. Sık, yük testleri Aracı bilgisayarların bir uzak kümesi üzerinde çalıştırılır. Test sonuçları, aracılarınız veya yerel bilgisayarınız bir yük testi sonuçları deposu oluşturmuş olduğunuz herhangi bir SQL Server'a kaydedilebilir. Her iki durumda da kullanarak yük testi sonuçlarınızın depolanacağı konumu tanımlamalısınız **Test Denetleyicilerini Yönet** penceresi.|-   [Nasıl Yapılır: Yük testi sonuç deposu seçin](../test/how-to-select-a-load-test-results-repository.md)<br />-   [Nasıl Yapılır: Analiz için yük testi sonuçlarına erişin](../test/how-to-access-load-test-results-for-analysis.md)|
|**Depodan bir yük testi sonucunu silme:** **Yük Testi Düzenleyicisi** yük testi sonucunu, **Load Test sonuçları aç ve Yönet** iletişim kutusunu kullanarak kaldırabilirsiniz.|-   [Nasıl Yapılır: Yük testi sonuçlarını bir depodan Sil](../test/how-to-delete-load-test-results-from-a-repository.md)|
|**Sonuçları bir depoya içeri ve dışarı aktarma:** Yük testi sonuçlarını **Yük Testi Düzenleyicisi**içeri ve dışarı aktarabilirsiniz.|-   [Nasıl Yapılır: Yük testi sonuçlarını bir depoya içeri aktarma](../test/how-to-import-load-test-results-into-a-repository.md)<br />-   [Nasıl Yapılır: Yük testi sonuçlarını bir depodan dışarı aktar](../test/how-to-export-load-test-results-from-a-repository.md)|

## <a name="related-tasks"></a>İlişkili görevler

[Yük testi sonuçlarını çözümleme](../test/analyze-load-test-results-using-the-load-test-analyzer.md)

Kullanarak hem çalışan bir yük testi hem de tamamlanmış bir yük testi sonuçlarını görüntüleyebilirsiniz **Yük Testi Çözümleyicisi**.

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi sonuçlarını çözümleme](../test/analyze-load-test-results-using-the-load-test-analyzer.md)
- [Nasıl yapılır: Analiz için yük testi sonuçlarına erişin](../test/how-to-access-load-test-results-for-analysis.md)