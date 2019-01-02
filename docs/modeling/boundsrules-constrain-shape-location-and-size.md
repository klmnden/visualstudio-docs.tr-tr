---
title: BoundsRules Şekil Konumunu ve Boyutunu Kısıtlamama
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, events
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: 449fb0c12b11163ba0ceca981e66a7da0c399e1c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53950205"
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