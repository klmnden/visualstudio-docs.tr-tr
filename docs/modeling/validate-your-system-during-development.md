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
ms.openlocfilehash: 9fb9810f1c212dfb881f5725676a79c6307b9cfa
ms.sourcegitcommit: 6a19c5ece38a70731496a38f2ef20676ff18f8a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65476502"
---
# <a name="validate-your-system-during-development"></a>Geliştirme sırasında sisteminizi doğrulama

Visual Studio, yazılım sisteminizin mimarisi ve kullanıcı gereksinimleri ile tutarlı korunmasına yardımcı olabilirsiniz.

Bu özelliklerin her biri Visual Studio'nun hangi sürümlerinin desteklediği için bkz [mimari ve Modelleme Araçları sürüm desteği](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport).

## <a name="key-tasks"></a>Anahtar görevler

Sisteminizi doğrulamak için aşağıdaki görevleri kullanın:

|**Görevler**|**İlişkili konular**|
|-|-|
|**Yazılım kullanıcıların gereksinimleri karşıladığından emin olun**:<br /><br />Gereksinimleri ve mimari modelleri, sistemin ve bileşenlerinin testleri düzenlemenize yardımcı olması için kullanın. Bu uygulama, kullanıcıların ve diğer proje katılımcıları için önemli olan gereksinimleri test etmek ve gereklilikler değiştiğinde testleri hızlı bir şekilde güncelleştirmenize yardımcı emin olun yardımcı olur.|- [Model aracılığıyla test geliştirme](../modeling/develop-tests-from-a-model.md)|
|**Yazılım sisteminizin hedeflenen tasarım ile tutarlı kalmasından emin olun:**<br /><br />Bağımlılık diyagramları uygulamanızın bileşenleri arasında istenen bağımlılıkları açıklar. Geliştirme sırasında gerçek kod bağımlılıkları hedeflenen tasarım ile uyumlu olduğunu doğrulayabilirsiniz.|- [Kodunuz aracılığıyla bağımlılık diyagramları oluşturma](../modeling/create-layer-diagrams-from-your-code.md)<br />- [Bağımlılık diyagramları ile kod doğrulama](../modeling/validate-code-with-layer-diagrams.md)|

## <a name="external-resources"></a>Dış Kaynaklar

|**Kategori**|**Bağlantılar**|
|-|-|
|**Videolar**|![video bağlantı](../data-tools/media/playvideo.gif) [Channel 9: Doug yedi: Kod anlama ve Visual Studio 2010 ile sistem tasarımı](https://channel9.msdn.com/shows/VS2010Launch/Doug-Seven-Code-Understanding-and-Systems-Design-with-Visual-Studio-2010)<br /><br /> ![video bağlantı](../data-tools/media/playvideo.gif) [Channel 9: Uygulama Mimarisi oluşturma](https://channel9.msdn.com/blogs/clinted/uml-with-vs-2010-part-5-architecting-an-application))|
|**Forumları**|- [Visual Studio Görselleştirme ve Modelleme Araçları](https://social.msdn.microsoft.com/Forums/en-US/home?forum=vsarch)<br />- [Visual Studio genişletilebilirliği](https://social.msdn.microsoft.com/Forums/vstudio/home?forum=vsx)|

## <a name="see-also"></a>Ayrıca bkz.

- [Kullanıcı gereksinimlerini modelleme](../modeling/model-user-requirements.md)
- [Analiz ve model mimarisi](../modeling/analyze-and-model-your-architecture.md)

[!INCLUDE[modeling_sdk_info](includes/modeling_sdk_info.md)]
