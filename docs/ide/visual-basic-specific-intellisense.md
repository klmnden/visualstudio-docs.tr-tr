---
title: Visual Basic IntelliSense
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.Basic.IntelliSense
helpviewer_keywords:
- IntelliSense [Visual Basic]
- IntelliSense [Visual Studio], Visual Basic
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: dc0897f3b2964996b18a40cc8dda16068ff772f2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62582517"
---
# <a name="intellisense-for-visual-basic-code-files"></a>Visual Basic kod dosyaları için IntelliSense

Visual Basic kaynak kod Düzenleyicisi, IntelliSense aşağıdaki özellikleri sunar:

## <a name="syntax-tips"></a>Söz dizimi ipuçları

Söz dizimi ipuçları, yazmakta olduğunuz deyimi sözdizimi görüntüler. Bu gibi deyimleri için kullanışlıdır [Declare](/dotnet/visual-basic/language-reference/statements/declare-statement).

## <a name="automatic-completion"></a>Otomatik Tamamlama

- Çeşitli anahtar sözcüklere tamamlama

     Örneğin, `goto` ve bir boşluk, IntelliSense, açılan menüde tanımlanan etiketler listesini görüntüler. Desteklenen diğer anahtar sözcükler içerir `Exit`, `Implements`, `Option`, ve `Declare`.

- Tamamlanma `Enum` ve `Boolean`

    Bir ifade bir sabit listesi üyesi için başvuracaktır, IntelliSense, üyelerinin listesini görüntüler. `Enum`. Ne zaman bir deyim başvurduğu bir `Boolean`, IntelliSense doğru yanlış açılan menü görüntüler.

Tamamlama kapatılabilir varsayılan seçimini kaldırarak **otomatik üyeleri Listele** gelen **genel** özellik sayfasında **Visual Basic** klasör.

Üyeleri listeleme, tam sözcük çağırarak tamamlama el ile çağırabilirsiniz veya **Alt**+**sağ ok**. Daha fazla bilgi için [kullanım IntelliSense](../ide/using-intellisense.md).

## <a name="intellisense-in-zone"></a>Bölgedeki IntelliSense

IntelliSense bölgesinde üzerinden dağıtmak için gereken Visual Basic geliştiriciler yönetmenize yardımcı olan [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] ve kısmi güven ayarlarına göre kısıtlanır. Bu özellik:

- Uygulamanın birlikte çalışacağı izinleri seçmenize olanak tanır.

- Seçilen görüntü API'leri, listesi üyeleri olarak kullanılabilir bölge ve gerektiren ek izinler olarak kullanılamayan API'leri görüntülemek.

Daha fazla bilgi için [ClickOnce uygulamaları için kod erişimi güvenliği](../deployment/code-access-security-for-clickonce-applications.md).

## <a name="filtered-completion-lists"></a>Filtrelenmiş tamamlanma listeleri

Visual Basic IntelliSense tamamlanma listelerinde listelerin altına bulunan iki sekme denetimleri sahip. **Ortak** varsayılan olarak seçilir, sekme, yazmakta olduğunuz deyimi tamamlamak için en sık kullanılan öğeleri görüntüler. **Tüm** sekmesi de açık olanlar dahil olmak üzere otomatik tamamlama için kullanılabilir olan tüm öğeleri görüntüler **ortak** sekmesi.

## <a name="see-also"></a>Ayrıca bkz.

- [IntelliSense kullanma](../ide/using-intellisense.md)