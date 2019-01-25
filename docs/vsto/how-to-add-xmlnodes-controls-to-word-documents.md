---
title: 'Nasıl yapılır: Word belgelerine XMLNodes denetimleri ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- XMLNodes control, adding to documents
- controls [Office development in Visual Studio], adding to documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 9d754d7be732931cf3d50cf28db396b5040e3874
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54870197"
---
# <a name="how-to-add-xmlnodes-controls-to-word-documents"></a>Nasıl yapılır: Word belgelerine XMLNodes denetimleri ekleme
  **Önemli** Microsoft Word ile ilgili bu konu kümesindeki bilgileri avantajı ve kişiler ve kimin bulunur Amerika Birleşik Devletleri ve kendi bölgeler dışında veya servis kullanan kuruluşlar için özel olarak sunulan veya geliştirme üzerinde çalışan programlar Ocak Microsoft uygulaması belirli işlevlerin ne zaman kaldırıldı 2010'dan önce Microsoft lisanslı Microsoft Word ürünler, Microsoft Word için özel XML ilgili. Bu bilgileri Microsoft Word ile ilgili değil okuma veya kişi ve kuruluşların Amerika Birleşik Devletleri ya da kullanarak veya Microsoft tarafından 10 Ocak 2010'dan sonra lisansına sahip Microsoft Word ürünleri üzerinde çalışan programlar geliştirme alt bölgeleri tarafından kullanılan ; Bu ürünlerin bu tarihten önce lisanslı veya satın alınan ve Amerika Birleşik Devletleri dışında kullanım için lisanslı ürünleri aynı davranmaz.  
  
 [!INCLUDE[appliesto_wdalldoc](../vsto/includes/appliesto-wdalldoc-md.md)]  
  
 Bir Microsoft Office Word belgesi için yinelenen bir XML şemasını eşlediğinizde, Visual Studio otomatik olarak ekler bir <xref:Microsoft.Office.Tools.Word.XMLNodes> belgenize denetimi.  
  
 XML Şeması öğelerini yinelenmeyen eşleme hakkında daha fazla bilgi için bkz: [nasıl yapılır: Word belgelerine XMLNode denetimleri ekleme](../vsto/how-to-add-xmlnode-controls-to-word-documents.md).  
  
> [!NOTE]  
>  <xref:Microsoft.Office.Tools.Word.XMLNodes> Denetim kullanılabilir değil **araç kutusu** veya **veri kaynakları** penceresi ya da can program aracılığıyla oluşturulabilir.  
  
 [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]  
  
### <a name="to-add-an-xmlnodes-control-to-a-document"></a>Belge XMLNodes denetimi eklemek için  
  
1.  Visual Studio tasarımcıda Şerit üzerindeki belgeyi tıklatın **Geliştirici** sekmesi.  
  
    > [!NOTE]  
    >  Varsa **Geliştirici** sekme görünür değilse, önce görünür olmalıdır. Daha fazla bilgi için [nasıl yapılır: Şeritte Geliştirici sekmesini gösterme](../vsto/how-to-show-the-developer-tab-on-the-ribbon.md).  
  
2.  İçinde **XML** grubunda **şema**.  
  
     **Şablonları ve eklentileri** iletişim kutusu açılır.  
  
3.  Tıklayın **XML Şeması** sekmesi.  
  
4.  Tıklayın **şema ekleme**.  
  
     **Şema Ekle** iletişim kutusu açılır.  
  
5.  Yinelenen şeması öğelerini ve tıklatın içeren bir XML Şeması Seç **açık**.  
  
     **Şema ayarları** iletişim kutusu görüntülenir.  
  
6.  Bir ad atayın veya tıklayın **Tamam** şema olmadan bir diğer ad eklemek için.  
  
     Şema eklenir **Şema Ekle** iletişim kutusu.  
  
7.  İçinde **Şema Ekle** iletişim kutusu, tıklayın **Tamam**.  
  
     **XML yapısı** görev bölmesi açılır.  
  
8.  Yinelenen şema öğesine tıklayarak **XML yapısı** belgeye eklemek için görev bölmesi.  
  
     Bir <xref:Microsoft.Office.Tools.Word.XMLNodes> denetim oluşturulur ve projeye eklendi.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [XMLNodes denetimi](../vsto/xmlnodes-control.md)   
 [Genişletilmiş nesneleri kullanarak Word'ü otomatikleştirirken](../vsto/automating-word-by-using-extended-objects.md)   
 [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)   
 [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)  
