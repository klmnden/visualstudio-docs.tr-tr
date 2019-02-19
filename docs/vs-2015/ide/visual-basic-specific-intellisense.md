---
title: Visual Basic'e özel IntelliSense | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- IntelliSense [Visual Basic]
- IntelliSense [Visual Studio], Visual Basic
ms.assetid: 4dec8753-05e5-4f74-b304-5f8c4ed8723b
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: ce0d1f2fd5c4ea8549f638f97846fdf7a1726b90
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54796899"
---
# <a name="visual-basic-specific-intellisense"></a>Visual Basic'e Özel IntelliSense
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Basic kaynak kod Düzenleyicisi, IntelliSense aşağıdaki özellikleri sunar:  
  
-   Söz dizimi ipuçları  
  
     Söz dizimi ipuçları, yazmakta olduğunuz deyimi sözdizimi görüntüler. Bu gibi deyimleri için kullanışlıdır [Declare](http://msdn.microsoft.com/library/d3f21fb0-b804-4c99-97ed-583b23894cf1).  
  
## <a name="automatic-completion"></a>Otomatik Tamamlama  
  
- Çeşitli anahtar sözcüklere tamamlama  
  
   Örneğin, `goto` ve boşluk, IntelliSense, açılan menüde tanımlanan Etiketler listesi görüntülenir. Desteklenen diğer anahtar sözcükler içerir `Exit`, `Implements`, `Option`, ve `Declare`.  
  
- Tamamlanma `Enum` ve `Boolean`  
  
   Bir ifade bir sabit listesi üyesi için başvuracaktır, IntelliSense üyelerinin bir listesini görüntüler `Enum`. Ne zaman bir deyim başvurduğu bir `Boolean`, IntelliSense doğru yanlış açılan menü görüntüler.  
  
  Tamamlama kapatılabilir varsayılan seçimini kaldırarak **otomatik üyeleri Listele** gelen **genel** özellik sayfasında **Visual Basic** klasör.  
  
  Tamamlanma listesi üyeleri, tam sözcük veya ALT + sağ ok çağırarak el ile çağırabilirsiniz. Daha fazla bilgi için [IntelliSense kullanarak](../ide/using-intellisense.md).  
  
## <a name="intellisense-in-zone"></a>Bölgedeki IntelliSense  
 IntelliSense bölgesinde üzerinden dağıtmak için gereken Visual Basic geliştiriciler yönetmenize yardımcı olan [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] ve kısmi güven ayarlarına göre kısıtlanır. Bu özellik:  
  
- Uygulamanın birlikte çalışacağı izinleri seçmenize olanak tanır.  
  
- Seçilen görüntü API'leri, listesi üyeleri olarak kullanılabilir bölge ve gerektiren ek izinler olarak kullanılamayan API'leri görüntülemek.  
  
  Daha fazla bilgi için [ClickOnce uygulamaları için kod erişimi güvenliği](../deployment/code-access-security-for-clickonce-applications.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IntelliSense Kullanma](../ide/using-intellisense.md)
