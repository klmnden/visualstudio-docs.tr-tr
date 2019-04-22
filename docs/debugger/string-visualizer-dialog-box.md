---
title: Dize Görselleştirici iletişim kutusu | Microsoft Docs
ms.date: 10/10/2018
ms.custom: seoapril2019
ms.topic: reference
f1_keywords:
- vs.debug.stringviewer
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JavaScript
helpviewer_keywords:
- string visualizer
- visualizers, string
ms.assetid: 080fd8f1-72b0-461f-8451-3c84d5dc51df
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 982db296fd17fb86b4a139e02a9418eeb507cd91
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59366789"
---
# <a name="string-visualizer-dialog-box"></a>Dize Görselleştirici iletişim kutusu

Visual Studio'da hata ayıklarken, dizeleri ile yerleşik dize Görselleştirici görüntüleyebilirsiniz. Dize Görselleştirici veri ipucu veya hata ayıklayıcı penceresi için çok uzun dizeler gösterir. Da hatalı biçimlendirilmiş dizeler belirlemenize yardımcı olabilir.

Düz metin, XML, HTML ve JSON yerleşik dize Görselleştirici içerir seçenekleri. Diğer bazı türleri için yerleşik görselleştiriciler gibi açabilirsiniz [DataSet ve DataTable DataView](../debugger/dataset-visualizer-dialog-box.md) nesneleri gelen **Otolar** ya da diğer hata ayıklayıcı pencereleri.

> [!NOTE]
> Görselleştirici XAML ya da WPF kullanıcı Arabirimi öğelerinde denetlemeye ihtiyacınız varsa bkz veya [hata ayıklama sırasında XAML İnceleme özellikleri](../debugger/inspect-xaml-properties-while-debugging.md) veya [WPF ağacı görselleştiricisini kullanma](../debugger/how-to-use-the-wpf-tree-visualizer.md).

Dize Görselleştirici'ni açmak için hata ayıklama sırasında duraklatılmış gerekir. Düz metin, XML, HTML veya dize değeri ve Büyüteç simgesini seçerek JSON sahip bir değişken üzerine geldiğinizde ![VisualizerIcon](../debugger/media/dbg-tips-visualizer-icon.png "Görselleştirici simgesi").

## <a name="uielement-list"></a>UIElement listesi

**İfade** alan değişkenin veya ifadenin üzerine geldiğinizde gösterir.

**Değer** alan dize değerini gösterir. Boş bir **değer** seçilen görselleştiricisi dize tanıyamaz anlamına gelir. Örneğin, **XML Görselleştirici** boş gösterir **değer** bir metin dizesiyle XML etiket yok veya bir JSON dizesi. Seçilen görselleştiricisi tanıyamaz dizeler görüntülemek için seçin **metin görselleştiricisi** yerine. **Metin görselleştiricisi** düz metin gösterir.

### <a name="json-string-data"></a>JSON dizesi verileri

İyi biçimlendirilmiş bir JSON dizesi aşağıdaki çizimde JSON Görselleştirici şunun gibi görünür. Hatalı biçimlendirilmiş JSON, bir hata simgesi (veya tanınmayan ise boş) görüntüleyebilir. JSON hatası tanımlamak için kopyalayın ve dize gibi bir JSON linting aracına yapıştırın [JSLint](https://www.jslint.com/).

![JSON dizesi Görselleştirici](../debugger/media/dbg-tips-string-visualizer-json.png "JSON dize Görselleştirici")

### <a name="xml-string-data"></a>XML dizesi verileri

İyi biçimlendirilmiş bir XML dizesi aşağıdaki çizimde XML Görselleştirici şunun gibi görünür. Hatalı biçimlendirilmiş XML XML etiket veya boş tanınmayan varsa görüntülenebilir.

![XML dizesi Görselleştirici](../debugger/media/dbg-string-visualizers-xml.png "XML dize Görselleştirici")

### <a name="html-string-data"></a>HTML dize verileri

İyi biçimlendirilmiş bir HTML dizesi görünür alacağı bir tarayıcıda aşağıdaki çizimde gösterildiği gibi çizilir. Hatalı biçimlendirilmiş HTML düz metin olarak görüntülenebilir.

![HTML dize Görselleştirici](../debugger/media/dbg-string-visualizers-html.png "HTML dize Görselleştirici")

## <a name="see-also"></a>Ayrıca bkz.

- [Özel görselleştiriciler (C#, Visual Basic) oluşturma](../debugger/create-custom-visualizers-of-data.md)
- [Mac için Visual Studio'da veri görselleştirmeleri](/visualstudio/mac/data-visualizations)