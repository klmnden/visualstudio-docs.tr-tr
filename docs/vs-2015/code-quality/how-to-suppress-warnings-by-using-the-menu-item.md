---
title: 'Nasıl yapılır: Menü öğesini kullanarak uyarıları bastırma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
helpviewer_keywords:
- warnings, suppressing
- code analysis, suppressing warnings
ms.assetid: 36bd1850-dcde-4ed0-9bc3-0b83df434362
caps.latest.revision: 26
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: a8fbc314580b106f5e1e8dae5a0a78d043d3940b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60080910"
---
# <a name="how-to-suppress-warnings-by-using-the-menu-item"></a>Nasıl yapılır: Menü Öğesini Kullanarak Uyarıları Bastırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[NOT]
>  Kaynak gizleme web sitesi projeleri için desteklenmiyor.  
  
 Kod çözümleme uyarılarını bastırma için Kod Analizi penceresi kullanabilirsiniz. Uyarı gizleme devre dışı bırakmasını ile aynı değil. Bir uyarıyı bastırmak ihlalinin yalnızca belirli bir örneği için uygulanır. Aynı uyarı diğer ihlalleri yine de hata Listesi penceresinde bildirilir.  
  
 Kod Analizi çalıştırdıktan sonra bir veya daha fazla kod Analizi penceresi içinde görüntülenen kod çözümleme uyarıları, uygulamanız için geçerli olmadığını belirlemek. Örneğin, kodun doğru olduğunu belirlemek. Veya bazı ihlalleri düşük öncelikli ve mevcut geliştirme döngüsü içinde sabit olmayan bir durum olabilir. Bunun nedeni ne olursa olsun, uyarı kodunu gözden geçirildi ve bu uyarı bastırılabilir belirlendi takım üyelerinizin izin vermek için geçerli olduğunu belirtmek çoğunlukla yararlı olur. Bu, uyarının oluşturulduğu yakın bir gizleme yerleştirmenizi sağlar çünkü kaynakta gizleme yararlı olur.  
  
 Kaynak kodu veya küresel bir gizleme dosyasında gizleme görüntülenip görüntülenmeyeceğini seçebilirsiniz. Genel gizleme dosyasında bazı gizlemeleri yerleştirilmelidir. Bu durum söz konusuysa **içinde kaynak** seçeneği devre dışı bırakılacak.  
  
### <a name="to-suppress-a-warning-by-using-menu-item"></a>Menü öğesini kullanarak bir uyarıyı bastırmak için  
  
1. Üzerinde **Çözümle** menüsünde seçin **Windows** seçip **Kod Analizi**.  
  
2. İçinde **Kod Analizi** penceresinde, uyarı bastır seçin.  
  
3. Eylem seçin ve ardından **iletileri gösterme**seçin **içinde kaynak** veya **proje gizleme dosyası**.  
  
     Özel uyarı bastırılır ve üzeri Kod Analizi penceresi bir uyarı görüntülenir.  
  
> [!NOTE]
>  Bir hedef olmayan gizlemeleri küresel bir gizleme dosyasında görünür.
