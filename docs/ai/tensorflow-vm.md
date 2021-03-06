---
title: TensorFlow modeli bulutta çalıştırın
description: tensorflow modeli derin öğrenme azure'da çalıştırın
keywords: yapay zeka, visual studio, ayrıntılı öğrenme sanal makinesi
author: lisawong19
ms.author: liwong
manager: routlaw
ms.date: 11/13/2017
ms.topic: tutorial
ms.devlang: python
ms.workload:
- multiple
ms.openlocfilehash: adb3720f1624f355b99d75bfe446fafab1c5e0ae
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62427589"
---
# <a name="train-a-tensorflow-model-in-the-cloud"></a>Bulutta bir TensorFlow modeli eğitme

Bu öğreticide, TensorFlow modelini kullanarak biz eğitme [MNIST dataset](http://yann.lecun.com/exdb/mnist/) bir azure'da [derin öğrenme](https://docs.microsoft.com/azure/machine-learning/data-science-virtual-machine/deep-learning-dsvm-overview) sanal makine.

MNIST veritabanını 60.000 örnekler Eğitim kümesi ve el yazısı basamak 10.000 örnekleri test kümesi vardır.

## <a name="prerequisites"></a>Önkoşullar
Başlamadan önce aşağıdaki yüklenmiş ve yapılandırılmış olduğundan emin olun:

### <a name="setup-azure-deep-learning-virtual-machine"></a>Azure ayrıntılı öğrenme sanal makinesi kurma

> [!NOTE]
> Ayarlama **işletim sistemi türü** Linux'a.

Ayrıntılı öğrenme sanal makinesi ayarlanıyor yönergeler bulunabilir [burada](https://docs.microsoft.com/azure/machine-learning/data-science-virtual-machine/provision-deep-learning-dsvm).

### <a name="remove-comment-in-parens"></a>Remove açıklamada parens

```bash
echo -e ". /etc/profile\n$(cat ~/.bashrc)" > ~/.bashrc
```

### <a name="download-sample-code"></a>Örnek kodu indirin

Bu indirme [GitHub deposu](https://github.com/Microsoft/samples-for-ai) TensorFlow, CNTK, Theano ve daha derin öğrenme ile çalışmaya başlama örnekler içeren.

## <a name="open-project"></a>Projeyi açma

- Visual Studio'yu başlatın ve seçin **Dosya > Aç > Proje/çözüm**.

- Seçin **Tensorflow örnekler** klasörü açık ve indirilen örnek deposundan **TensorflowExamples.sln** dosya.

   ![Projeyi açma](media/tensorflow-local/open-project.png)

   ![Çözüm Aç](media/tensorflow-local/open-solution.png)

## <a name="add-azure-remote-vm"></a>Uzak Azure VM Ekle

Sunucu Gezgini'nde sağ tıklayın **uzak makinede** düğümü seçin ve yapay ZEKA araçları düğümü altında "Ekle...". Uzak makine görünen adı, IP konak, SSH bağlantı noktası, kullanıcı adı ve parola/anahtar dosyası girin.

![Yeni bir uzak makine Ekle](media/tensorflow-vm/add-remote-vm.png)

## <a name="submit-job-to-azure-vm"></a>Azure VM için iş gönderme
MNIST projeye sağ **Çözüm Gezgini** seçip **işi Gönder**.

![Uzak bir makine için iş gönderme](media/tensorflow-vm/job-submission.png)

Gönderim penceresinde:

- Listesinde **kullanmak için küme**, uzak makine seçin (ile "rm:" ön eki) için işi göndermek için.

- Girin bir **iş adı**.

- **Gönder**'e tıklayın.

## <a name="check-status-of-job"></a>İş durumunu denetleyin
Durum ve işlerinin ayrıntılarını görmek için: sanal makine içinde işe gönderdiğiniz genişletin **Sunucu Gezgini**. Çift **işleri**.

![İş tarayıcı](media/tensorflow-vm/job-browser.png)

## <a name="clean-up-resources"></a>Kaynakları temizleme

Yakın gelecekte kullanmayı planlıyorsanız, sanal Makineyi durdurun. Bu öğreticiyle tamamladıysanız, kaynakları temizlemek için aşağıdaki komutu çalıştırın:

```azurecli-interactive
az group delete --name myResourceGroup
```
