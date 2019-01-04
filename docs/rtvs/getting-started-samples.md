---
title: Örnek R projeleri
description: Bir dizi örnek, Visual Studio ve R ile başlamak için dizini.
ms.date: 01/24/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: douge
ms.workload:
- data-science
ms.openlocfilehash: 80553e54489b5c887facca57f3491fd81fd8d24b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53837465"
---
# <a name="r-tools-for-visual-studio-sample-projects"></a>Örnek projeleri Visual Studio için R araçları

Bu örnekleri koleksiyonunu, R, Visual Studio (RTVS) ve Microsoft Machine Learning sunucusu için R araçları kullanmaya başlamanızı sağlar:

1. İndirme [örnekleri zip dosyası](https://github.com/Microsoft/RTVS-docs/archive/master.zip) ve seçtiğiniz bir klasöre ayıklayın.
1. Açık `examples/Examples.sln` projede iki klasör görmek için:

    - *İlk bakış R adresindeki* r için yeni gelenlere için size bir giriş sağlar.
    - *MRS ve Machine Learning* machine learning için R ve Microsoft Machine Learning sunucusu kullanma örnekleri sağlar.

## <a name="a-first-look-at-r"></a>R ilk göz

Bu örnek, R iki kaynak dosyalarında kapsamlı açıklamaları arasında ayrıntılı bir giriş sağlar. En iyi deneyimi dosyasının en üstüne imleci yerleştirin ve kod satırı-tarafından-kalan için göndermek için Ctrl + Enter tuşlarına basın **R etkileşimli** penceresi. (Yükleme paketleri satırları veya iki tamamlanması bir dakika sürebilir.)

- `1-Getting Started with R.R` paketleri kullanma, yükleme ve verileri çözümleme ve çizim dahil olmak üzere birçok R temelleri ele alınmaktadır.

    ![Örnek 1-Başlarken R.R örnek çıktısı](media/samples-getting-started-output.png)

- `2-Introduction to ggplot2.R` Basit söz dizimi ve görsel olarak çekici çizimler için bilinen ggplot2 grafik paket tanıtır. Bu örnekte, Fiji deprem verilerden görselleştirir.

    ![2-giriş ggplot2 için çıktı örneği. Örnek R](media/samples-ggplot-output.png)

## <a name="microsoft-machine-learning-server-and-machine-learning"></a>Microsoft Machine Learning sunucusu ve makine öğrenimi

Bu koleksiyon örnek makine öğrenimi modelleri oluşturma ve yararlanmak için R kullanmayı gösterir [Microsoft Machine Learning sunucusu](/machine-learning-server/what-is-machine-learning-server).

Tüm örnekleri ile dosya sayısı arttıkça, üstünde imleci yerleştirin ve ardından kodu satır satır ile **Ctrl**+**Enter**. Her klasöründeki markdown dosyaları ek bilgiler de içerir.

- `Benchmarks` Microsoft R Open ve Intel matematik çekirdek Kitaplığı'nı (MKL) kullanarak, bir dizi performans göstermesini doğrusal Cebir yoğun, paralel hesaplamalar kazançları çalıştırmaları mümkündür. Sanal verilerle birlikte Kıyaslama noktalarını, özellikle iki yerine tek bir iş parçacığı matris hesaplamaları karşılaştırın.

    ![Örnek Kıyaslama çizimi](media/samples-mro-benchmark-plot.png)

- `Bike_Rental_Estimation_with_MRS` bisiklet kiralama bir geçmiş verileri kullanarak Microsoft ML Server kümesini temel alan için bir talep tahmin modeli oluşturur. 

- `Data_Exploration` üç betik içerir:

  - `Import Data from URL.R` r bir URL tanımlanan veri dosyası yükleme işlemini gösterir
  - `Import Data from URL to xdf.R` Microsoft ML Server bir xdf olarak bir URL tanımlanan veri dosyası yükleme işlemi gösterilmektedir.
  - `Using ggplot2.R` bir uzantısıdır `A First Look at R/2-Introduction to ggplot2.R` örnek, veren ggplot2'ın işlevsellik etkileşimli 3B çizim dahil olmak üzere daha kapsamlı bir turu.

      ![Ggplot2 kullanarak çıktı. Örnek R](media/samples-3d-interactive.png)

- `Datasets` üç içeren *.csv* diğer örnekleri tarafından kullanılan dosyalar
- `Flight_Delays_Prediction_with_R` ve `Flight_Delays_Prediction_with_MRS` uçuş gecikme R, makine öğrenimi ve geçmişteki tarihlere ait zamanında kalkış performansı ve hava durumu verileri kullanarak tahmin işlemi gösterilmektedir. 
- `Machine learning` Uçuş gecikme, konut fiyatları ve bisiklet kiralama tahmin etmek öğrenme için üç örnekleri içerir. Birlikte, bu örnekler Microsoft ML Server ile R ve uygulamayı gerçek dünyadaki sorunları gösterir. Bunlar ayrıca, çeşitli popüler makine öğrenimi modellerini kullanın ve bunları kullanarak Azure Web hizmeti olarak dağıtma hakkında bilgi sağlanmıştır bir [Azure Machine Learning](https://azure.microsoft.com/services/machine-learning/) çalışma.

- `R_MRO_MRS_Comparison` benzerlikleri ve farkları, R, Microsoft R Open ve Microsoft ML Server komutları, söz dizimi, yapıları ve performans ile gösteren bir Particle karşılaştırmasıdır.

## <a name="whats-special-about-microsoft-r-open-and-microsoft-ml-server"></a>Microsoft R Open ve Microsoft ML Server hakkında özel nedir?

[Microsoft R Open](http://aka.ms/rtvs-r-open), R, Microsoft'un dağılımını farklı [CRAN R](https://cran.r-project.org/) iki önemli şekilde:

1. [Daha iyi performans hesaplama](https://mran.revolutionanalytics.com/rro/#intelmkl1) ile kullanıldığında [Intel matematik çekirdek kitaplıkları](https://software.intel.com/intel-mkl). Kitaplıklar, Microsoft R Open ile kullanmak için Microsoft ücretsiz bir indirme olarak kullanılabilir.

1. [Tekrarlanabilir R Araç Seti](https://mran.revolutionanalytics.com/rro/#reproducibility) R programınızı oluşturmak için kullanılan kitaplıklar her zaman iş yeniden oluşturmak için istediğiniz diğer kullanılabilir olmasını sağlar.

[Microsoft ML Server (MLS)](/machine-learning-server/what-is-machine-learning-server) daha fazla veri işleme ve daha hızlı işlemesi olanak tanıyan R bir uzantısıdır. Bu iki R güçlü yetenekler sunar:

1. RAM kısıtlama olmadan büyük veri kümeleri. ML Server, Hadoop kümeleri, veritabanlarınıza ve veri ambarlarınıza gibi kaynakları çeşitli bellek yetersiz veri işleyebilir.

1. Paralel, çok çekirdekli işleme. MLS verimli bir şekilde hesaplama dağıtmak hesaplama kaynaklarında kullanılabilir vardır. Kişisel istasyonunuzu veya uzak bir kümeye, MLS daha hızlı bir yanıt alır.

Aşağıdaki karşılaştırmaya MLS ve MRO MKL ile R ve MRO MKL olmadan belirli matris hesaplamasından ilgili önemli ölçüde daha iyi hesaplama performans olduğunu gösterir. Sanal verileri kullanarak bu hesaplamada kullanılır:

![MLS ve MRO MKL r ile ve MRO MKL olmadan karşılaştırma](media/samples-speed-comparison.png)

R MRO ve MLS teknik bir karşılaştırması için kullanıma [Lixun Zhang'ın ayrıntılı tartışma](http://htmlpreview.github.io/?https://github.com/lixzhang/R-MRO-MRS/blob/master/Introduction_to_MRO_and_MRS.html) konusunda.

Aşağıdaki şekilde, lojistik regresyon modellerini oluşturmaya, uçuş gecikme 15 dakikadan fazla tahmin etmek için kullanılan saniye sonra geçen süre karşılaştırır.  Geçen süre CRAN R kullanılan MLS yalnızca yaklaşık iki kez artarken küçük bir satır sayısını artırmak, büyük ölçüde artar. Bu kıyaslama ayrıntılarını gözden geçirin *Kıyaslama/rxGlm_benchmark. R* örnek.

![rxGlm Kıyaslama](media/samples-rxGLM-benchmark.png)
