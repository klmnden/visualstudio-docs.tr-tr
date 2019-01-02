---
title: 'Nasıl Yapılır: Gölgelendiriciyi dışarı aktarma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 0bd48bf4-9792-4456-a545-e462a2be668d
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 92e0ae391cb196053d136dc44a8e64758f485115
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53861458"
---
# <a name="how-to-export-a-shader"></a>Nasıl Yapılır: Gölgelendiriciyi dışarı aktarma

Bu makalede nasıl yapılacağı açıklanır **gölgelendirici Tasarımcısı** böylece uygulamanızda kullanabilirsiniz yönlendirilmiş grafik gölgelendirici dili (DGSL) gölgelendiriciyi dışarı aktarma için.

## <a name="export-a-shader"></a>Gölgelendiriciyi dışarı aktarma

Gölgelendirici Tasarımcısı'nı kullanarak ve uygulamanızda kullanmadan önce bir gölgelendirici oluşturduktan sonra bunu, grafik API'si anlayan bir biçimde dışarı aktarmanız gerekir. Farklı ihtiyaçları karşılamak üzere farklı şekillerde gölgelendiriciyi dışarı aktarabilirsiniz.

1. Visual Studio'da açın bir **görsel gölgelendirici grafiği (.dgsl)** dosya.

     Yoksa bir **görsel gölgelendirici grafiği (.dgsl)** açın, içinde açıklandığı gibi oluşturmak için dosya [nasıl yapılır: Temel renk gölgelendiricisi oluşturma](../designers/how-to-create-a-basic-color-shader.md).

2. Üzerinde **gölgelendirici Tasarımcısı** araç seçin **Gelişmiş** > **dışarı** > **dışarı aktarma olarak**. **Gölgelendiriciyi dışarı aktarma** iletişim kutusu görüntülenir.

3. İçinde **farklı kaydetme türü** aşağı açılan listesinde, dışa aktarmak istediğiniz biçimi seçin.

     Seçebileceğiniz biçimler şunlardır:

     **HLSL piksel gölgelendiricisi (\*.hlsl)** gölgelendirici üst düzey gölgelendirici dili (HLSL) kaynak kodu dışarı aktarır. Bu seçenek, bir uygulamada bile dağıtıldıktan sonra gölgelendirici daha sonra değiştirmek mümkün kılar. Bu, hata ayıklama ve son kullanıcı sorunları göre kod düzeltme eki kolaylaştırabilir, ancak aynı zamanda istenmeyen yollarla gölgelendiricinize değiştirmek bir kullanıcı için kolaylaştırır — Örneğin, bir rekabet oyununda bir haksız avantaj elde etmek için. Gölgelendirici yükleme süresi da artırabilir.

     **Derlenmiş piksel gölgelendiricisi (\*.cso)** gölgelendirici HLSL bayt dışarı aktarır. Bu seçenek, bir uygulamada bile dağıtıldıktan sonra gölgelendirici daha sonra değiştirmek mümkün kılar. Bu, hata ayıklama ve son kullanıcı sorunları göre kod düzeltme eki kolaylaştırabilir, ancak önceden derlenmiş gölgelendirici olduğundan, gölgelendirici uygulama tarafından yüklendiğinde, ek çalışma zamanı yükü tabi değildir. Yeterince deneyimli kullanıcılar hala istenmeyen yollarla gölgelendiriciyi değiştirebilirsiniz, ancak gölgelendirici derleme bu önemli ölçüde daha zor hale getirir.

     **C++ üst bilgisi (\*.h)** gölgelendirici HLSL bayt içeren bir bayt dizisi tanımlayan bir C stili başlığı dışarı aktarır. Bu seçenek, hata ayıklama ve son kullanıcı sorunlarını düzeltme test etmek için uygulamayı yeniden derlenmesi için temel kod düzeltme eki daha fazla zaman zorlaştırabilir. Ancak, bu seçenek, imkansız olsa, bir uygulama dağıtıldıktan sonra gölgelendirici değiştirmek zorlaştırır çünkü gölgelendirici istenmeyen yollarla değiştirmek isteyen bir kullanıcı için birçok zorluk sunduğu.

4. İçinde **dosya adı** birleşik giriş kutusu, dışarı aktarılan gölgelendirici için bir ad belirtin ve ardından **Kaydet** düğmesi.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Temel renk gölgelendiricisi oluşturma](../designers/how-to-create-a-basic-color-shader.md)
- [Gölgelendirici Tasarımcısı](../designers/shader-designer.md)