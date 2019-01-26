---
title: BoundsRules Şekil Konumunu ve Boyutunu Kısıtlamama
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, events
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: 8c6ab2a25838935ff0c0b7dcc860fa9196504974
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54986234"
---
# <a name="boundsrules-constrain-shape-location-and-size"></a>BoundsRules Şekil Konumunu ve Boyutunu Kısıtlamama

A *sınırları kural* boyut ve konum bir şeklin sınırları tanımlayan bir sınıftır. Bu durumdayken bir kullanıcı bir şekil veya köşeleri veya bir şekil tarafına sürükleyerek tekrar tekrar çağrılan bir yöntem sağlar.

Aşağıdaki örnek, bir çubuk yatay veya dikey olarak sabit boyutta olacak şekilde bir dikdörtgen kısıtlar. Kullanıcı, kenarlar ve köşeler sürüklediğinde, ana hat iki izin verilen yapılandırma yükseklik ve genişlik çevirir.

Bir sınıf türetilir sınırları kural <xref:Microsoft.VisualStudio.Modeling.Diagrams.BoundsRules>. Kural örneği şeklinde oluşturulur:

```csharp
using Microsoft.VisualStudio.Modeling.Diagrams; ...

public partial class BarShape
{
  /// <summary>
  /// Rule invoked when the user is resizing a shape.
  /// </summary>
  public override BoundsRules BoundsRules
  { get { return new BarBoundsRule(); } }
}

/// <summary>
/// Rule invoked when the user is changing a shape's outline.
/// Provides real-time mouse rubber-band feedback, so must work fast.
/// </summary>
public class BarBoundsRule: BoundsRules
{
  public override RectangleD GetCompliantBounds
     (ShapeElement shape, RectangleD proposedBounds)
  {
    double thickness = 0.1;
    if (proposedBounds.Height > proposedBounds.Width)
    {
      // There is a minimum width for a shape; the width
      // will actually be set to the lesser of
      // thickness and that minimum.
      return new RectangleD(proposedBounds.Location,
            new SizeD(thickness, proposedBounds.Height));
    }
    else
    {
      // There is a minimum height for a shape; the
      // height will actually be set to the lesser of
      // thickness and that minimum.
      return new RectangleD(proposedBounds.Location,
         new SizeD(proposedBounds.Width, thickness));
} } }
```

İsterseniz konum ve boyut kısıtlanabilir dikkat edin.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualStudio.Modeling.Diagrams.BoundsRules>
- [Değişiklikleri Yanıtlama ve Yayma](../modeling/responding-to-and-propagating-changes.md)