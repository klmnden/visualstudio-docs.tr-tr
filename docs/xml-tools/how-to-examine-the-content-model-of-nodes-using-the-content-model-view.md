---
title: XML şema Tasarımcısı'nda içerik modeli görünümünü kullanarak düğümlerin içerik modelini İnceleme
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c42ddac8-b0e3-48d6-9832-112a19d6c104
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 63e337162dc8499bf9ac2acb5606fbf75292574f
ms.sourcegitcommit: 51dad3e11d7580567673e0d426ab3b0a17584319
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/10/2019
ms.locfileid: "66820453"
---
# <a name="how-to-examine-the-content-model-of-nodes-using-the-content-model-view"></a>Nasıl yapılır: İçerik modeli görünümünü kullanarak düğümlerin içerik modelini İnceleme

Bu konuda düğümlerinizi kullanarak keşfedin açıklar [içerik modeli görünümünü](../xml-tools/content-model-view.md).

## <a name="to-create-a-new-xsd-file-and-display-the-root-element-in-the-content-model-view"></a>Yeni bir XSD dosyası oluşturun ve kök öğe içerik modeli Görünümü'nde görüntülemek için

1. Yeni bir XML şema dosyası oluşturun.

2. Tıklayın **görüntülemek ve temel alınan XML şema dosyası düzenleme için kullanım XML Düzenleyicisi** başlangıç görünümü.

3. XML şema örnek koddan kopyalama [örnek XML şeması: satın alma siparişi şeması](../xml-tools/sample-xsd-file-purchase-order-schema.md) ve varsayılan olarak yeni bir XSD dosyasına eklenen kodu değiştirmek için yapıştırın.

4. Seçin `purchaseOrder` sağ tıklanarak şema Gezgini öğesinde `purchaseOrder` öğesinde XML Düzenleyicisi ve seçerek **XML Gezgini'nde Göster**.

5. Sağ `purchaseOrder` XML Gezgini seçip **içerik modeli görünümünde göster**.

     İçerik modeli görünümünü görüntüler `purchaseOrder` tasarım yüzeyinde öğesi.

6. Genişletin `shipTo`, `billTo`, ve `items` düğümleri her düğümünü çift veya çift her düğümün sağ oka tıklayarak.

     Düğümleri `purchaseOrder` öğesi artık genişletilmiş ve öğenin içerik modeli görebilirsiniz.

7. Tıklayın altında herhangi bir düğümde `purchaseOrder` öğesi ve seçili düğümü şema kümesinde nerede olduğunu görmek için içerik haritası çubuğu bakın.

8. Tıklayın **Göster belgeleri** belgeleri açıp kapatmak için XSD araç çubuğu düğmesi. Ayrıca, belgeleri açıp kapatmak için tasarım yüzeyine sağ tıklayabilirsiniz.

9. Sağ `purchaseOrder` düğümünü seçip alt **örnek XML oluşturmak** XML örneği görmek için.
