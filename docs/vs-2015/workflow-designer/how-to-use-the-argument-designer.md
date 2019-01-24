---
title: 'Nasıl yapılır: Bağımsız değişken Tasarımcısını kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Presentation.View.ArgumentDesigner.UI
- System.Activities.Presentation.View.DesignTimeArgument.UI
ms.assetid: 64813fd5-1ea1-499a-98b4-ab2a44b7ee5e
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 9844745951be9c29bc9dd624db47991ab2437692
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54790462"
---
# <a name="how-to-use-the-argument-designer"></a>Nasıl yapılır: Bağımsız Değişken Tasarımcısını Kullanma
Önceki sürümlere göre [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)], bağımsız değişken tasarımcısını veri ekleme çıkarma bir etkinlik akışı izin vermek kolaylaştırır. Tasarımcı tıklayarak erişilen **bağımsız değişkenleri** tasarım tuvalin sol alt köşesindeki düğme. Tasarımcı, bir tablo biçiminde görünür ve her bir sütun üst bilgileri dışında sıralanabilir bağımsız değişkenlerinin listesi içeren **varsayılan değer** sütun. Her bağımsız değişken adı, / out/içinde-out/özellik yönü, türü ve varsayılan ifade değeri (varsa) içerir. Adı ve varsayılan ifade değeri düzenlenebilir metin alanları ve türü ve Yön açılan listeler. [!INCLUDE[crabout](../includes/crabout-md.md)] bağımsız değişkenleri, görmek [değişkenleri ve bağımsız değişkenler](http://msdn.microsoft.com/library/d03dbe34-5b2e-4f21-8b57-693ee49611b8).  
  
### <a name="to-create-a-new-argument"></a>Yeni bir değişken oluşturmak için  
  
1.  İş akışı veya etkinliği bir çözüm açın [!INCLUDE[vs2010](../includes/vs2010-md.md)].  
  
2.  Bağımsız değişkenler Tasarımcısı'nı tıklatarak **bağımsız değişkenleri** tasarım tuvalin sol alt köşesindeki düğme. Bağımsız değişken tasarımcısını görünür.  
  
3.  Etiketli boş satırı tıklatın **bağımsız değişken oluşturma**. Bu aşağıdaki varsayılan değerleri kullanarak yeni bir değişken ile yeni bir satır ekler: argumentx için **adı** x benzersiz bağımsız değişken adları oluşturmak için otomatik olarak artırılır 1 başlangıç değeri bir tamsayı olduğu **içinde**  için **yönü**, ve **dize** için **bağımsız değişken türü**. Hiçbir değer için eklenen **varsayılan değer**. İş akışı tasarım işlemi sırasında herhangi bir zamanda bu değerleri değiştirebilirsiniz.  
  
    > [!NOTE]
    >  Bir değişkeni silmek için bağımsız değişken tıklayarak seçin ve tuşuna **Sil** anahtarı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş akışı Tasarımcısını kullanma](../workflow-designer/using-the-workflow-designer.md)   
 [Değişkenler ve Bağımsız Değişkenler](http://msdn.microsoft.com/library/d03dbe34-5b2e-4f21-8b57-693ee49611b8)