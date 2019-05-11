---
title: Lambda ifadesi veya blok gövdesi kullanma
ms.date: 02/14/2019
ms.topic: reference
author: kendrahavens
ms.author: kehavens
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 5c46506e81e5334efea9060e957269e92e9d49cc
ms.sourcegitcommit: 614d5b99576ea27a41957cd94062dc95cbd29c1c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2019
ms.locfileid: "65531910"
---
# <a name="use-expression-body-or-block-body-for-lambda-expressions"></a>Lambda ifadeleri için ifade gövdesi veya blok gövdesi kullan

Bu yeniden düzenleme için geçerlidir:

- C#

**Ne:** Bir lambda ifadesi bir deyim gövdesinin veya blok gövdesi kullanacak şekilde yeniden düzenleme sağlar.

**ne zaman:** Tercih ettiğiniz bir lambda ifadeleri ifade gövdesi ya da bir blok gövdesi kullan.

**Neden:** Lambda ifadeleri, kullanıcı tercihinize göre okunabilirliği artırmak için yeniden.

## <a name="lambda-expression-body-or-block-body-refactoring"></a>Lambda ifadesi gövdesinin veya blok gövdesini yeniden düzenleme

1. İmlecinizi bir lambda işlecinin sağ tarafta yerleştirin.
2. Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

  ![Lambda ifadesi/blok gövdesi kullan](media/block-body-lambda.png)

3. Seçin **lambda ifadeleri için blok gövdesi kullan** veya **lambda ifadeleri için ifade gövdesi kullan**.

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [.NET Geliştiricileri için İpuçları](../csharp-developer-productivity.md)