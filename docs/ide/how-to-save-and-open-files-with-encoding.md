---
title: 'Nasıl Yapılır: Dosyaları kodlamayla kaydetme ve açma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- Unicode, bi-directional language support
- files, encoding
- bi-directional language support, encoded files
- file encoding, bi-directional languages
ms.assetid: cb52b732-b395-4ba1-a3ef-104b3942a12a
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 38d52cdee3ee0f6ccbdd378e4fb70e356d5826c2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53869576"
---
# <a name="how-to-save-and-open-files-with-encoding"></a>Nasıl Yapılır: Dosyaları kodlamayla kaydetme ve açma

Dosyaları belirli karakter çift yönlü dil desteği için kodlama ile kaydedebilirsiniz. Ayrıca, böylece Visual Studio dosyayı doğru görüntüler bir dosyayı açtığınızda kodlama belirtebilirsiniz.

## <a name="to-save-a-file-with-encoding"></a>Dosya kodlama ile kaydetmek için

1.  Gelen **dosya** menüsünde seçin **dosyayı farklı Kaydet**ve yanındaki açılan düğmeyi'ye tıklayın **Kaydet** düğmesi.

     **Gelişmiş kaydetme seçenekleri** iletişim kutusu görüntülenir.

2.  Altında **kodlama**, dosya için kullanılacak kodlama seçin.

3.  İsteğe bağlı olarak, altında **satır sonlarını**, satır sonu karakterleri için biçimi seçin.

     Bu seçenek dosyayı farklı bir işletim sistemi kullanıcılarla alışverişi yapmak istiyorsanız yararlıdır.

     Belirli bir biçimde kodlandı bildiğiniz bir dosyayla çalışmak istiyorsanız, Visual Studio kodlama dosyası açılırken kullanılacak söyleyebilirsiniz. Kullandığınız yöntem, dosyanın, projenizin bir parçası olmasına göre değişir.

## <a name="to-open-an-encoded-file-that-is-part-of-a-project"></a>Bir projenin parçası olan kodlanmış bir dosyayı açmak için

1.  İçinde **Çözüm Gezgini**, dosyaya sağ tıklayın ve seçin **birlikte Aç**.

2.  İçinde **birlikte Aç** iletişim kutusunda, dosyayı açmak için bir düzenleyici seçin.

     Form Düzenleyicisi gibi birçok Visual Studio düzenleyicileri kodlamasını Otomatik Algıla ve uygun şekilde dosyasını açın. Bir kodlama seçmenize olanak tanıyan bir düzenleyici seçerseniz **kodlama** iletişim kutusu görüntülenir.

3.  İçinde **kodlama** iletişim kutusunda, düzenleyici kullanması gereken kodlama seçin.

## <a name="to-open-an-encoded-file-that-is-not-part-of-a-project"></a>Bir projenin parçası değil kodlanmış bir dosyayı açmak için

1.  Üzerinde **dosya** menüsünde **açın**, seçin **dosya** veya **Web'den dosya**ve ardından dosyayı açmak için seçin.

2.  Yanındaki açılan düğmeyi tıklayın **açık** düğmesini tıklatın ve seçin **birlikte Aç**.

3.  Adım 2 ve 3 önceki yordamı izleyin.

## <a name="see-also"></a>Ayrıca bkz.

- [Kodlama ve satır sonları](encodings-and-line-breaks.md)
- [Kodlama ve Windows Forms Genelleştirme](/dotnet/framework/winforms/advanced/encoding-and-windows-forms-globalization)
- [Globalize ve uygulamaları yerelleştirme](../ide/globalizing-and-localizing-applications.md)