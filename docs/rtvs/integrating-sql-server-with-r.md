---
title: SQL Server R ile tümleştirme
description: Visual Studio, oluşturma ve R SQL sorguları ve depolanan yordamlarla çalışma R özelliği destekler.
ms.date: 06/25/2018
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: jillfra
ms.workload:
- data-science
ms.openlocfilehash: f15c785658b5c4cd5a6b158b05eb67ff9a4e4c2d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62814445"
---
# <a name="work-with-sql-server-and-r"></a>SQL Server ve R ile çalışma

SQL Server için mükemmel destek Visual Studio'nun veri bilimcileri, R ve SQL veritabanlarını oluşturma ve SQL sorguları çalıştırmak ve depolanan yordamlarla çalışma olanağı ile çalışmak yardımcı olur.

> [!Note]
> SQL ve R ile birlikte çalışmak için SQL Server veri araçları yüklü olması gerekir:
> - Visual Studio 2017: Visual Studio Yükleyicisi'ni çalıştırın ve veri depolama ve SQL Server veri Araçları'nı içeren, işleme iş yükünü seçin.
> - Visual Studio 2015: yönergelerini izleyin [SQL Server veri araçları indirin](https://docs.microsoft.com/sql/ssdt/download-sql-server-data-tools-ssdt).

|   |   |
|---|---|
| ![video kamera simgesini film](../install/media/video-icon.png "bir video izleyin") | [(Youtube.com) videoyu](https://www.youtube.com/watch?v=n4AYr0QIwdQ) SQL Server ve R (3 m 03s) genel bakış. |

## <a name="create-and-run-sql-queries"></a>SQL sorguları oluşturun ve çalıştırın

RTVS, aradığınız sonuçları alana kadar yinelemeli olarak ayrı bir bağlamda SQL sorguları geliştirmenize imkan sağlayan, R projelere ekleme SQL sorgularını destekler.

SQL sorgu dosyası eklemek için projeyi seçin Çözüm Gezgini'nde sağ **Ekle** > **yeni öğe**seçip **SQL sorgusu** dosya türü:

![SQL sorgu öğesi bir projeye ekleyin.](media/sql-add-item.png)

Bu komut dosyasının tam IntelliSense SQL ve sorguları çalıştırma olanağı sağlayan, Visual Studio'nun Transact-SQL Düzenleyicisi'nde açılır. Bir sorgu çalıştırmayı deneyin veya düzenleyici araç çubuğunda Bağlan düğmesini kullanarak bir veritabanına bağlanmak gereken bu özellikleri çalışacak şekilde (**Ctrl**+**Shift**+**E** , ayrıca çalıştığı seçimine göre). Her iki durumda da, bağlantı iletişim kutusunu açar:

![SQL bağlantı iletişim kutusu](media/sql-connection-dialog.png)

Bağlantı kurulduktan sonra sorguları çalıştırmak ve sonuçları bakın:

![SQL penceresinin sorgu sonuçları](media/sql-query-results.png)

Transact-SQL Düzenleyicisi, sorgu ve sorgu hata ayıklayıcı yürütme planı görüntüleme gibi diğer özellikleri çeşitli destekler.
Daha fazla bilgi için [Transact-SQL Düzenleyicisi'ni kullanma düzenleme ve komut dosyaları yürütme](https://msdn.microsoft.com/library/hh272706.aspx).

## <a name="work-with-sql-server-stored-procedures"></a>SQL Server saklı yordamlarla çalışın

[SQL Server R Services](https://docs.microsoft.com/sql/advanced-analytics/r/sql-server-r-services) saklı yordamı ekleyin ve bir T-SQL R kodunu çalıştırın (SQL Server 2016 ve üzeri) sağlar. SQL Server yüklü bir bilgisayara R kodu çalıştırmak, bir SQL sorgusunun döndürdüğü veri çubuğunda çalıştırmak ve daha fazla SQL tarafından işlendiği veya istemciye döndürülen bir SQL sonuç kümesi oluşturur.

Aşağıdaki bölümlerde açıklandığı gibi RTVS tek bir SQL deyimi içinde SQL ve R kodu birleştirme aksi zahmetli ve hatalara işlemini basitleştirir:

- [Veritabanı Bağlantısı Ekle](#add-a-database-connection)
- [Yazın ve bir SQL saklı yordamı test edin](#write-and-test-a-sql-stored-procedure)
- [SQL saklı yordamı yayımlama](#publish-a-sql-stored-procedure)

|   |   |
|---|---|
| ![video kamera simgesini film](../install/media/video-icon.png "bir video izleyin") | [(Youtube.com) videoyu](https://www.youtube.com/watch?v=dFKIT2OitWQ) bakış R ve SQL saklı yordamları (6 milyon 09s) için. |

### <a name="add-a-database-connection"></a>Veritabanı Bağlantısı Ekle

1. Seçin **R Araçları** > **veri** > **veritabanı bağlantı Ekle** ortaya çıkarmak için **bağlantı özellikleri** iletişim kutusu. Burada belirttiğiniz (Bu durumda SQL Server) veri kaynağının adı, sunucu kimlik doğrulama modu ve veritabanının adı adı. Seçin **Test Bağlantısı** iletişim kutusunu kapatmadan önce girişinizi doğrulayın.

    ![SQL bağlantı iletişim kutusu](media/sql-connection-string-dialog.png)

1. Seçtiğinizde **Tamam** geçerli bir bağlantı ile Visual Studio adlı bir bağlantı dizesi oluşturur. `dbConnection` yeni *ayarları. R* dosya. RTVS kaynakları otomatik olarak (çalışır) Bu dosya, R betikleri bağlantısından hemen kullanabilirsiniz:

![SQL Settings.R dosyası](media/sql-settings-dot-r.png)

### <a name="write-and-test-a-sql-stored-procedure"></a>Yazın ve bir SQL saklı yordamı test edin

Yeni bir SQL saklı yordamı eklemek için projenize sağ tıklayın, **Ekle** > **yeni öğe**seçin **SQL saklı yordamı R ile** şablonları listesinden dosyaya bir ad verin ve seçin **Tamam**. Varsayılan dosya adı *SqlSProc.R*; kolay okunması, dosya adı için *StoredProcedure.R* bu bölümün geri kalanında kullanılır. Birden çok saklı yordam varsa, her dosyanın benzersiz bir dosya adı olmalıdır.

Saklı yordam için üç dosyayı RTVS oluşturur: bir *. R* dosya R kodunuz için bir *. Query.SQL* SQL kod dosyası ve bir *. Template.SQL* ikisi bir araya getiren dosya. Bunlar alt öğe olarak iki görünür Çözüm Gezgini'nde ikinci *. R* dosyası:

![Çözüm Gezgini görünümü SQL saklı yordamı R ile genişletilmiş](media/sql-solution-explorer-expanded.png)

*. R* dosyası (*StoredProcedure.R* Bu örnekte) burada, R kod yazdığınız yerdedir. Varsayılan içeriklerini şunlardır:

```R
# @InputDataSet: input data frame, result of SQL query execution
# @OutputDataSet: data frame to pass back to SQL

# Test code
# library(RODBC)
# channel <- odbcDriverConnect(dbConnection)
# InputDataSet <- sqlQuery(channel, )
# odbcClose(channel)

OutputDataSet <- InputDataSet
```

Kısaca, kod olarak adlandırılan bir R dataframe alır `InputDataSet` ve kendi sonuçları `OutputDataSet`, çıkış girişi kopyalamakla şablon kod ile.

> [!Note]
> Bu veri çerçevelerini adlarını denetlediği `@input_data_1_name` ve `@output_data_1_name` parametreleri çağrısında `sp_execute_external_script` sistem saklı yordamı. Bu çağırma kuralı tasarımını hakkında daha fazla ayrıntı ve kullanımı ile ilgili bazı örnekler için bkz: [sp_execute_external_script (Transact-SQL)](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-execute-external-script-transact-sql).

Diğer üretilen kodda (açıklamaları) kullanan bir küçük test betiği sağlar [RODBC paket](https://cran.r-project.org/web/packages/RODBC/index.html) bir SQL deyimi SQL sunucusuna aktarmak için çalıştırın ve almak, sonucu bir R veri çerçevesi ayarlayın. SQL Server'dan alma etkileşimli olarak R kodunuzu sonucu yazmak için bu test kodu ayarlamak açıklama durumundan çıkarabilirsiniz.

*. Query.SQL* dosyası (*StoredProcedure.Query.sql* Bu örnekte), yazma ve test için veri üreten SQL sorgu `InputDataSet`. Bu *.sql* dosya Düzenleyicisi tüm olağan Transact-SQL özellikleri sağlar.

SQL kodunuzla memnun olduğunuzda sürükleyerek, R kodu ile tümleştirmek *.sql* için açık düzenleyiciye dosyasını *. R* dosya. Aşağıdaki görüntüde *StoredProcedure.Query.sql* noktasına sürüklediğiniz *StoredProcedure.R* virgülle sonra `sqlQuery(channel, )`:

![R dize değişkenine SQL dosyası okuma](media/sql-reference-sql-file-from-r.png)

Gördüğünüz gibi bu basit adım R kodunu açmak için otomatik olarak oluşturur. *.sql* dosya içeriğini bir dizeye okumak ve SQL Server için göndermeden RODBC paketini geçirebilirsiniz.

Etkileşimli olarak işleyen kod yazma R artık `InputDataSet` istediğiniz gibi veri çerçevesi. R Kod Düzenleyicisi yalnızca ve göndermeden unutmayın [etkileşimli pencere](interactive-repl-for-r-in-visual-studio.md) tuşuna basarak **Ctrl**+**Enter**.

*. Template.SQL* dosyası (*StoredProcedure.Template.sql* Bu örnekte), son olarak, SQL saklı yordamı oluşturmak için şablon içerir:

```sql
CREATE PROCEDURE [StoredProcedure]
AS
BEGIN
EXEC sp_execute_external_script @language = N'R'
    , @script = N'_RCODE_'
    , @input_data_1 = N'_INPUT_QUERY_'
--- Edit this line to handle the output data frame.
    WITH RESULT SETS (([MYNEWCOLUMN] NVARCHAR(max)));
END;
```

- `_RCODE_` Yer tutucu içeriğine göre değiştirilir *. R* dosya (örneğin, *StoredProcedure.R*).
- `_INPUT_QUERY_` Yer tutucu içeriğine göre değiştirilir *. Query.SQL* dosya (örneğin, *StoredProcedure.Query.sql*).
- Düzen `WITH RESULT SETS` yan tümcesi, sonuç kümesi saklı yordamdan döndürülen şemasını tanımlamak için. Özellikle sütunları belirlemek `OutputDataSet` saklı yordamın çağırana döndürmek istediğiniz veri çerçevesi.

Örneğin, aşağıdaki sorguyu için:

```sql
SELECT TOP 100 medallion, hack_license FROM nyctaxi_sample
```

Aşağıdaki kullanacağınız `WITH RESULT SETS` yan tümcesi dönüş değerlerinin veri türlerini belirtmek için:

```sql
WITH RESULT SETS ((medallion NVARCHAR(max), hack_license NVARCHAR(max)));
```

### <a name="publish-a-sql-stored-procedure"></a>SQL saklı yordamı yayımlama

1. Seçin **R Araçları** > **veri** > **yayımlama seçeneği ile** menü komutu.
1. Görüntülenen iletişim kutusunda, değiştirmek **yayımlama:** için **veritabanı**, hedef belirtin, seçin **Yayımla**, RTVS oluşturur ve saklı yordam yayımlar ve:

    ![Saklı yordam iletişim yayımlama](media/sql-publish-with-options.png)

1. Bir projedeki tüm depolanmış yordamları yayımlamak için kullanabileceğiniz **R Araçları** > **veri** > **saklı yordamları Yayımla** de komutu Çözüm Gezgini'nde projeye sağ tıklayın, kullanılabilir.

> [!Tip]
> SQL Server Nesne Gezgini Visual Studio'da açın varsa, yayımlanan depolanmış yordamınızdaki görünür **programlama** > **saklı yordamlar** veritabanınızın klasör. Ayrıca, nesne Gezgini'nde sağ tıklatıp seçerek çalıştırabileceğiniz **yordamı Yürüt**, veya etkileşimli olarak buradan çağırarak bir *.sql* sorgu penceresi.
