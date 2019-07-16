---
title: BoundsRules şekil konumunu ve boyutunu Kısıtlamama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, events
ms.assetid: 4d08e541-fc67-4e68-bf31-30d346aa2aa0
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: d09be82be084767bfb2d300a1877e95456a957b4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68159659"
---
# <a name="boundsrules-constrain-shape-location-and-size"></a>BoundsRules Şekil Konumunu ve Boyutunu Kısıtlamama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

A *sınırları kural* boyut ve konum bir şeklin sınırları tanımlayan bir sınıftır. Bu durumdayken bir kullanıcı bir şekil veya köşeleri veya bir şekil tarafına sürükleyerek tekrar tekrar çağrılan bir yöntem sağlar.  
  
 Aşağıdaki örnek, bir çubuk yatay veya dikey olarak sabit boyutta olacak şekilde bir dikdörtgen kısıtlar. Kullanıcı, kenarlar ve köşeler sürüklediğinde, ana hat iki izin verilen yapılandırma yükseklik ve genişlik çevirir.  
  
 Bir sınıf türetilir sınırları kural <xref:Microsoft.VisualStudio.Modeling.Diagrams.BoundsRules>. Kural örneği şeklinde oluşturulur:  
  
```  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.Modeling.Diagrams.BoundsRules>   
 [Değişikliklere Yanıt Verme ve Değişiklikleri Yayma](../modeling/responding-to-and-propagating-changes.md)
