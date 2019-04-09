---
title: Hızlı Başlangıç - Python kodu klasörünü açın
description: Bu hızlı başlangıçta, açın ve Visual Studio projesi (Visual Studio 2019 yalnızca) kullanmadan bir klasörden Python kodunu çalıştırma.
ms.date: 03/12/2019
ms.topic: quickstart
author: JoshuaPartlow
ms.author: joshuapa
manager: jillfra
ms.custom: seodec18
ms.workload:
- python
- data-science
monikerRange: '>= vs-2019'
ms.openlocfilehash: ab234d9482cf9cbab49c15167ea45aff9ac2c7e6
ms.sourcegitcommit: 0e22ead8234b2c4467bcd0dc047b4ac5fb39b977
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59366126"
---
# <a name="quickstart-open-and-run-python-code-in-a-folder"></a>Hızlı Başlangıç: Python kodunu bir klasörde açma ve çalıştırma

Kaydederler [Python desteği Visual Studio 2019 yüklü](installing-python-support-in-visual-studio.md), Visual Studio projesi oluşturmaya gerek kalmadan mevcut Python kodu Visual Studio 2019 ' çalıştırmak daha kolaydır.

> [!Note]
> Visual Studio 2017 ve öncesinde kolayca Python kodu çalıştırmak için Visual Studio projesi oluşturmak gerekli bir yerleşik proje şablonunu kullanarak yapın. Bkz: [hızlı başlangıç: Varolan koddan bir Python projesi oluşturma](quickstart-01-python-in-visual-studio-project-from-existing-code.md)

1. Bu kılavuz için istediğiniz ipucuyla Python kodunda herhangi bir klasörü kullanabilirsiniz. Burada gösterilen örnek ile birlikte izlemek için gregmalcolm/python_koans GitHub deposu'komutunu kullanarak bilgisayarınıza kopyalayın `git clone https://github.com/gregmalcolm/python_koans` uygun bir klasörde.

1. Visual Studio 2019 başlatın ve başlangıç penceresinde **açık** kısmındaki **başlama** sütun. Alternatif olarak, Visual Studio çalıştırma zaten varsa, seçin **dosya** > **açık** > **klasör** yerine komutu.

    ![Visual Studio Başlangıç ekranı](media/quickstart-open-folder/01-open-local-folder.png)

1. Python kodunuzu içeren klasöre gidin ve ardından **Klasör Seç**. Python_koans kod kullanıyorsanız, seçtiğinizden emin olun `python3` klasörüne kopyalama.

    ![Klasör Seç iletişim kutusundan Klasör Aç komutu](media/quickstart-open-folder/02-select-folder.png)

