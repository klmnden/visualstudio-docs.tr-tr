---
title: Proje oluşturma
description: örneğini kullanarak azure machine learning Galeriden proje oluşturma
keywords: yapay zeka, visual studio, azure machine learning
author: lisawong19
ms.author: liwong
manager: routlaw
ms.date: 11/13/2017
ms.topic: conceptual
ms.workload:
- multiple
ms.openlocfilehash: 5694bfe49e88d0ea5911e72abba842e98f54e373
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62538069"
---
# <a name="create-an-ai-project-from-the-azure-machine-learning-gallery-in-visual-studio"></a>Yapay ZEKA proje Visual Studio'da Azure Machine Learning Galerisi oluşturma

Azure Machine Learning, yapay ZEKA için Visual Studio Araçları ile tümleşiktir. Machine learning gibi Azure sanal makineleri, Spark kümelerine ve daha fazla uzak bilgisayar hedefine göndermek için kullanabilirsiniz. Daha fazla bilgi edinin [Azure Machine Learning denemesi](https://docs.microsoft.com/azure/machine-learning/preview/experimentation-service-configuration)

Kaydederler [yapay ZEKA için Visual Studio Araçları yüklü](installation.md), Azure Machine Learning örnek galerideki önceden yapılmış tarifleri kullanarak yeni Python projesi oluşturmak daha kolaydır.

> [!NOTE]
> Azure Machine Learning Workbench yüklenmiş olmalıdır. Lütfen bkz. yüklemek için [Azure Machine Learning yükleme hızlı başlangıç](https://docs.microsoft.com/azure/machine-learning/preview/quickstart-installation)

1. Visual Studio'yu başlatın. Açık **Sunucu Gezgini** açarak **yapay ZEKA Araçları** menü ve seçme **kümesi seçin**

    ![Küme Seçici](media/create-project-gallery/select-cluster.png)

2. Azure Machine Learning aboneliğinize sağ tıklayarak oturum açın **Azure Machine Learning** Sunucu Gezgininde seçip **oturum açma** ve yönergeleri izleyin.

    ![Oturum açma](media/create-project-gallery/azureml-login.png)

3. Seçin **yapay ZEKA araçları > Azure Machine Learning örnek Galerisi**.

    ![Örnek Galerisi](media/create-project-gallery/gallery.png)

4. Bu hızlı başlangıçta seçin "**TensorFlow kullanarak MNIST**" örnek ve tıklayın **yükleme**. Aşağıdakileri sağlar:

   - **Kaynak grubu**: Meta verilerinizi depolanacağı azure kaynak grubu
   - **Hesap**: Azure Machine Learning denemesi hesabı
   - **Çalışma alanı**: Azure Machine Learning çalışma alanı
   - **Proje türü**: Makine öğrenmesi çerçeveleri. Bu durumda seçin **TensorFlow**
   - **Çözüme eklemek**: geçerli Visual Studio çözümünüzü veya bir oluşturma eklemek ve yeni bir çözüm açın belirler
   - **Proje yolu**: Kod kaydetmek için konum
   - **Proje adı**: Tür **TensorFlowMNIST**

   ![Python uygulaması şablonu kullanılarak elde edilen proje](media/create-project-gallery/new-AzureSampleProject.png)

5. Visual Studio Proje dosyası oluşturur (bir `.pyproj` diskteki dosyanın) birlikte örnekte tanımlanan diğer dosyalar. "MNIST" şablonu ile çeşitli dosyalar projesi içerir.

    ![mnıst](media/create-project-gallery/azml-mnist.png)

6. Azure Machine Learning iş gönderin.

    ![mnıst](media/create-project-gallery/submit-azml.png)

7. Yerel makinenizde veya bir Docker kapsayıcısında çalıştırma

    ![mnıst](media/create-project-gallery/azml-local.png)