---
title: 'Nasıl yapılır: Bir özelliği yerelleştirme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- features [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, localizing
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 26eb3a1352228d48fb451e3a3520162cdea18b73
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54867383"
---
# <a name="how-to-localize-a-feature"></a>Nasıl yapılır: Bir özelliği yerelleştirme
  Varsayılan olarak, sabit kodlanmış dize değerleri özellik başlıkları ve açıklamaları kullanın. Özellik başlığı ve açıklamayı yerelleştirmek için dizeleri yerelleştirilmiş kaynaklara başvuran deyimleri ile değiştirin.  
  
## <a name="localize-a-feature"></a>Bir özelliği yerelleştirme  
  
#### <a name="to-localize-a-feature"></a>Bir özelliği yerelleştirmek için  
  
1.  İçinde **Çözüm Gezgini**, kısayol menüsünü açın **özellik1** düğümünü seçip **özellik kaynağı Ekle**.  
  
2.  İçinde **kaynak Ekle** iletişim kutusunda **sabit dil** varsayılan dil özelliği kaynak dosyanın kültürüyle listeden.  
  
3.  Diller için yerelleştirilmiş özelliği, tercih ettiğiniz kaynak dosyaları seçerek yerelleştirilen her dil için önceki adımı yineleyin.  
  
     Ayrı bir özellik kaynak dosyaları oluşturulur: varsayılan dil için bir tane ve her bir yerelleştirilmiş desteklemek istediğiniz dili.  
  
4.  Her kaynak dosyası kaynak düzenleyicisinde açın ve tüm dize kimliklerini ve bunların değerlerini girin.  
  
     Örneğin, varsayılan özellik kaynak dosyası, bir dize kimliği girin **başlık** değeriyle **My özellik başlığı**, ve ikinci bir dize kimliği **açıklama** değerine sahip **My özellik açıklaması**. Her bir yerelleştirilmiş kaynak dosyası için aynı dize kimliklerini varsayılan özellik kaynak kullanılan kullanın, ancak yerelleştirilmiş dizeleri için değerleri girin.  
  
5.  Tüm kaynak değerleri girdikten sonra bu özellik için kısayol menüsünü açın (örneğin, *Feature1.feature*) ve ardından **Görünüm Tasarımcısı** özelliğini özellik Tasarımcısı'nda açmak için.  
  
6.  Yerelleştirmek için **başlık** ve **açıklama** özellik alanlarında kendi kutularında değerleri girmek için aşağıdaki biçimi kullanın:  
  
     `$Resources:` *Dize kimliği*  
  
     $Resources girin:**başlık** içinde **özellik başlığı** kutusu ve $Resources:**açıklama** içinde **özellik açıklaması** kutusu .  
  
     Dize kimliklerini kaynak dosyalarında kullanılan eşleşmelidir.  
  
7.  Seçin **F5** anahtarı oluşturun ve uygulamayı çalıştırın.  
  
8.  SharePoint'te açın **Site eylemleri** menüsünde seçin **Site Ayarları**ve ardından **Site eylemleri** bölümü seçin **Site özellikleriyönetme** bağlantı.  
  
9. SharePoint'te, varsayılan görüntüleme dilini değiştirin.  
  
     Yerelleştirilmiş özellik başlığı ve açıklamayı uygulamada görüntülenir. Yerelleştirilmiş kaynakları görüntülemek için SharePoint server kaynak dosyanın kültürüyle eşleşen bir dil paketi yüklü olmalıdır.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint Çözümlerini Yerelleştirme](../sharepoint/localizing-sharepoint-solutions.md)   
 [Nasıl yapılır: Kaynak dosyası ekleme](../sharepoint/how-to-add-a-resource-file.md)   
 [Nasıl yapılır: ASPX işaretlemesini yerelleştirme](../sharepoint/how-to-localize-aspx-markup.md)   
 [Nasıl yapılır: Kod yerelleştirme](../sharepoint/how-to-localize-code.md)  
