---
title: Office çözümlerine genel bakış yerel veritabanı dosyaları kullanma
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office applications [Office development in Visual Studio], data
- data [Office development in Visual Studio], local
- local data [Office development in Visual Studio]
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 527b2e2561b89dc38e56c0d9d854034a791edf19
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53939206"
---
# <a name="use-local-database-files-in-office-solutions-overview"></a>Office çözümlerine genel bakış yerel veritabanı dosyaları kullanma
  SQL Server Express gibi bir veritabanı dosyası içerebilir (*.mdf*) dosya veya bir Microsoft Office Access (*.mdb*) dosyasında Office çözümünüzü. Bu, son kullanıcıların merkezi bir veritabanındaki bakım çözümünde yalnızca tek bir bilgisayarda kullanılan örneğin yerel Envanter gerekli olduğu durumlarda yerel bir veritabanı bakımı olanak tanır.  
  
 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]  
  
## <a name="import-the-database-file-into-a-project"></a>Veritabanı dosyası bir projeye içeri aktarma  
 Veritabanı dosyasını projenize aktarmak için kullanın **veri kaynağı Yapılandırma Sihirbazı** veritabanı dosyasını temel alan bir veri kaynağını oluşturmak için. Sihirbaz projenize veritabanı dosyası ve bir türü belirtilmiş veri kümesi ekler.  
  
## <a name="deploy-the-database-file"></a>Veritabanı dosyasını dağıtma  
 **Veri kaynağı Yapılandırma Sihirbazı** yerel veritabanı dosyasındaki bağlantılar oluşturmak için göreli bir yol kullanır. Bu dosyalar göreli konumlarını korur çözüm bir bilgisayardan diğerine kopyalamak sağlar.  
  
 Bir sunucuya çözümünüzü dağıtın ve ardından her son kullanıcıya belgeyi dağıtın, gerekir el ile de veritabanı dosyası dağıtmak ve belge göre aynı konumda yükleyin. Veritabanı dosyası isterse de taşınır sürece bu, son kullanıcı kendi bilgisayarda yeni bir konuma belge taşınamıyor anlamına gelir.  
  
## <a name="local-database-files-and-caching-the-dataset"></a>Yerel veritabanı dosyaları ve veri kümesi önbelleğe alma  
 Microsoft Office Excel ve Microsoft Office Word için belge düzeyi çözümlerde, belge kümelerinde veri kümesi örneği öznitelik ile işaretleyerek önbelleğe alabilir <xref:Microsoft.VisualStudio.Tools.Applications.Runtime.CachedAttribute>. Eklediğinizde, veritabanı dosyasını projenize kullanarak **veri kaynağı Yapılandırma Sihirbazı**, yazılan veri kümesi projenize otomatik olarak eklenir. Uygulanacak nadiren gereklidir <xref:Microsoft.VisualStudio.Tools.Applications.Runtime.CachedAttribute> bu veri kümesine veri kullanıcının bilgisayarında yerel olduğundan. Daha fazla bilgi için [veriyi önbelleğe alma](../vsto/caching-data.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Office çözümlerinde denetimlere veri bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)   
 [Nasıl yapılır: Belgeleri veritabanı verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-a-database.md)   
 [Nasıl yapılır: Bir konak kontrolü verileriyle veri kaynağını güncelleme](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md)   
 [Office çözümünü dağıtma](../vsto/deploying-an-office-solution.md)   
 [Verileri önbelleğe](../vsto/caching-data.md)  
