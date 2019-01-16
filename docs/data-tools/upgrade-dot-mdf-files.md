---
title: .mdf dosyalarını yükseltme
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- SQL Server Express
- SQL Server LocalDB
- LocalDB
- SQLEXPRESS
- upgrading SQLExpress to SQLExpress
- upgrading to LocalDB
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 4e42058d2728d806551ae319112052e664950dab
ms.sourcegitcommit: 5a65ca6688a2ebb36564657d2d73c4b4f2d15c34
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "53863426"
---
# <a name="upgrade-mdf-files"></a>.mdf dosyalarını yükseltme

Bu konu, bir veritabanı dosyası yükseltme seçenekleri açıklar (*.mdf*) Visual Studio'nun daha yeni bir sürümünü yükledikten sonra. Yönergeler için aşağıdaki görevleri içerir:

- Yükseltme daha yeni bir SQL Server Express LocalDB sürümünü kullanmak için bir veritabanı dosyası

- SQL Server Express daha yeni sürümü kullanmak için bir veritabanı dosyası yükseltme

- Visual Studio'da bir veritabanı dosyası ile çalışır ancak veya SQL Server Express LocalDB daha eski bir sürümüyle uyumluluğu korumak

- Varsayılan veritabanı altyapısı SQL Server Express olun

Bir veritabanı dosyasını içeren bir projeyi açmak için Visual Studio'yu kullanabilirsiniz (*.mdf*) veya SQL Server Express LocalDB daha eski bir sürümü kullanılarak oluşturuldu. Ancak, projenizi Visual Studio'da geliştirmeye devam etmek için bu sürüm veya SQL Server Express LocalDB Visual Studio ile aynı makinede yüklü olmalıdır veya veritabanı dosyasını yükseltmeniz gerekir. Veritabanını yükseltirseniz, veya SQL Server Express LocalDB daha eski sürümleri kullanılarak erişmek mümkün olmayacaktır.

Ayrıca dosya sürümü SQL Server Express veya şu anda yüklü olan LocalDB örneği ile uyumlu değilse veya SQL Server Express LocalDB önceki bir sürümü ile oluşturulmuş bir veritabanı dosyanız yükseltme istenebilir. Sorunu çözmek için Visual Studio dosyayı yükseltme yapmanızı ister.

> [!IMPORTANT]
> Yükseltmeden önce veritabanı dosyasını yedekleyin öneririz.

> [!WARNING]
> Yükseltirseniz bir *.mdf* LocalDB 2014'te (V12) 32 bit LocalDB 2016'ya (V13) ya da daha sonra oluşturulan dosya olmayacaktır dosyayı yeniden LocalDB 32-bit sürümünde açabilirsiniz.

Bir veritabanını yükseltmeden önce aşağıdaki ölçütleri dikkate alın:

-   Projeniz daha eski bir sürümü hem de Visual Studio'nun daha yeni bir sürümü üzerinde çalışmak istiyorsanız yükseltmeyin.

-   Uygulamanızı SQL Server Express LocalDB yerine kullanan ortamlarda kullanılacaksa yükseltmeyin.

-   Uzak bağlantılar, uygulamanız kullanıyorsa LocalDB kabul etmez çünkü yükseltmeyin.

-   Uygulamanızı Internet Information Services (IIS) üzerinde dayanıyorsa yükseltmeyin.

-   Bir korumalı alan ortamında veritabanı uygulamalarını test etmek istediğiniz ancak bir veritabanını yönetmek istemiyorsanız, yükseltme yapmayı düşünün.

### <a name="to-upgrade-a-database-file-to-use-the-localdb-version"></a>LocalDB sürümünü kullanmak için bir veritabanı dosyası yükseltmek için

1.  İçinde **Sunucu Gezgini**seçin **veritabanına bağlan** düğmesi.

