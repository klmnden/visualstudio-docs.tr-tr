---
title: 'Nasıl Yapılır: Görünümler ile XML Düzenleyicisi Arasında Geçiş Yapma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: cb69fbbd-d99c-439e-9498-5df9050f8df0
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 09ad752dc87ea322396d6e6513593d71a7554b98
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53936249"
---
# <a name="how-to-switch-between-views-and-the-xml-editor"></a>Nasıl Yapılır: Görünümler ile XML Düzenleyicisi arasında geçiş yapın

Bu konuda, XML şema Tasarımcısı (XSD Tasarımcısı) görünümler ile XML Düzenleyicisi arasında geçiş yapma gösterilmektedir. Bu örnekte [satınalma siparişi şeması](../xml-tools/sample-xsd-file-simple-schema.md).

## <a name="to-switch-between-the-views-and-the-xml-editor"></a>Görünümler ile XML Düzenleyicisi arasında geçiş yapmak için

1.  Yeni bir XML şema dosyası oluşturma ve düzenleme için adımları [nasıl yapılır: Bir XSD şema dosyası oluşturma ve düzenleme](../xml-tools/how-to-create-and-edit-an-xsd-schema-file.md).

2.  İçin XML şema tasarımcısını XML düzenleyicisinden geçiş yapmak için herhangi bir XML Düzenleyicisi'nde sağ tıklayıp **Görünüm Tasarımcısı**.

3.  Filigran kullanarak grafik görünümüne geçmek için tıklatın **düğümler arasındaki ilişkiyi görmek için graf görünümünü kullanın** başlangıç görünümünde bağlantı.

4.  Sürükle `USAddress` düğümünden **XML Şeması Gezgini** graf görünümünü sürükleyin. Sağ `USAddress` graf görünümünden ve select düğümünde **içerik modeli görünümünde göster** bağlam menüsünde.

     İçerik modeli görünümünü ayrıntılarıyla `USAddress` düğümü görüntülenir.

5.  Araç çubuğunu kullanarak içerik modeli görünümünden başlatmak görünümüne geçmek için tıklatın **başlangıç görünümündeki** XSD araç çubuğu düğmesi.

6.  Kısayol tuşlarını kullanarak görünümler arasında geçiş yapmak için basın **Ctrl**+**1** başlangıç görünümü **Ctrl**+**2** graf görünümü ve **Ctrl**+**3** içerik modeli görünümünden için.

7.  İçerik modeli görünümünden XML Düzenleyicisi'ne gitmek için düğümünü sağ tıklatın ve seçin **kodu görüntüle** bağlam menüsünde.