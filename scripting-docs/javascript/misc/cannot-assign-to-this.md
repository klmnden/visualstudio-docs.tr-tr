---
title: "'This' nesnesine atanamaz | Microsoft Docs"
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5000
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: ba2b0a2b-f0f8-4698-b335-a4ab6c166671
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4a4ba5d852a7d131a88930dd66931c026074549b
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58149503"
---
# <a name="cannot-assign-to-this"></a>'this' nesnesine atanamaz
Bir değer atayın çalışıldı **bu**. **Bu** olduğu bir [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] anahtar sözcüğü ya da ifade eder:

- bir yöntem yürütülmekte nesnesi

- Genel nesne geçerli bir yöntem (veya başka bir nesneye yöntemi ait değil ise).

Bir yöntem bir [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] nesneyle çağrılan işlev. Bir yöntem içinde **bu** anahtar sözcüğü yöntemi aracılığıyla çağrıldığı nesneye bir başvurudur (ile sınıfın Oluşturucusu çağrılarak oluşturulan nesne olmasını olur **yeni** işleci).

Bir yöntem içinde kullanabilirsiniz **bu** geçerli nesne, ancak sizin için yeni bir değere atanamaz **bu**.

## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

- Atama çalışmayın **bu**. Bir özellik veya yöntem örneklenmiş bir nesnenin erişmek için nokta işlecini kullanın (örneğin, **circle.radius**).

  > [!NOTE]
  > Örneğin bir kullanıcı tarafından oluşturulan değişken adı **bu**; bu bir [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] ayrılmış sözcük.

## <a name="see-also"></a>Ayrıca Bkz.

- [this Deyimi](../../javascript/reference/this-statement-javascript.md)
- [Komut Dosyalarınızda Sorun Giderme](../../javascript/advanced/troubleshooting-your-scripts-javascript.md)