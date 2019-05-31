---
title: 'XML şema Tasarımcısı: Graf görünümünü kullanarak şema kümesine genel bakış elde edin'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c0df4b0d-52ef-4a6c-9676-1d8311aad7c7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e0a0fc62a0d6dfe772a550f33cafa02bc5bc1bf3
ms.sourcegitcommit: ba5e072c9fedeff625a1332f22dcf3644d019f51
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/31/2019
ms.locfileid: "66432167"
---
# <a name="how-to-get-an-overview-of-a-schema-set-using-the-graph-view"></a>Nasıl yapılır: Graf görünümünü kullanarak şema genel bakış

Bu konu nasıl kullanılacağını açıklar [graf görünümünü](../xml-tools/graph-view.md) düğümlerin ve düğümler arasındaki ilişkileri şema kümesi üst düzey bir görünümünü görmek için.

## <a name="to-create-a-new-xsd-file-and-display-the-root-element-in-the-content-model-view"></a>Yeni bir XSD dosyası oluşturun ve kök öğe içerik modeli Görünümü'nde görüntülemek için

1. Yeni bir XML şema dosyası oluşturma ve dosyayı farklı Kaydet *Relationships.xsd*.

2. Tıklayın **görüntülemek ve temel alınan XML şema dosyası düzenleme için kullanım XML Düzenleyicisi** başlangıç görünümünde bağlantı.

3. XML şema örnek koddan kopyalama [örnek XML şeması: ilişkileri](../xml-tools/sample-xsd-file-relationships.md) ve varsayılan olarak yeni bir XSD dosyasına eklenen kodu değiştirmek için yapıştırın.

4. XML Düzenleyicisi'nde herhangi bir yere sağ tıklayıp **Görünüm Tasarımcısı**.

5. Graf görünümünden seçim **XSD araç**.

6. Seçin **şeması Ayarla** düğümünde **XML Şeması Gezgini** ve düğümü graf görünümünü tasarım yüzeyine sürükleyin. Tüm genel düğümleri ve ilişkileri düğümlerini bağlayan oklar görmeniz gerekir.

     ![Graf Görünümü](../xml-tools/media/relationshipingraphview.gif)

7. Tasarım yüzeyinde herhangi bir düğümde tıklayın ve şema kümesindeki Seçili düğümün nerede bulunduğunu görmek için içerik haritası çubuğu bakın.

8. Tasarım yüzeyi ve select herhangi bir öğe düğümü Rick tıklayın **örnek XML oluşturmak** XML örneği görmek için.