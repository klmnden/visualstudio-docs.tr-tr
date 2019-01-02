---
title: 'Nasıl Yapılır: Word belgelerine XMLNode denetimleri ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- XMLNode control, adding to documents
- controls [Office development in Visual Studio], adding to documents
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: e0b3f4970dd1699efe000a67970f03629bef48a8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53838917"
---
# <a name="how-to-add-xmlnode-controls-to-word-documents"></a>Nasıl Yapılır: Word belgelerine XMLNode denetimleri ekleme
  **Önemli** Microsoft Word ile ilgili bu konu kümesindeki bilgileri avantajı ve kişiler ve kimin bulunur Amerika Birleşik Devletleri ve kendi bölgeler dışında veya servis kullanan kuruluşlar için özel olarak sunulan veya geliştirme üzerinde çalışan programlar Ocak Microsoft uygulaması belirli işlevlerin ne zaman kaldırıldı 2010'dan önce Microsoft lisanslı Microsoft Word ürünler, Microsoft Word için özel XML ilgili. Bu bilgileri Microsoft Word ile ilgili değil okuma veya kişi ve kuruluşların Amerika Birleşik Devletleri ya da kullanarak veya Microsoft tarafından 10 Ocak 2010'dan sonra lisansına sahip Microsoft Word ürünleri üzerinde çalışan programlar geliştirme alt bölgeleri tarafından kullanılan ; Bu ürünlerin bu tarihten önce lisanslı veya satın alınan ve Amerika Birleşik Devletleri dışında kullanım için lisanslı ürünleri aynı davranmaz.  
  
 [!INCLUDE[appliesto_wdalldoc](../vsto/includes/appliesto-wdalldoc-md.md)]  
  
 Bir Microsoft Office Word belgesi için yinelenmeyen bir XML şemasını eşlediğinizde, Visual Studio otomatik olarak ekler bir <xref:Microsoft.Office.Tools.Word.XMLNode> belgenize denetimi. Yinelenen XML Şeması öğelerini eşleme hakkında daha fazla bilgi için bkz: [nasıl yapılır: Word belgelerine XMLNodes denetimleri ekleme](../vsto/how-to-add-xmlnodes-controls-to-word-documents.md).  
  
> [!NOTE]  
>  <xref:Microsoft.Office.Tools.Word.XMLNode> Denetim kullanılabilir değil **araç kutusu** veya **veri kaynakları** penceresi ve programlı olarak oluşturulamıyor.  
  
 [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]  
  
### <a name="to-add-an-xmlnode-control-to-a-document"></a>XMLNode denetimi bir belgeye eklemek için  
  
1.  Visual Studio tasarımcıda Şerit üzerindeki belgeyi tıklatın **Geliştirici** sekmesi.  
  
    > [!NOTE]  
    >  Varsa **Geliştirici** sekme görünür değilse, önce görünür olmalıdır. Daha fazla bilgi için [nasıl yapılır: Şeritte Geliştirici sekmesini gösterme](../vsto/how-to-show-the-developer-tab-on-the-ribbon.md).  
  
2.  İçinde **XML** grubunda **şema**.  
  
     **Şablonları ve eklentileri** iletişim kutusu açılır.  
  
3.  Tıklayın **XML Şeması** sekmesi.  
  
4.  Tıklayın **şema ekleme**.  
  
     **Şema Ekle** iletişim kutusu açılır.  
  
5.  Yinelenmeyen şema öğeleri içeren bir XML Şeması Seç **Şema Ekle** iletişim kutusu ve tıklatın **açık**.  
  
     **Şema ayarları** iletişim kutusu görüntülenir.  
  
6.  Bir ad atayın veya tıklayın **Tamam** şema olmadan bir diğer ad eklemek için.  
  
     Şema eklenir **Şema Ekle** iletişim kutusu.  
  
7.  İçinde **Şema Ekle** iletişim kutusu, tıklayın **Tamam**.  
  
8.  **XML yapısı** görev bölmesi açılır.  
  
9. Yinelenmeyen bir şema öğesine tıklayarak **XML yapısı** belgeye eklemek için görev bölmesi.  
  
     Bir <xref:Microsoft.Office.Tools.Word.XMLNode> denetim oluşturulur ve projeye eklendi.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [XMLNode denetimi](../vsto/xmlnode-control.md)   
 [Genişletilmiş nesneleri kullanarak Word'ü otomatikleştirirken](../vsto/automating-word-by-using-extended-objects.md)   
 [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)   
 [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)  
