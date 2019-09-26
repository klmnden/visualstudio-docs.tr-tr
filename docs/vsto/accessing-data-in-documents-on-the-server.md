---
title: Sunucudaki belgelerdeki verilere erişin
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- data [Office development in Visual Studio], accessing on server
- data access [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ab033120c0913bbae33458c5a2d0b53972364581
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255776"
---
# <a name="access-data-in-documents-on-the-server"></a>Sunucudaki belgelerdeki verilere erişin
  Microsoft Office Word veya Microsoft Office Excel 'in nesne modelini kullanmak zorunda kalmadan belge düzeyi özelleştirmesindeki verilere karşı programlama yapabilirsiniz. Bu, Word veya Excel yüklü olmayan bir sunucuda bulunan bir belgede bulunan verilere erişebileceğiniz anlamına gelir. Örneğin, bir sunucudaki kod (örneğin, bir [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] sayfada) bir belgedeki verileri özelleştirebilir ve özelleştirilmiş belgeyi bir son kullanıcıya gönderebilir. Son Kullanıcı belgeyi açtığında, çözüm derlemesinde veri bağlama kodu özelleştirilmiş verileri belgeye bağlar. Belgedeki veriler kullanıcı arabiriminden ayrıldığından bu mümkündür. Daha fazla bilgi için bkz. [belge düzeyi özelleştirmelerde önbelleğe alınmış veriler](../vsto/cached-data-in-document-level-customizations.md).

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

## <a name="cache-data-for-use-on-a-server"></a>Sunucuda kullanılmak üzere verileri önbelleğe alma
 Belgedeki bir veri nesnesini önbelleğe almak için, tasarım zamanında <xref:Microsoft.VisualStudio.Tools.Applications.Runtime.CachedAttribute> özniteliği ile işaretleyin veya çalışma zamanında bir konak öğesinin `StartCaching` yöntemini kullanın. Belgedeki bir veri nesnesini önbelleğe aldığınızda, nesneyi belgede depolanan bir [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] xml dizesine dizileştirir. Nesnelerin önbelleğe almak için uygun gereksinimleri karşılaması gerekir. Daha fazla bilgi için bkz. [önbelleği verileri](../vsto/caching-data.md).

 Sunucu tarafı kod, veri önbelleğindeki tüm veri nesnelerini işleyebilir. Önbelleğe alınmış veri örneklerine bağlı denetimler Kullanıcı arabirimiyle eşitlenir, böylece verilerde yapılan tüm sunucu tarafı değişiklikleri, belge istemcide açıldığında otomatik olarak görünür.

## <a name="access-data-in-the-cache"></a>Önbellekteki verilere erişin
 Önbellekteki verilere, örneğin bir konsol uygulamasından, bir Windows Forms uygulamadan veya bir Web sayfasından, Office dışındaki uygulamalardan erişebilirsiniz. Önbelleğe alınmış verilere erişen uygulamanın tam güven olması gerekir; kısmi güvene sahip bir Web uygulaması, bir Office belgesinde önbelleğe alınmış verileri ekleyemez, alamaz veya değiştiremezler.

 Veri önbelleğine, <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.CachedData%2A> <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> sınıfının özelliği tarafından açığa çıkarılan koleksiyonlar hiyerarşisi aracılığıyla erişilebilir:

- Özelliği, belge düzeyi <xref:Microsoft.VisualStudio.Tools.Applications.CachedData>özelleştirmesindeki tüm önbelleğe alınmış verileri içeren bir döndürür. <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.CachedData%2A>

- Her <xref:Microsoft.VisualStudio.Tools.Applications.CachedData> biri bir veya daha <xref:Microsoft.VisualStudio.Tools.Applications.CachedDataHostItem> fazla nesne içerir. , Tek bir sınıfta tanımlanan önbelleğe alınmış veri nesnelerinin tümünü içerir.<xref:Microsoft.VisualStudio.Tools.Applications.CachedDataHostItem>

- Her <xref:Microsoft.VisualStudio.Tools.Applications.CachedDataHostItem> biri bir veya daha <xref:Microsoft.VisualStudio.Tools.Applications.CachedDataItem> fazla nesne içerir. Tek bir önbelleğe alınmış veri nesnesini temsileder.<xref:Microsoft.VisualStudio.Tools.Applications.CachedDataItem>

  Aşağıdaki kod örneğinde, bir Excel çalışma kitabı projesinin `Sheet1` sınıfında önbelleğe alınmış bir dizeye nasıl erişebileceğiniz gösterilmektedir. Bu örnek, <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.Save%2A> yöntemi için sağlanmış daha büyük bir örneğin bir parçasıdır.

  [!code-csharp[Trin_ServerDocument#12](../vsto/codesnippet/CSharp/Trin_ServerDocument/Form1.cs#12)]
  [!code-vb[Trin_ServerDocument#12](../vsto/codesnippet/VisualBasic/Trin_ServerDocument/Form1.vb#12)]

## <a name="modify-data-in-the-cache"></a>Önbellekteki verileri değiştirme
 Önbelleğe alınmış bir veri nesnesini değiştirmek için genellikle aşağıdaki adımları gerçekleştirirsiniz:

1. Önbelleğe alınmış nesnenin XML gösterimini nesnenin yeni bir örneğine serisini kaldırma. XML 'e, önbelleğe alınmış veri nesnesini temsil <xref:Microsoft.VisualStudio.Tools.Applications.CachedDataItem.Xml%2A> <xref:Microsoft.VisualStudio.Tools.Applications.CachedDataItem> eden öğesinin özelliğini kullanarak erişebilirsiniz.

2. Bu kopyada değişiklikleri yapın.

3. Değiştirilen nesneyi, aşağıdaki seçeneklerden birini kullanarak veri önbelleğine geri doğru bir şekilde seri hale getirme:

    - Değişiklikleri otomatik olarak seri hale getirmek istiyorsanız <xref:Microsoft.VisualStudio.Tools.Applications.CachedDataItem.SerializeDataInstance%2A> yöntemini kullanın. Bu yöntem veri önbelleğinde seri hale <xref:System.Data.DataSet>getirmek, <xref:System.Data.DataTable>ve türü belirtilmiş veri kümesi nesneleri için DiffGram biçimini kullanır. **DiffGram** biçimi çevrimdışı bir belgedeki veri önbelleğinde yapılan değişikliklerin sunucuya doğru şekilde gönderilmesini sağlar.

    - Önbelleğe alınan verilerde yapılan değişiklikler için kendi serileştirme işlemini gerçekleştirmek istiyorsanız, doğrudan <xref:Microsoft.VisualStudio.Tools.Applications.CachedDataItem.Xml%2A> özelliğine yazabilirsiniz. Bir veritabanını <xref:System.Data.Common.DataAdapter> <xref:System.Data.DataSet>, ,<xref:System.Data.DataTable>veya türü belirtilmiş veri kümesindeki verilerde yapılan değişikliklerle güncelleştirmek için kullanıyorsanız, DiffGram biçimini belirtin. <xref:System.Data.Common.DataAdapter> Aksi takdirde, mevcut satırları değiştirmek yerine yeni satırlar ekleyerek veritabanını güncelleştirir.

### <a name="modify-data-without-deserializing-the-current-value"></a>Geçerli değerin serisini kaldırmadan verileri Değiştir
 Bazı durumlarda, önbelleğe alınmış nesnenin değerini, önce geçerli değeri seri durumdan kaldırmadan değiştirmek isteyebilirsiniz. Örneğin, bir dize veya tamsayı gibi basit bir türe sahip bir nesnenin değerini değiştiriyorsanız veya bir sunucuda önbelleğe alınmış <xref:System.Data.DataSet> bir belgeyi başlatırken bunu yapabilirsiniz. Bu durumlarda, önce önbelleğe alınmış nesnenin geçerli <xref:Microsoft.VisualStudio.Tools.Applications.CachedDataItem.SerializeDataInstance%2A> değerini seri durumdan çıkarmak zorunda kalmadan yöntemini kullanabilirsiniz.

 Aşağıdaki kod örneğinde, bir Excel çalışma kitabı projesinin `Sheet1` sınıfında önbelleğe alınmış bir dizenin değerinin nasıl değiştirileceği gösterilmektedir. Bu örnek, <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.Save%2A> yöntemi için sağlanmış daha büyük bir örneğin bir parçasıdır.

 [!code-csharp[Trin_ServerDocument#11](../vsto/codesnippet/CSharp/Trin_ServerDocument/Form1.cs#11)]
 [!code-vb[Trin_ServerDocument#11](../vsto/codesnippet/VisualBasic/Trin_ServerDocument/Form1.vb#11)]

### <a name="modify-null-values-in-the-data-cache"></a>Veri önbelleğindeki null değerleri Değiştir
 Veri önbelleği, belge kaydedilip kapatıldığında **null** değeri olan nesneleri depolamaz. Önbelleğe alınmış verileri değiştirirken bu sınırlamanın çeşitli sonuçları vardır:

- Veri önbelleğindeki herhangi bir nesneyi **null**değerine ayarlarsanız, belge açıldığında veri önbelleğindeki tüm nesneler otomatik olarak **null** olarak ayarlanır ve belge kaydedilip kapatıldığında tüm veri önbelleğinin temizlenmesi gerekir. Diğer bir deyişle, önbelleğe alınmış tüm nesneler veri önbelleğinden kaldırılır ve <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.CachedData%2A> koleksiyon boş olur.

- Veri önbelleğinde **null** nesnelerle bir çözüm oluşturursanız ve belge ilk kez açılmadan önce <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> sınıfını kullanarak bu nesneleri başlatmak istiyorsanız, veri önbelleğindeki tüm nesneleri başlattığınızdan emin olmanız gerekir. Nesneleri yalnızca bir kısmını başlattığınızda, belge açıldığında tüm nesneler **null** olarak ayarlanır ve belge kaydedilip kapatıldığında tüm veri önbelleğinin temizlenmesi gerekir.

## <a name="access-typed-datasets-in-the-cache"></a>Önbellekte yazılan veri kümelerine erişme
 Yazılı bir veri kümesindeki verilere hem Office çözümünden hem de Office dışındaki bir uygulamadan (Windows Forms uygulaması veya bir [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] proje gibi) erişmek istiyorsanız, yazılan veri kümesini her ikisi de başvurulan ayrı bir derlemede tanımlamanız gerekir projeyle. **Veri kaynağı yapılandırma** Sihirbazı 'nı veya **veri kümesi Tasarımcısı**kullanarak her bir projeye türü belirtilmiş veri kümesini eklerseniz, .NET Framework iki projedeki türü belirtilmiş veri kümelerini farklı türler olarak değerlendirir. Türü belirtilmiş veri kümeleri oluşturma hakkında daha fazla bilgi için bkz. [Visual Studio 'da veri kümeleri oluşturma ve yapılandırma](../data-tools/create-and-configure-datasets-in-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Sunucudaki belgelerdeki verilere erişin](../vsto/accessing-data-in-documents-on-the-server.md)
- [Belge düzeyi Özelleştirmelerdeki önbelleğe alınmış veriler](../vsto/cached-data-in-document-level-customizations.md)