---
title: Program kodundaki katman modellerini gezin ve güncelleştirin | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- layer models, navigating in program code
- layer models, updating in program code
ms.assetid: c60edc87-33ee-4964-a954-40069f9febf3
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: eb0c600830c114ca24f9cdc0619fd84c6e18d232
ms.sourcegitcommit: 2da366ba9ad124366f6502927ecc720985fc2f9e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68871819"
---
# <a name="navigate-and-update-layer-models-in-program-code"></a>Program kodunda katman modellerini gezinme ve güncelleştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu konu başlığı altında, program kodu kullanarak gezinebileceğiniz ve güncelleştirebileceğiniz katman modellerindeki öğeler ve ilişkiler açıklanmıştır. Kullanıcının Görünüm noktasındaki katman diyagramları hakkında daha fazla bilgi için bkz [. katman diyagramları: Başvuru](../modeling/layer-diagrams-reference.md) ve[katman diyagramları: Yönergeler](../modeling/layer-diagrams-guidelines.md).

 Bu konuda açıklanan <xref:Microsoft.VisualStudio.GraphModel> `Microsoft.VisualStudio.ArchitectureTools.Extensibility.Layer` model, daha genel bir modelde bir façlade 'dir. Bir [menü komutu veya hareket uzantısı](../modeling/add-commands-and-gestures-to-layer-diagrams.md)yazıyorsanız, `Layer` modeli kullanın. [Katman doğrulama uzantısı](../modeling/add-custom-architecture-validation-to-layer-diagrams.md)yazıyorsanız, kullanmak `GraphModel`daha kolay olur.

## <a name="transactions"></a>İşlemler
 Bir modeli güncelleştirdiğinizde, içindeki `ILinkedUndoTransaction`değişiklikleri kapsayan göz önünde bulundurun. Bu, değişikliklerinizi tek bir işlem halinde gruplandırır. Değişikliklerden herhangi biri başarısız olursa, tüm işlem geri alınacaktır. Kullanıcı bir değişikliği geri alıyorsa, tüm değişiklikler birlikte geri alınacaktır.

 Daha fazla bilgi için bkz. [işlemleri kullanarak UML model güncelleştirmelerini bağlama](../modeling/link-uml-model-updates-by-using-transactions.md).

```
using (ILinkedUndoTransaction t =
        LinkedUndoContext.BeginTransaction("a name"))
{
    // Make changes here ....
    t.Commit(); // Don't forget this!
}
```

## <a name="containment"></a>Kapsama
 ![ILayer ve ILayerModel, her ikisi de ıkatmanları içerebilir.](../modeling/media/layerapi-containment.png "LayerApi_Containment")

 Katmanlar ([ILayer](/previous-versions/ff644251(v=vs.140))) ve katman modeli ([ILayerModel](/previous-versions/ff643069(v=vs.140))), açıklamalar ve katmanlar içerebilir.

 Bir katman (`ILayer`) bir katman modelinde bulunabilir (`ILayerModel`) veya başka `ILayer`bir içinde iç içe geçmiş olabilir.

 Bir açıklama veya katman oluşturmak için ilgili kapsayıcıda oluşturma yöntemlerini kullanın.

## <a name="dependency-links"></a>Bağımlılık bağlantıları
 Bir bağımlılık bağlantısı bir nesne tarafından temsil edilir. Her iki yönde de gezinilebilir:

 ![ILayerDependencyLink Iki ıkatmanlı bağlar.](../modeling/media/layerapi-dependency.png "LayerApi_Dependency")

 Bir bağımlılık bağlantısı oluşturmak için çağrısı `source.CreateDependencyLink(target)`yapın.

## <a name="comments"></a>Açıklamalar
 Açıklamalar katmanların veya katman modelinin içinde bulunabilir ve ayrıca herhangi bir katman öğesiyle bağlantılı olabilir:

 ![Açıklamalar, herhangi bir katman öğesine iliştirilebilir.](../modeling/media/layerapi-comments.png "LayerApi_Comments")

 Bir yorum, None dahil olmak üzere herhangi bir sayıda öğe ile bağlantılı olabilir.

 Bir katman öğesine iliştirilmiş açıklamaları almak için şunu kullanın:

```csharp
ILayerModel model = diagram.GetLayerModel();
IEnumerable<ILayerComment> comments =
   model.Comments.Where(comment =>
      comment.Links.Any(link => link.Target == layerElement));

```

> [!CAUTION]
> Öğesinin özelliği içinde yer alan açıklamaları alır.`ILayer` `ILayer` `Comments` Onunla bağlantılı olan açıklamaları almaz.

 Uygun kapsayıcıyı çağırarak `CreateComment()` bir yorum oluşturun.

 Açıklamasında kullanarak `CreateLink()` bir bağlantı oluşturun.

