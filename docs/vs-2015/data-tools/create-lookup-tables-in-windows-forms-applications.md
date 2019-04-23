---
title: Windows Forms uygulamalarında arama tabloları oluşturma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
- aspx
helpviewer_keywords:
- lookup tables
- lookup tables, creating
ms.assetid: 0edd5385-c381-4b17-9096-74e2778db9d5
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 76c55d45e279a3fcf6579c77bf7d226c7baf13d2
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60102984"
---
# <a name="create-lookup-tables-in-windows-forms-applications"></a>Windows Forms uygulamalarında arama tabloları oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Terim *arama tablosu* iki ilgili veri tablolarına bağlı denetimler açıklar. Bu arama denetimleri, ikinci tabloda seçilen bir değere göre ilk tablosundan verileri görüntülemek.  
  
 Arama tabloları üst tablonun ana düğüm sürükleyerek oluşturabilirsiniz (gelen [veri kaynakları penceresi](http://msdn.microsoft.com/library/0d20f699-cc95-45b3-8ecb-c7edf1f67992)) üzerine formunuzdaki ilgili alt tablo sütununda zaten bağlı bir denetim.  
  
 Örneğin, bir tablo düşünün `Orders` satış veritabanındaki. Her kayıtta `Orders` tablo içeren bir `CustomerID`, siparişi hangi müşterinin verdiğini gösteren. `CustomerID` Bir müşteri kaydı işaret eden bir yabancı anahtar `Customers` tablo. Bu senaryoda, genişletme `Orders` tablosundaki **veri kaynakları** penceresi ve ana düğüm kümesine **ayrıntıları**. Ardından `CustomerID` kullanılacak sütunu bir <xref:System.Windows.Forms.ComboBox> (veya arama bağlamayı destekleyen başka bir denetimi) sürükleyin `Orders` formunuza düğümü. Son olarak, sürükleyin `Customers` ilgili sütuna bağlı denetim düğüme — bu durumda, <xref:System.Windows.Forms.ComboBox> bağlı `CustomerID` sütun.  
  
## <a name="to-databind-a-lookup-control"></a>Veri bağlama için bir arama denetimi  
  
1. Açık **veri kaynakları** penceresi.  
  
    > [!NOTE]
    > Arama tabloları gerektiren iki ilişkili tablolar veya nesnelerin kullanılabilir olduğunu **veri kaynakları** penceresi.
  
2. Ait düğümleri genişletebilirsiniz **veri kaynakları** üst tablo ve tüm alt sütunları ve ilgili alt tablo ve sütunları görene kadar penceresi.  
  
    > [!NOTE]
    >  Alt tablo düğümü üst tablo bir Genişletilebilir alt düğüm olarak görünen düğümüdür.  
  
3. Alt tablo için bırakma türünü değiştirme **ayrıntıları** seçerek **ayrıntıları** alt tablonun düğümde denetim listesinden. Daha fazla bilgi için [veri kaynakları penceresinden sürüklendiğinde oluşturulacak denetimi ayarlama](../data-tools/set-the-control-to-be-created-when-dragging-from-the-data-sources-window.md).  
  
4. İki tablo ilişkili düğümü bulun ( `CustomerID` önceki örnekte düğümü). Bırakma türünü değiştirin bir <xref:System.Windows.Forms.ComboBox> seçerek **ComboBox** denetim listesinden.  
  
5. Ana alt tablo düğümünden sürükleyin **veri kaynakları** formunuza penceresi.  
  
     Veriye bağlı denetimler (tanımlayıcı etiketlerle) ve bir aracı (<xref:System.Windows.Forms.BindingNavigator>) formda görünür. A [veri kümesi](../data-tools/dataset-tools-in-visual-studio.md), TableAdapter, <xref:System.Windows.Forms.BindingSource>, ve <xref:System.Windows.Forms.BindingNavigator> bileşen tepsisinde görünür.  
  
6. Artık ana üst tablo düğümden sürükleyin **veri kaynakları** penceresinden doğrudan arama denetimi ( <xref:System.Windows.Forms.ComboBox>).  
  
     Arama bağlamaları artık oluşturulur. Denetimde ayarlanan belirli özellikleri için aşağıdaki tabloya bakın.  
  
    |Özellik|Ayar açıklaması|  
    |--------------|----------------------------|  
    |**Veri kaynağı**|Visual Studio bu özelliği ayarlar <xref:System.Windows.Forms.BindingSource> denetimin sürükleyin tablosu için oluşturulan (başlangıcı yerine sonundan <xref:System.Windows.Forms.BindingSource> denetim oluşturduğunuzda oluşturulan).<br /><br /> Ayarlama yapmanız gerekirse, ardından bunu <xref:System.Windows.Forms.BindingSource> görüntülemek istediğiniz sütun içeren tablo.|  
    |**DisplayMember**|Visual Studio bu özellik, bir dize veri türü denetimi sürükleyin tablosu için birincil anahtar sonra ilk sütuna ayarlar.<br /><br /> Ayarlama yapmanız gerekirse, bu görüntülemek istediğiniz sütun adına ayarlayın.|  
    |**ValueMember**|Visual Studio bu özellik anahtarı yok tanımlanmışsa, birincil anahtarda yer alan ilk sütunun veya tablonun ilk sütunda ayarlar.<br /><br /> Ayarlama yapmanız gerekirse, ardından bu tabloda görüntülemek istediğiniz sütunu ile birincil anahtarı ayarlayın.|  
    |**SelectedValue**|Visual Studio düşürülmüştür özgün sütun için bu özelliği ayarlar **veri kaynakları** penceresi.<br /><br /> Ayarlama yapmanız gerekirse, ardından bunu ilgili tablosundaki yabancı anahtar sütunu ayarlayın.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio'da verilere Windows Forms denetimleri bağlama](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)
