---
title: Geliştirme sırasında sisteminizi doğrulama
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- dependency diagrams
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ce0822f5731e7c09a6f6dff9116e70b97a529206
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62907153"
---
# <a name="validate-your-system-during-development"></a>Geliştirme sırasında sisteminizi doğrulama
Visual Studio, yazılım sisteminizin mimarisi ve kullanıcı gereksinimleri ile tutarlı korunmasına yardımcı olabilirsiniz.

 Bu özelliklerin her biri Visual Studio'nun hangi sürümlerinin desteklediği için bkz [mimari ve Modelleme Araçları sürüm desteği](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport).

## <a name="key-tasks"></a>Anahtar görevler
 Sisteminizi doğrulamak için aşağıdaki görevleri kullanın.

|**Görevler**|**İlişkili konular**|
|-|-|
|**Yazılım kullanıcıların gereksinimleri karşıladığından emin olun**:<br /><br /> Sisteminiz ve bileşenlerinin testleri düzenlemenize yardımcı olması için gereksinimleri ve mimari modelleri kullanabilirsiniz. Bu uygulama, kullanıcıların ve diğer proje katılımcıları için önemli olan gereksinimleri test etmek ve gereklilikler değiştiğinde testleri hızlı bir şekilde güncelleştirmenize yardımcı emin olun yardımcı olur.|-   [Model aracılığıyla test geliştirme](../modeling/develop-tests-from-a-model.md)|
|**Yazılım sisteminizin hedeflenen tasarım ile tutarlı kalmasından emin olun:**<br /><br /> Bağımlılık diyagramları uygulamanızın bileşenleri arasında istenen bağımlılıkları açıklar. Geliştirme sırasında gerçek kod bağımlılıkları hedeflenen tasarım ile uyumlu olduğunu doğrulayabilirsiniz.|-   [Kodunuz aracılığıyla bağımlılık diyagramları oluşturma](../modeling/create-layer-diagrams-from-your-code.md)<br />-   [Bağımlılık diyagramları ile kod doğrulama](../modeling/validate-code-with-layer-diagrams.md)|

## <a name="external-resources"></a>Dış Kaynaklar

|**Kategori**|**Bağlantılar**|
|-|-|
|**Videolar**|![video bağlantı](../data-tools/media/playvideo.gif) [Channel 9: Doug yedi: Kod anlama ve Visual Studio 2010 ile sistem tasarımı](http://go.microsoft.com/fwlink/?LinkId=216100)<br /><br /> ![video bağlantı](../data-tools/media/playvideo.gif) [Channel 9: Bir bağımlılık diyagramı kullanarak uygulama mimarileri oluşturma](http://go.microsoft.com/fwlink/?LinkID=201117)<br /><br /> ![video bağlantı](../data-tools/media/playvideo.gif) [MSDN nasıl yaparım serisi: Bağımlılık diyagramları kullanarak kod doğrulama](http://go.microsoft.com/fwlink/?LinkID=214405)|
|**Forumları**|-   [Visual Studio Görselleştirme ve Modelleme Araçları](http://go.microsoft.com/fwlink/?LinkId=184720)<br />-   [Visual Studio Görselleştirme ve modelleme SDK'sını (DSL araçları)](http://go.microsoft.com/fwlink/?LinkId=184721)|
|**Bloglar**|-   [Microsoft DevOps](https://devblogs.microsoft.com/devops/)|
|**Teknik makaleler ve belgeler**|[MSDN Mimari Merkezi](http://go.microsoft.com/fwlink/?LinkId=201343)|

## <a name="see-also"></a>Ayrıca bkz.

- [Uygulamayı test etme](/azure/devops/test/overview?view=vsts)
- [Kullanıcı gereksinimlerini modelleme](../modeling/model-user-requirements.md)
- [Mimariyi Çözümleme ve Mimarinin Modelini Oluşturma](../modeling/analyze-and-model-your-architecture.md)

[!INCLUDE[modeling_sdk_info](includes/modeling_sdk_info.md)]
