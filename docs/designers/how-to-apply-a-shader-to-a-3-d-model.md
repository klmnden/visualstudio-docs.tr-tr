---
title: 'Nasıl yapılır: 3B modele gölgelendirici uygulama'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: a3877bd6-abd8-4a9d-842c-6848b6c2f335
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8ef5f4f840991d78bc67f1ba32685e49765deaef
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54957409"
---
# <a name="how-to-apply-a-shader-to-a-3d-model"></a>Nasıl yapılır: 3B modele gölgelendirici uygulama

Bu makalede, 3B modele gölgelendirici yönlendirilmiş grafik gölgelendirici dili (DGSL) uygulamak için Model Düzenleyicisi'ni kullanma gösterilmektedir.

## <a name="apply-a-shader-to-a-3d-model"></a>3B modele gölgelendirici uygulama

İlgi çekici bir görünüm sağlamak için 3B modele gölgelendirici efekti uygulayabilirsiniz.

Başlamadan önce emin **özellikleri** penceresi görüntülenir.

1. Bir veya daha fazla modeli içeren bir 3B Sahne ile başlar. Uygun bir 3B Sahne yoksa açıklandığı gibi oluşturmak [nasıl yapılır: Temel 3B Model oluşturma](../designers/how-to-create-a-basic-3-d-model.md). Modele uygulayabileceğiniz bir DGSL gölgelendirici sahip olmalısınız. Uygun bir gölgelendirici yoksa açıklandığı gibi oluşturmak [nasıl yapılır: Temel renk gölgelendiricisi oluşturma](../designers/how-to-create-a-basic-color-shader.md) ve devam etmeden önce onu bir dosyayı kaydettiğinizden emin olun.

2. İçinde **seçin** modu, gölgelendirici uygulamak istediğiniz ve daha sonra modeli seçin **özellikleri** penceresi içinde **Filename** özelliği **etkisi**  özelliği Grup, modele uygulamak istediğiniz DGSL gölgelendirici belirtin.

Temel renk etkisi uygulanmış bir model şu şekildedir:

![3&#45;temel renk etkisini gösteren D Sahne](../designers/media/digit-3d-model-effect.png)

Bir modele gölgelendirici uygulama sonra bunu gölgelendirici Tasarımcısı'nda model seçerek ve sonra da açabilirsiniz **özellikleri** penceresi içinde **(Gelişmiş)** özelliği **etkisi**özellik grubu, üç nokta seçme (**...** ) düğmesi.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Temel 3B model oluşturma](../designers/how-to-create-a-basic-3-d-model.md)
- [Nasıl yapılır: Temel renk gölgelendiricisi oluşturma](../designers/how-to-create-a-basic-color-shader.md)
- [Model düzenleyicisi](../designers/model-editor.md)
- [Gölgelendirici tasarımcısı](../designers/shader-designer.md)