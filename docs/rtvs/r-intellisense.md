---
title: R kodu için IntelliSense
description: R kodu yazdığınız sırada visual Studio IntelliSense işlev, nesne üyeleri, kod parçacıkları ve tamamlamalar hakkındaki bilgileri görüntüler.
ms.date: 01/24/2018
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: jillfra
ms.workload:
- data-science
ms.openlocfilehash: 854f7d410e327ca92d0c5156d89bc21765e13cc7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62999047"
---
# <a name="intellisense"></a>IntelliSense

Visual Studio IntelliSense çağırabilirsiniz, işlev nesneleri, işlev bağımsız değişkenleri, üyeleri hakkında daha fazla bilgi görüntüler ve [kod parçacıkları](code-snippets-for-r.md) yazarken görünümünde doğrudan kod yazın. Ayrıca yazarken tamamlanabilir görüntüler ve bastığınızda tamamlandıktan **sekmesini** veya **Enter** anahtarları (bkz [Düzenleyici Seçenekleri](editing-r-code-in-visual-studio.md#editor-options) için **Gelişmiş** sekmesi). Her iki düzenleyicide IntelliSense kullanılabilir ve [etkileşimli pencere](interactive-repl-for-r-in-visual-studio.md).

![İşlev imzası gösteren IntelliSense](media/intellisense-function-signature.png)

Bir işlev veya diğer deyimi yazarken IntelliSense otomatik tamamlama sağlar ne daha önce girdiğiniz tarafından menü (case-sensitively) filtrelenmiştir:

![IntelliSense otomatik tamamlama menüsü](media/intellisense-auto-complete-menu.png)

Tuşuna basarak **sekmesini** (veya **Enter**, veya **alanı**seçenekleri nasıl ayarlanacağını bağlı olarak), açılan menüde seçtiğiniz öğe ekler. Seçimi ok tuşlarını kullanarak değiştirebilirsiniz.

IntelliSense, R nesneleri üyeleri için öneriler de sağlar:

![Nesne üyeleri için IntelliSense önerileri](media/intellisense-auto-complete-r-objects.png)

Tuşuna basarak **ESC** menüsünü tamamen kapatır. Bu ile getirebilir yedekleme **Ctrl**+**alanı**.

Açılış yazarak `(` işlevi için çağrı kapatma ekler `)` ve imza Yardımı ' daha önce gösterildiği gibi getirir:

![Bir işlev için IntelliSense imza Yardımı](media/intellisense-function-signature.png)

Yeniden **ESC** açılır; kapatılana işlev imzası için onu yeniden ile kutusunu görüntüleyebilirsiniz **Ctrl**+**Shift**+**alanı** .

> [!Tip]
> Parametre Yardımı altındaki metin engelliyorsa, basılı **Ctrl** parametre Yardım metni saydam yapmak için anahtar.

## <a name="intellisense-for-user-defined-functions-and-variables"></a>Kullanıcı tanımlı işlevler ve değişkenler için IntelliSense

IntelliSense, parametre adı tamamlama da dahil olmak üzere aynı dosyada, kullanıcı tanımlı işlevler için geçerlidir:

![Kullanıcı tanımlı işlevler için IntelliSense](media/intellisense-same-file-functions.png)

![Kullanıcı tanımlı işlevler için IntelliSense parametresi tamamlama](media/intellisense-parameter-completion.png)

IntelliSense de aynı dosya ve geçerli oturumun değişkenler için geçerlidir:

![IntelliSense değişken tamamlama](media/intellisense-variable-completion.png)

> [!Note]
> Etkileşimli pencerede, IntelliSense geçerli R oturumda yalnızca adları göz önünde bulundurur ve projenizdeki dosyaları yok sayar.

## <a name="code-suggestions"></a>Kod önerileri

(Akıllı etiket olarak adlandırılır) bir ampul kenar boşluğunda göründüğünde, yaygın olarak kullanılan bir eylem için bir kısayol olduğunu Visual Studio önerme. Örneğin, içeren bir çizginin üzerine getirin bir `library` düzenleyicisinde bir ampul görmek için deyimi. Ampul seçme kullanılabilir seçenekleri görüntüler:

![Düzenleyicisi'nde R için akıllı etiketler](media/intellisense-smart-tags.png)
