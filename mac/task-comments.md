---
title: Görev Açıklamaları
description: Kodunuza Görev açıklamalarını ekleme
author: cobey
ms.author: cobey
ms.date: 05/06/2018
ms.assetid: 562DCB46-D8FA-4DC4-AAEA-F274448C4CD2
ms.openlocfilehash: d88b74ab953f97e061f4be3befc227646006f38b
ms.sourcegitcommit: 7fbfb2a1d43ce72545096c635df2b04496b0be71
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/09/2019
ms.locfileid: "67692318"
---
# <a name="task-comments"></a>Görev Açıklamaları

Kod yazarken, tamamlanmamış veya şüpheli kod veya uyarılar ile Hızlı çözümler açıkça açıklama standart bir uygulamadır. Mac için Visual Studio tarafından sağlanan varsayılan sinyal TODO, HACK, FIXME ve UNDONE belirteçleridir. Kişiselleştirilmiş belirteçleri altında tanımlanabilir **Visual Studio > Tercihler > ortam > görevleri**aşağıdaki görüntüde gösterildiği gibi:

![Görev listesi tercihleri](media/source-editor-image10.png)

Yeni görev açıklama eklemek için görev anahtar sözcüğü içeren bir açıklama ekleyin. Örneğin:

```csharp
//TODO: Finish this for all properties.
```

Mac için Visual Studio bunları vurgulayarak bu işaretleyicileri dikkat çizer **görev listesi** giderek görüntülenebilen paneli **Görüntüle > doldurmalar > görev**:

![Görev listesi paneli](media/source-editor-image11.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Görev listesi (Windows için Visual Studio) kullanın](/visualstudio/ide/using-the-task-list)