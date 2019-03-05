---
title: Veri bilimi ve analitik uygulamalar iş yükü
description: Bu Visual Studio iş yükü, Python, araya F#ve Anaconda dahil olmak üzere kendi ilgili çalışma zamanı dağıtımlar. (R ayrıca Visual Studio 2017'de yalnızca mevcut değildir.)
ms.date: 02/28/2019
ms.topic: overview
author: kraigb
ms.author: kraigb
manager: jillfra
ms.workload:
- python
- data-science
ms.openlocfilehash: 44dfa13059e16338111bbeb2eb2f0bc6d6b44408
ms.sourcegitcommit: 11337745c1aaef450fd33e150664656d45fe5bc5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57325332"
---
# <a name="install-data-science-support-in-visual-studio"></a>Visual Studio'da veri bilimi desteğini yükleme

Seçin ve Visual Studio yükleyicisi yüklemek, veri bilimi ve analitik uygulamalar iş yükü, çeşitli diller ve onların ilgili çalışma zamanı dağıtımları bir araya getirir:

::: moniker range="vs-2017"
- [Python ve Anaconda](../python/overview-of-python-tools-for-visual-studio.md)
- [F#.NET framework ile](/dotnet/fsharp/)
- [R ve Microsoft R istemcisi](../rtvs/index.md)
::: moniker-end

::: moniker range="vs-2019"
- [Python](../python/overview-of-python-tools-for-visual-studio.md)
- [F#.NET framework ile](/dotnet/fsharp/)
::: moniker-end

![Visual Studio Yükleyicisi'nde veri bilimi ve analitik uygulamalar iş yükü](media/workload/data-science-workload.png)

::: moniker range="vs-2017"
Python ve R veri bilimi için kullanılan birincil komut dosyası dilleri ikisidir. Her iki dil öğrenmek kolaydır ve paketlerin zengin bir ekosisteme tarafından desteklenir. Bu paketleri, çok çeşitli veri alma, temizleme, model eğitiminin, dağıtım ve çizim gibi senaryolar adresi. F#Ayrıca, çok çeşitli veri işleme görevleri için uygun bir güçlü işlevsellik öncelikli .NET dilidir.
::: moniker-end

::: moniker range="vs-2019"
Python, veri bilimi için kullanılan birincil bir betik dilidir. Python öğrenmek kolaydır ve paketlerin zengin bir ekosisteme tarafından desteklenir. Bu paketleri, çok çeşitli veri alma, temizleme, model eğitiminin, dağıtım ve çizim gibi senaryolar adresi. F#Ayrıca, çok çeşitli veri işleme görevleri için uygun bir güçlü işlevsellik öncelikli .NET dilidir. (R dilinin öneririz [Azure not defterleri](https://notebooks.azure.com).)
::: moniker-end

<!--Note link on the image because this one is large -->
[![Visual Studio ile R, Python, ekran görüntüleri veF#](media/workload/data-science-workload-screens.png)](media/workload/data-science-workload-screens.png#lightbox)

## <a name="workload-options"></a>İş yükü seçenekleri

Varsayılan olarak, iş yükünü Visual Studio Yükleyicisi'nde iş yükü için Özet bölümünde değiştirebilirsiniz aşağıdaki seçenekleri yükler:

::: moniker range="vs-2019"
- F#Masaüstü dil desteği
- Python:
  - Python dil desteği
  - Python web desteği
::: moniker-end

::: moniker range="vs-2017"
- F#dil desteği
- Python:
  - Python dil desteği
  - [Anaconda3 64 bit](https://www.continuum.io), kapsamlı bir veri bilimi kitaplıkları ile bir Python yorumlayıcısı içerir bir Python distro.
  - Python web desteği
  - Cookiecutter şablonu desteği
- R:
  - R dil desteği
  - R geliştirme araçları için çalışma zamanı desteği
  - [Microsoft R Client](/machine-learning-server/r-client/what-is-microsoft-r-client) (Microsoft'un tam olarak uyumlu, topluluk tarafından desteklenen İnterpret R ile daha hızlı hesaplama tek düğümler ve kümeler üzerindeki ScaleR kitaplıklarında. Öğesinden herhangi bir R kullanabilirsiniz [CRAN](https://cran.r-project.org/).)
::: moniker-end

## <a name="sql-server-integration"></a>SQL Server tümleştirmesi

::: moniker range="vs-2017"
Hem Python hem de R doğrudan SQL Server içinde Gelişmiş analiz yapmak için SQL Server kullanılmasını destekler. R desteği, SQL Server 2016 ve sonraki sürümlerinde; Python desteği, SQL Server 2017 CTP 2.0 kullanılabilir ve üzerinde desteklenir.
::: moniker-end

::: moniker range=">=vs-2019"
SQL Server, doğrudan SQL Server içinde Gelişmiş analiz yapmak için Python kullanarak destekler. Python desteği, SQL Server 2017 CTP 2.0 kullanılabilir ve üzerinde desteklenir.
::: moniker-end

Aşağıdaki avantajları, verileriniz zaten nerede kodunuzu çalıştırarak keyfini çıkarın:

- **Veri taşıma saydamlığından**: Verileri veritabanından uygulamanızı veya model için taşıma yerine, veritabanı uygulamalar oluşturabilirsiniz. Bu özellik, güvenlik, uyumluluk, idare, bütünlük ve çok büyük miktarda veri moving'e ilgili benzer sorunları çok sayıda engelleri ortadan kaldırır. Bir istemci makinesi belleğe sığması uygulanamadı veri kümeleri de kullanabilir.

- **Kolay dağıtım**: Modeli hazır olduktan sonra Üretim dağıtımı bir T-SQL betiği ekleme basit bir konudur. Herhangi bir SQL istemci uygulama herhangi bir dilde yazılmış bir saklı yordam çağrısı aracılığıyla zeka ve modelleri yararlanabilirsiniz. Hiçbir özel dil tümleştirmelerinin gereklidir.

- **Kurumsal düzeyde performans ve ölçek**: Bellek içi tablo ve sütun dizinleri yüksek performanslı ölçeklenebilir API'leri ile RevoScale paketleri depolamak gibi SQL Server'ın gelişmiş özelliklerini kullanabilirsiniz. Veri taşıma saydamlığından çoğalan veya uygulamanın performansını artırmak istediğiniz istemci bellek kısıtlamaları kaçının anlamına gelir.

- **Zengin genişletilebilirlik**: Yükleme ve SQL Server'ın çok büyük miktarda verileri SQL Server üzerinde derin öğrenme ve yapay ZEKA uygulamaları oluşturmak için en yeni açık kaynak paketlerinden birini çalıştırın. SQL Server'da bir paket yükleme, yerel makinenizde bir paket yüklemek kadar basittir.

- **Hiçbir ek ücret ödemeden geniş kullanılabilirlik**: Dil tümleştirmelerinin Express sürümü de dahil olmak üzere SQL Server 2017 ve sonraki tüm sürümlerinde kullanılabilir.

SQL Server Tümleştirme tam olarak yararlanmak için Visual Studio yükleyicisini kullanma **veri depolama ve işleme** yüküyle **SQL Server veri Araçları** seçeneği. İkinci seçeneği, SQL IntelliSense, sözdizimi vurgulama ve dağıtımını sağlar.

![Veri depolama ve işleme iş yükü](media/workload/data-storage-workload.png) &nbsp;&nbsp;&nbsp;&nbsp; ![Veri depolama ve işleme iş yükü seçenekleri](media/workload/data-storage-workload-options.png)

Daha fazla bilgi için:

::: moniker range="vs-2017"
- [SQL Server ve R ile çalışma](../rtvs/integrating-sql-server-with-r.md)
- [Veritabanı SQL Server 2016 (blog) R ile Gelişmiş analiz](https://blogs.technet.microsoft.com/dataplatforminsider/2016/03/29/in-database-advanced-analytics-with-r-in-sql-server-2016/)
::: moniker-end
- [SQL Server 2017 Python: Gelişmiş veritabanında machine learning (blog)](https://blogs.technet.microsoft.com/dataplatforminsider/2017/04/19/python-in-sql-server-2017-enhanced-in-database-machine-learning/)

## <a name="additional-services-and-sdks"></a>Ek hizmetler ve SDK'lar

Veri bilimi ve analitik uygulamalar iş yükü doğrudan nedir ek olarak, Azure not defterleri hizmet ve Python için Azure SDK'sı ayrıca veri bilimi için yararlıdır.

Python için Azure SDK'sını kullanma ve uygulamaları Windows, Mac ve Linux üzerinde çalışan Microsoft Azure hizmetlerini yönetmenize daha kolay hale getirir. Daha fazla bilgi için [Python için Azure SDK'sı](../python/azure-sdk-for-python.md)

Azure Not Defterleri (şu anda önizlemede), Jupyter not defterleri bulutta Microsoft Azure üzerinde çalışan ücretsiz çevrimiçi erişim sağlar. Hizmet, Python, R, örnek not defterlerini içerir ve F# başlamanıza yardımcı olmak için. Ziyaret [notebooks.azure.com](https://notebooks.azure.com/).

<!--Note link on the image because this one is large -->
[![Ekran görüntüleri, Azure not defterleri ile R örnek giriş](media/workload/data-science-workload-notebooks.png)](media/workload/data-science-workload-notebooks.png#lightbox)