1. Visual Studio görüntüler klasöründe **Çözüm Gezgini** ne çağrılır içindeki **klasör görünümü**. Genişletin ve klasörleri okları kullanarak klasör adlarını sol kenarları üzerinde Daralt:

    ![Çözüm Gezgini'nde klasörleri daraltmak ve genişletmek için denetimleri](media/quickstart-open-folder/03-expand-collapse-folders.png)

1. Bir Python klasör açılırken Visual Studio ayarlarını projeyle ilgili yönetmek için birkaç gizli klasörlere oluşturur. Bu klasör görmek için (ve diğer gizli dosyalar ve klasörler gibi *.git* klasör), select **tüm dosyaları göster** araç çubuğu düğmesi:

    ![Çözüm Gezgini'nde, gizli klasörlere ilişkin bir görünüm](media/quickstart-open-folder/05-view-hidden-folders.png)

1. Kodu çalıştırmak için önce başlatmanın veya birincil program dosyası tanımlamak gerekir. Burada, başlangıç dosyasını gösterilen örnekte *contemplate koans.py*. Dosya ve seçin, sağ tıklama **başlangıç öğesi olarak ayarla**.

    ![Çözüm Gezgini'nde başlangıç öğesi ayarlama](media/quickstart-open-folder/06-set-as-startup-item-command.png)

    > [!Important]
    > Başlangıç öğeniz açtığınız klasörün kökünde yer almıyorsa, ayrıca bir satır başlatma yapılandırma JSON dosyasını bölümünde açıklandığı gibi eklemelisiniz [çalışan bir dizine ayarlayın](#set-a-working-directory).

1. Kodu tuşuna basarak çalıştırın **Ctrl**+**F5** veya seçerek **hata ayıklama** > **hata ayıklama olmadan Başlat**. Başlangıç öğesi ile Visual Studio hata ayıklayıcıda kod çalıştıran bir Oynat düğmesini gösteren araç çubuğu düğmesini de seçebilirsiniz. Her durumda, Visual Studio, bu nedenle otomatik olarak varsayılan Python ortamda kod çalıştırılır, başlangıç öğesi bir Python dosyası olduğunu algılar. (Bu ortamda araç çubuğundaki başlangıç öğesi sağındaki gösterilir.)

    ![Hata ayıklayıcı araç çubuğu düğmesini Başlat](media/quickstart-open-folder/07-start-debug-toolbar.png)

1. Program çıkış ayrı komut penceresinde görünür:

    ![Python kodu çalıştırmak için çıkış penceresine](media/quickstart-open-folder/08-result-window.png)

1. Kodu farklı bir ortamda çalıştırmak için araç çubuğundaki açılan denetimden gelen o ortamı seçin, sonra başlangıç öğesini yeniden başlatın.

1. Visual Studio'da klasörü kapatın için seçin **dosya** > **Kapat klasör** menü komutu.

## <a name="set-a-working-directory"></a>Çalışan bir dizine ayarlayın

Varsayılan olarak, Visual Studio aynı klasörde kökünde bir klasör olarak açılan bir Python projesi çalıştırır. Kod projenizde, ancak Python bir alt klasöre çalıştırıldığı varsayabilirsiniz. Örneğin, python_koans deponun kök klasörü açın ve ardından varsayalım *python3/contemplate-koans.py* dosyası başlangıç öğesi olarak. Daha sonra kodu çalıştırmak bir hata görürsünüz, *koans.txt* dosyası bulunamıyor. Bu hata nedeniyle oluşur *contemplate koans.py* Python çalıştırıldığı olduğunu varsayar *python3* depo kökünde yerine klasör.

Bu gibi durumlarda, çalışma dizini belirtmek için başlatma yapılandırma JSON dosyasına bir satır da eklemeniz gerekir:

1. Python'ı sağ tıklayın (*.py*) başlangıç dosyasında **Çözüm Gezgini** seçip **hata ayıklama ve başlatma ayarları**.

    ![Bir Python dosyası için hata ayıklama ve başlatma ayarları komutu](media/quickstart-open-folder/09-debug-launch-settings-menu-command.png)

1. İçinde **seçin hata ayıklayıcı** görüntülenen Seç iletişim kutusu **varsayılan** seçip **seçin**.

    ![Bir Python dosyası için hata ayıklama ve başlatma ayarları komutu](media/quickstart-open-folder/10-select-debugger.png)

    > [!Note]
    > Görmüyorsanız **varsayılan** bir seçenek olarak, bir Python tıklattığınız mutlaka *.py* dosya seçerken **hata ayıklama ve başlatma ayarları** komutu. Visual Studio hata ayıklayıcısı seçenekleri görüntülemek için belirlemek için dosya türü kullanır.

1. Visual Studio adlı bir dosya açar *launch.vs.json*, bulunduğu gizli olarak *.vs* klasör. Bu dosya, proje için hata ayıklama içeriğini açıklar. Bir çalışma dizini belirlemek için bir değer ekleyin `"workingDirectory"`, olarak `"workingDirectory": "python3"` python koans örneğin:

    ```json
    {
      "version": "0.2.1",
      "defaults": {},
      "configurations": [
        {
          "type": "python",
          "interpreter": "(default)",
          "interpreterArguments": "",
          "scriptArguments": "",
          "env": {},
          "nativeDebug": false,
          "webBrowserUrl": "",
          "project": "python3\\contemplate_koans.py",
          "name": "contemplate_koans.py",
          "workingDirectory": "python3"
        }
      ]
    }
    ```

1. Dosyayı kaydedin ve programı yeniden başlatma, belirtilen klasörde şimdi çalıştırır.

## <a name="next-steps"></a>Sonraki adımlar

> [!div class="nextstepaction"]
> [Öğretici: Visual Studio'da Python ile çalışma](tutorial-working-with-python-in-visual-studio-step-01-create-project.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Hızlı Başlangıç: Varolan koddan bir Python projesi oluşturma](quickstart-01-python-in-visual-studio-project-from-existing-code.md)
- [Hızlı Başlangıç: Bir depodan bir Python projesi oluşturma](quickstart-03-python-in-visual-studio-project-from-repository.md)
- [El ile var olan bir Python yorumlayıcısı tanımlayın](managing-python-environments-in-visual-studio.md#manually-identify-an-existing-environment)