## <a name="layer-elements"></a>Katman öğeleri
 Bir modelde yer alan tüm öğe türleri katman öğeleridir:

 ![Katman diyagramı Içerikleri ılayerelements.](../modeling/media/layerapi-layerelements.png "LayerApi_LayerElements")

## <a name="properties"></a>Özellikler
 Her `ILayerElement` birinin adlı `Properties`bir dize sözlüğü vardır. Bu sözlüğü, herhangi bir katman öğesine rastgele bilgi eklemek için kullanabilirsiniz.

## <a name="artifact-references"></a>Yapıt başvuruları
 Yapıt başvurusu ([ILayerArtifactReference](/previous-versions/ff644536(v=vs.140))), bir katman ve dosya, sınıf veya klasör gibi bir proje öğesi arasındaki bağlantıyı temsil eder. Kullanıcı bir katman oluştururken veya Çözüm Gezgini, Sınıf Görünümü veya Nesne Tarayıcısı öğeleri bir katman diyagramına sürükleyerek yapılar oluşturur. Herhangi bir sayıda yapıt başvurusu bir katmana bağlanabilir.

 Katman Gezgini 'ndeki her satır bir yapıt başvurusu görüntüler. Daha fazla bilgi için, bkz. [kodunuzda katman diyagramları oluşturma](../modeling/create-layer-diagrams-from-your-code.md).

 Yapıt başvurularıyla ilgilenen asıl türler ve yöntemler aşağıdaki gibidir:

 [ILayerArtifactReference](/previous-versions/ff644536(v=vs.140)). Categories özelliği, bir sınıf, yürütülebilir dosya veya derleme gibi ne tür bir yapıya başvurulduğunu gösterir. Kategoriler, tanımlayıcının hedef yapıtı nasıl tanımladığını belirler.

 [ArtifactReferenceExtensions. CreateArtifactReferenceAsync](/previous-versions/ff695840(v=vs.140)) bir <xref:EnvDTE.Project> veya <xref:EnvDTE.ProjectItem>' den bir yapıt başvurusu oluşturur. Bu zaman uyumsuz bir işlemdir. Bu nedenle, genellikle oluşturma işlemi tamamlandığında çağrılan bir geri çağırma sağlarsınız.

 Katman yapıt başvuruları, kullanım örneği diyagramlarında yapıtlarla karıştırılmamalıdır.

## <a name="shapes-and-diagrams"></a>Şekiller ve diyagramlar
 İki nesne bir katman modelinde her öğeyi temsil etmek için kullanılır: `ILayerElement`a ve bir [ıvpe](/previous-versions/ee806673(v=vs.140)). , `IShape` Diyagramdaki şeklin konumunu ve boyutunu temsil eder. Katman modellerinde, `ILayerElement` her biri `IShape`içerir ve her `IShape` bir katman diyagramında bir tane `ILayerElement`bulunur. `IShape`UML modelleri için de kullanılır. Bu nedenle, her `IShape` bir katman öğesi yoktur.

 Aynı şekilde `ILayerModel` , tek bir [IDiagram](/previous-versions/ee789658(v=vs.140))üzerinde görüntülenir.

 Özel bir komut veya hareket işleyicisi kodunda, `DiagramContext` içeri aktarma işleminden geçerli diyagramı ve geçerli şekillerin seçimini alabilirsiniz:

```
public class ... {
[Import]
    public IDiagramContext DiagramContext { get; set; }
...
public void ... (...)
{ IDiagram diagram = this.DiagramContext.CurrentDiagram;
  ILayerModel model = diagram.GetLayerModel();
  if (model != null)
  { foreach (ILayer layer in model.Layers) { ... }}
  foreach (IShape selected in diagram.SelectedShapes)
  { ILayerElement element = selected.GetLayerElement();
    if (element != null) ... }}
```

 ![Her ILayerElement bir IShape tarafından sunulur.](../modeling/media/layerapi-shapes.png)

 [IShapes](/previous-versions/ee806673(v=vs.140)) ve [ıDIAGRAM](/previous-versions/ee789658(v=vs.140)) , UML modellerini göstermek için de kullanılır. Daha fazla bilgi için bkz. [DIYAGRAMLARDA UML modeli görüntüleme](../modeling/display-a-uml-model-on-diagrams.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Katman diyagramlarına komut ve hareket ekleme](../modeling/add-commands-and-gestures-to-layer-diagrams.md)
- [Katman diyagramlarına özel mimari doğrulaması ekleme](../modeling/add-custom-architecture-validation-to-layer-diagrams.md)
- [Katman diyagramlarına özel özellikler ekleme](../modeling/add-custom-properties-to-layer-diagrams.md)
- [Katman Diyagramları: Başvuru](../modeling/layer-diagrams-reference.md)
- [Katman Diyagramları: Yönergeler](../modeling/layer-diagrams-guidelines.md)
- [UML modellerini ve diyagramları genişletme](../modeling/extend-uml-models-and-diagrams.md)