2.  İçinde **Bağlantı Ekle** iletişim kutusunda, aşağıdaki bilgileri belirtin:

    -   **Veri kaynağı**: `Microsoft SQL Server (SqlClient)`

    -   **Sunucu adı**:

        -   Varsayılan sürümü kullanmak için: `(localdb)\MSSQLLocalDB`.  Bu ProjectV12 ya da ProjectV13, Visual Studio'nun hangi sürümünün yüklü olduğunu ve ilk LocalDB örneği oluşturulduğu bağlı olarak belirtin. **İfadesini MSSQLLocalDB** düğümünde **SQL Server Nesne Gezgini** hangi sürümün onu işaret etmesi gösterir.

        -   Belirli bir sürümünü kullanmak için: `(localdb)\ProjectsV12` veya `(localdb)\ProjectsV13`, burada V12 LocalDB 2014 ve V13 LocalDB 2016.

    -   **Bir veritabanı dosyası iliştirmek**: Birincil fiziksel yolunu *.mdf* dosya.

    -   **Mantıksal ad**: Dosya ile kullanmak istediğiniz adı.

3.  **Tamam** düğmesini seçin.

4.  İstendiğinde, seçin **Evet** dosya yükseltme düğmesi.

    Veritabanı yükseltilir LocalDB veritabanına ekli ve artık LocalDB eski sürümü ile uyumlu değil.

Bağlantı için kısayol menüsünü açarak ve ardından seçerek Localdb'yi kullanmak üzere bir SQL Server Express bağlantı değiştirebilirsiniz **değiştirme bağlantı**. İçinde **değiştirme bağlantı** iletişim kutusunda, sunucu adına değiştirin `(LocalDB)\MSSQLLocalDB`. İçinde **Gelişmiş Özellikler** iletişim kutusunda, emin **kullanıcı örneği** ayarlanır **False**.

### <a name="to-upgrade-a-database-file-to-use-the-sql-server-express-version"></a>SQL Server Express sürümü kullanmak için bir veritabanı dosyası yükseltmek için

1.  Veritabanı bağlantısı için kısayol menüsünden seçin **değiştirme bağlantı**.

2.  İçinde **değiştirme bağlantı** iletişim kutusunda **Gelişmiş** düğmesi.

3.  İçinde **Gelişmiş Özellikler** iletişim kutusunda **Tamam** sunucu adını değiştirmeden düğmesi.

    Veritabanı dosyası geçerli SQL Server Express sürümüyle eşleşecek şekilde yükseltilir.

### <a name="to-work-with-the-database-in-visual-studio-but-retain-compatibility-with-sql-server-express"></a>Visual Studio'da veritabanıyla çalışmaya, ancak SQL Server Express ile uyumluluğu korumak için

-   Visual Studio'da, yükseltme yapmadan projeyi açın.

    -   Projeyi çalıştırmak için seçin **F5** anahtarı.

    -   Veritabanı düzenlemek için açın *.mdf* dosyası **Çözüm Gezgini**ve düğümde genişletme **Sunucu Gezgini** , veritabanı ile çalışmak üzere.

### <a name="to-make-sql-server-express-the-default-database-engine"></a>Varsayılan veritabanı altyapısı SQL Server Express yapma

1.  Menü çubuğunda, seçin **Araçları** > **seçenekleri**.

2.  İçinde **seçenekleri** iletişim kutusunda **veritabanı araçları** seçenekleri ve ardından **veri bağlantıları**.

3.  İçinde **SQL Server örneği adı** metin kutusunda, SQL Server Express veya kullanmak istediğiniz LocalDB örneğinin adını belirtin. Adlandırılmış bir örnek değil belirtebilmeniz `.\SQLEXPRESS or (LocalDB)\MSSQLLocalDB`.

4.  **Tamam** düğmesini seçin.

    SQL Server Express, uygulamalarınız için varsayılan veritabanı altyapısı olacaktır.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da verilere erişime](accessing-data-in-visual-studio.md)