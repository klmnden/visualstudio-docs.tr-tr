---
title: Yerel olarak tensorflow modeli eğitme
description: Tensorflow modeli yapay ZEKA araçları Visual Studio için yerel olarak çalıştırın.
keywords: yapay zeka, visual studio, tensorflow, yerel
author: lisawong19
ms.author: liwong
manager: routlaw
ms.date: 11/13/2017
ms.topic: quickstart
ms.devlang: python
ms.workload:
- multiple
ms.openlocfilehash: 26668247bf993da3eb3f2803abaf9288e566ffee
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62555467"
---
# <a name="train-a-tensorflow-model-locally"></a>Yerel olarak TensorFlow modeli eğitme

Bu hızlı başlangıçta biz TensorFlow modeliyle eğitme [MNIST](http://yann.lecun.com/exdb/mnist/) yerel olarak yapay ZEKA için Visual Studio Araçları veri kümesi.

MNIST veritabanını 60.000 örnekler Eğitim kümesi ve el yazısı basamak 10.000 örnekleri test kümesi vardır.

## <a name="prerequisites"></a>Önkoşullar

Başlamadan önce aşağıdakilerin yüklü olduğundan emin olun:

### <a name="google-tensorflow"></a>Google TensorFlow

Bir terminalde aşağıdaki komutu çalıştırın:

```cmd
C:\>pip.exe install tensorflow
```

### <a name="numpy-and-scipy"></a>NumPy ve SciPy
Yükleme [NumPy](https://www.lfd.uci.edu/~gohlke/pythonlibs/#numpy) ve [SciPy](https://www.lfd.uci.edu/~gohlke/pythonlibs/#scipy).

### <a name="download-sample-code"></a>Örnek kodu indirin
Bu indirme [GitHub deposu](https://github.com/Microsoft/samples-for-ai) TensorFlow, CNTK, Theano ve daha fazlası arasında derin öğrenme ile çalışmaya başlama örnekler içeren.

## <a name="open-solution-and-train-model"></a>Modeli eğitmek ve çözümü açın

- Visual Studio'yu başlatın ve seçin **Dosya > Aç > Proje/çözüm**.

- Seçin **Tensorflow örnekler** klasörü açık ve indirilen örnek deposundan **TensorflowExamples.sln** dosya.

   ![Projeyi açma](media/tensorflow-local/open-project.png)

   ![Çözüm Aç](media/tensorflow-local/open-solution.png)

- MNIST projede bulma **Çözüm Gezgini**seçin ve sağ tıklatıp **başlangıç projesi olarak ayarla**.

- **Başlat**'a tıklayın.

- Çıkış konsolda yazdırılır.

   ![Örnek konsol çıktısı](media/tensorflow-local/console-output.png)

> [!div class="nextstepaction"]
> [Bulutta bir TensorFlow modeli eğitme](tensorflow-vm.md)