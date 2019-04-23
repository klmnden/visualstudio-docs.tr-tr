---
title: 'Nasıl yapılır: İçerik modeli görünümünü kullanarak düğümlerin içerik modelini İnceleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: c42ddac8-b0e3-48d6-9832-112a19d6c104
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 24ceb80c0ffd03e7c796b7a5d5abdc93f4c1c78d
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60099071"
---
# <a name="how-to-examine-the-content-model-of-nodes-using-the-content-model-view"></a>Nasıl yapılır: İçerik Modeli Görünümünü Kullanarak Düğümlerin İçerik Modelini İnceleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu konuda düğümlerinizi kullanarak keşfedin açıklar [içerik modeli görünümünü](../xml-tools/content-model-view.md).  
  
### <a name="to-create-a-new-xsd-file-and-display-the-root-element-in-the-content-model-view"></a>Yeni bir XSD dosyası oluşturun ve kök öğe içerik modeli Görünümü'nde görüntülemek için  
  
1. Yeni bir XML şema dosyası oluşturun.  
  
2. Tıklayın **görüntülemek ve temel alınan XML şema dosyasını düzenlemek için XML Düzenleyicisi'ni kullanma** başlangıç görünümü.  
  
3. XML şema örnek koddan kopyalama [örnek XML şeması: Satınalma siparişi şeması](../xml-tools/sample-xsd-file-purchase-order-schema.md) ve varsayılan olarak yeni bir XSD dosyasına eklenen kodu değiştirmek için yapıştırın.  
  
4. Seçin `purchaseOrder` sağ tıklanarak şema Gezgini öğesinde `purchaseOrder` öğesi XML Düzenleyicisi'ni seçerek **XML Gezgini'nde Göster**.  
  
5. Sağ `purchaseOrder` XML Gezgini seçip **içerik modeli görünümünde göster**.  
  
     İçerik modeli görünümünü görüntüler `purchaseOrder` tasarım yüzeyinde öğesi.  
  
6. Genişletin `shipTo`, `billTo`, ve `items` düğümleri her düğümünü çift veya çift her düğümün sağ oka tıklayarak.  
  
     Düğümleri `purchaseOrder` öğesi artık genişletilmiş ve öğenin içerik modeli görebilirsiniz.  
  
7. Tıklayın altında herhangi bir düğümde `purchaseOrder` öğesi ve seçili düğümü şema kümesinde nerede olduğunu görmek için içerik haritası çubuğu bakın.  
  
8. Tıklayın **Göster belgeleri** platformlarının geçiş yapmak için XSD araç çubuğu düğmesi. Ayrıca, belgeleri açıp kapatmak için tasarım yüzeyine sağ tıklayabilirsiniz.  
  
9. Rick tıklamayla `purchaseOrder` düğümünü seçip alt **örnek XML oluşturmak** XML örneği görmek için.
