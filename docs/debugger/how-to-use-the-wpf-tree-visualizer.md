---
title: 'Nasıl yapılır: WPF ağacı Görselleştiricisini kullanma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- WPF, debugging
- debugging, WPF
ms.assetid: 2a1bf1cd-90f9-4d06-9fb4-1bfc925afef3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: da18990620644834192c38c24ced9a25ecb56215
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62906115"
---
# <a name="how-to-use-the-wpf-tree-visualizer"></a>Nasıl yapılır: WPF Ağacı Görselleştiricisini kullanma
WPF ağacı görselleştiricisini WPF nesne görsel ağacını keşfedin ve o ağaç içinde bulunan nesneler için WPF bağımlılık özellikleri görüntülemek için kullanabilirsiniz. Görsel ağacı hakkında daha fazla bilgi için bkz: [WPF içinde ağaçlar](/dotnet/framework/wpf/advanced/trees-in-wpf). Bağımlılık özellikleri hakkında daha fazla bilgi için bkz: [bağımlılık özelliklerine genel bakış](/dotnet/framework/wpf/advanced/dependency-properties-overview).

 WPF ağacı görselleştiricisini açtığınızda, iki bölme görürsünüz: **görsel ağacı** soldaki ve **özelliklerini** _adı_**:**  _Tür_ sağ bölmesinde. Herhangi bir nesne seçin **görsel ağacı** bölmesinde ve **özelliklerini** _adı_**:**_türü_ bölmesi Bu nesne özelliklerini göstermek için otomatik olarak güncelleştirilir.

### <a name="to-open-the-wpf-tree-visualizer"></a>WPF ağacı görselleştiricisini açmak için

1. Bir DataTip içinde **Watch** penceresinde **Otolar** penceresinde veya **Yereller** penceresinde, bir WPF nesne adının yanındaki oka bitişik için büyüteç simgesini tıklayın.

     Görselleştiriciler listesi görüntülenir.

2. Tıklayın **WPF ağacı Görselleştiricisini**.

### <a name="to-search-the-visual-tree"></a>Görsel ağacı aramak için

- İçinde **görsel ağacı** bölmesinde, içinde arama yapmak istediğiniz dizeyi yazın **arama** kutusu.

     WPF ağacı görselleştiricisini, yazdığınız dizesiyle eşleşen görsel ağaçta ilk nesnenin hemen bulur. Daha fazla karakter daha doğru bir eşleşme bulmak için yazın.

    - Sonraki eşleşmeye görsel ağacı içinde gitmek için tıklayın **sonraki**.

    - Önceki eşleşmeye geri gitmek için tıklayın **önceki**.

    - Arama ölçütlerini temizlemek için tıklatın **Temizle**.

### <a name="to-search-the-properties-list"></a>Özellikler listesinde aramak için

- İçinde **özelliklerini** _adı_**:**_türü_ bölmesinde, içinde arama yapmak istediğiniz dizeyi yazın **filtre**kutusu.

     WPF ağacı görselleştiricisini hemen yazdığınız dizeyi eşleştir özelliklerini bulur; Artık, listede yalnızca yazdığınız dize eşleşen özellikler görüntülenir. Daha fazla karakter daha doğru bir eşleşme bulmak için yazın.

    - Arama ölçütlerini temizlemek için tıklatın **Temizle**.

### <a name="to-close-the-visualizer"></a>Görselleştirici kapatmak için

- Tıklayın **Kapat** iletişim kutusunun sağ alt köşesindeki simgeyi.

## <a name="see-also"></a>Ayrıca Bkz.
- [Özel Görselleştirici Oluşturma](../debugger/create-custom-visualizers-of-data.md)
- [WPF İçinde Ağaçlar](/dotnet/framework/wpf/advanced/trees-in-wpf)
- [Bağımlılık Özelliklerine Genel Bakış](/dotnet/framework/wpf/advanced/dependency-properties-overview)
