---
title: İş Akışı Tasarımcısı Kabuk Özellikleri
ms.date: 11/04/2016
ms.topic: conceptual
ms.prod: visual-studio-dev15
f1_keywords:
- WFDShellFeatures.UI
ms.assetid: 14bfe312-9592-408e-92ce-e98585ad16e7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 538a9d7b0a895b5cc50c04c107dad55d1c662f3f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54977518"
---
# <a name="workflow-designer-shell-features"></a>İş Akışı Tasarımcısı Kabuk Özellikleri

İş Akışı Tasarımcısı, üç temel kullanıcı Arabirimi alanları oluşur: tasarım yüzeyinde, içerik haritası çubuğu üstünde ve altındaki Kabuk. Ekranın en üstünde konumlandırılmış içerik haritası çubuğu, geçerli bir kök etkinlik öncüleri listesini görüntülemek için kullanılır. Daha fazla bilgi için [nasıl yapılır: İçerik haritası gezintisini kullanma](../workflow-designer/how-to-use-breadcrumb-navigation.md). Tasarımcı yüzeyine konumlandırılmış ekranın merkezinde, iş akışları oluşturmak için kullanılır. Ekranın alt kısmında konumlandırılmış Kabuk geçerli görünümü yönetme düğmelerini içerir.

## <a name="shell-features"></a>Kabuk özellikleri
 Kabuk düğmeleri yakınlaştırma veya uzaklaştırma iş akışınızı, iş akışınızın, ekran boyutuna içindekilere ve Göster veya gizle genel bakış haritasını için kullanabileceğiniz çubuğunun sağ tarafında vardır. İçine veya dışına CTRL ++ ve CTRL + klavye kısayollarını kullanarak iş akışı yakınlaştırma yapabilirsiniz-.

## <a name="overview-map"></a>Genel Bakış haritasını
 Genel Bakış haritasını, tüm alt öğelerini ve tüm genişletilmiş bunların alt öğeleri dahil olmak üzere geçerli içerik haritası kökündeki tüm etkinlik küçük bir sürümünü görüntüler. Görünüm penceresi, şu anda Düzenleyicisi içinde görüntülenen bir etkinlik kısmını vurgular turuncu bir kenarlık ile bir dikdörtgen yoktur. Genel Bakış haritasını çevresinde bir dikdörtgen sürükleyerek iş akışı Tasarımcısı kaydırılır ve düzenleyici görünümünü değiştirir.

> [!NOTE]
> İş Akışı Tasarımcısı kullanıcı arabirimi sanallaştırılır. Etkinlik tasarımcıları, yalnızca gerekli olduğunda işlenir. İş akışının bir kısmını hiçbir zaman Tasarımcı yüzeyinde düzenlendi, söz konusu bölümü genel bakış harita üzerinde beyaz olarak görünür. Genel Bakış haritasını tamamen kaydırma iş akışı çizer.

## <a name="copying-or-saving-workflows-as-images"></a>Kopyalama veya görüntü olarak iş akışları kaydediliyor
 İş akışları, bit eşlem biçiminde kopyalanamaz veya bit eşlem ya da vektör biçiminde kaydedilmiş. Kopyalama veya görüntü kaydetme kökünde tüm alt öğelerini ve tüm genişletilmiş alt öğelerini başka bir programa dahil olmak üzere geçerli içerik haritası, tüm etkinlik görünümünü dışarı aktarmak için bir yol sağlar.

 Görüntü olarak Kopyala için herhangi bir yere Tasarımcısı seçin sağ tıklayıp **görüntü olarak Kopyala**. Görüntü olarak kaydetmek için her yerde Tasarımcısı seçin sağ tıklayın ve **görüntüyü farklı Kaydet**. İş akışları, JPG, GIF, PNG ya da XPS biçiminde kaydedilebilir. Biçimi seçildiğinde **Kaydet** iletişim kutusunda **farklı kaydetme türü:** pencerenin alt kısmındaki liste kutusunda aşağı açılır.

## <a name="fonts-and-colors"></a>Yazı tipleri ve renkler

Visual Studio içinde iş akışı Tasarımcısı'nda kullanılan yazı tiplerini ortam yazı tipi tarafından denetlenir. İşletim sistemi temanızı yüksek karşıtlık renk düzeni kullanıyorsanız, iş akışı Tasarımcısı'nda görüntülenen renklerini değiştirin. İş Akışı Tasarımcısı'nda değişiklikler etkili olmadan önce bir yazı tipi veya renk ayarları değiştirdikten sonra Visual Studio'yu yeniden başlatmanız gerekir.