---
title: 'Nasıl yapılır: Şemaları Visual Studio içindeki Word belgeleriyle eşleştirme'
titleSuffix: ''
ms.custom: seodec18
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- XML schemas [Office development in Visual Studio], mapping
- mappings [Office development in Visual Studio], XML schemas to Word documents
- Word [Office development in Visual Studio], mapping XML schemas
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 4c6f9ee9a7b636c6c12bfe2f8debcc05911e3b04
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63441763"
---
# <a name="how-to-map-schemas-to-word-documents-inside-visual-studio"></a>Nasıl yapılır: Şemaları Visual Studio içindeki Word belgeleriyle eşleştirme
  **Önemli** Microsoft Word ile ilgili bu konu kümesindeki bilgileri avantajı ve kişiler ve kimin bulunur Amerika Birleşik Devletleri ve kendi bölgeler dışında veya servis kullanan kuruluşlar için özel olarak sunulan veya geliştirme üzerinde çalışan programlar Ocak Microsoft uygulaması belirli işlevlerin ne zaman kaldırıldı 2010'dan önce Microsoft lisanslı Microsoft Word ürünler, Microsoft Word için özel XML ilgili. Bu bilgileri Microsoft Word ile ilgili değil okuma veya kişi ve kuruluşların Amerika Birleşik Devletleri ya da kullanarak veya Microsoft tarafından 10 Ocak 2010'dan sonra lisansına sahip Microsoft Word ürünleri üzerinde çalışan programlar geliştirme alt bölgeleri tarafından kullanılan ; Bu ürünlerin bu tarihten önce lisanslı veya satın alınan ve Amerika Birleşik Devletleri dışında kullanım için lisanslı ürünleri aynı davranmaz.

 [!INCLUDE[appliesto_wdalldoc](../vsto/includes/appliesto-wdalldoc-md.md)]

 Belge, Visual Studio'da açıkken bir XML Şeması belge eşleyebilirsiniz. Visual Studio'nun dışında belge açıldığında kullandığınız aynı Microsoft Office Word araçları kullanırsınız. Office proje önce belgeye şema eşleştirdiğinizde veya Word çözümünüzü oluşturduktan sonra aynı nesneleri oluşturur.

## <a name="to-map-an-xml-schema-to-a-word-document-in-visual-studio"></a>Visual Studio'da bir Word belgesi bir XML Şeması eşlemek için

1. Visual Studio içindeki Word belgesi veya şablonu projesi açın.

2. Belgenin tasarımcıya odağı taşımak için tıklayın.

3. Şerit üzerinde tıklayın **Geliştirici** sekmesi.

    > [!NOTE]
    > Varsa **Geliştirici** sekme görünür değilse, önce görünür olmalıdır. Daha fazla bilgi için [nasıl yapılır: Şeritte Geliştirici sekmesini gösterme](../vsto/how-to-show-the-developer-tab-on-the-ribbon.md).

4. İçinde **XML** grubunda **şema**.

     **Şablonları ve eklentileri** iletişim kutusu açılır.

5. Tıklayın **XML Şeması** sekmesi.

6. Tıklayın **şema ekleme**.

     **Şema Ekle** iletişim kutusu açılır.

7. Şema dosyasına göz atın, onu seçin ve ardından **açık**.

     **Şema ayarları** iletişim kutusu açılır.

8. Bir ad atayın veya tıklayın **Tamam** şema olmadan bir diğer ad eklemek için.

9. **Tamam**'ı tıklatın.

     **XML yapısı** penceresi açılır.

10. Öğeleri sürükleme **XML yapısı** belgenizi oluşturulacak ilgili denetimlerin, istediğiniz yerde penceresine.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Şemaları Visual Studio içindeki çalışma sayfalarıyla eşleştirme](../vsto/how-to-map-schemas-to-worksheets-inside-visual-studio.md)
- [XML şemaları ve belge düzeyi özelleştirmelerdeki veriler](../vsto/xml-schemas-and-data-in-document-level-customizations.md)
