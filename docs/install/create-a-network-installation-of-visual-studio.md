---
title: Bir ağ tabanlı yüklemesini oluşturma
description: Visual Studio içinde bir kuruluş dağıtımı için bir ağ yükleme noktasını oluşturmayı öğrenin.
ms.date: 04/26/2019
ms.custom: seodec18
ms.topic: conceptual
helpviewer_keywords:
- '{{PLACEHOLDER}}'
- '{{PLACEHOLDER}}'
ms.assetid: 4CABFD20-962E-482C-8A76-E4012052F701
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: c0ac63fda69290bef28604cda7524a318c01edc8
ms.sourcegitcommit: 01c3c9dcade5d913bde2c7efa8c931a7b04e6cd0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/25/2019
ms.locfileid: "67365340"
---
# <a name="create-a-network-installation-of-visual-studio"></a>Visual Studio'nun bir ağ oluşturun

Genellikle, bir kuruluş yöneticisi istemci iş istasyonlarına dağıtmak için bir ağ yükleme noktası oluşturur. Visual Studio, tek bir klasöre tüm ürün güncelleştirmeleri ile birlikte ilk yükleme dosyaları önbelleğe almak sağlamak için tasarladık. (Bu işlem, ayrıca olarak adlandırılır _bir düzen oluşturma_.)

Böylece istemci iş istasyonları, aynı ağ konumunu en son hizmet güncelleştirmesi güncelleştirilmemiş olmasanız bile yükleme yönetmek için kullanabilirsiniz biz bunu yaptık.

 > [!NOTE]
 > (Örneğin, Visual Studio Professional ve Visual Studio Enterprise), kuruluşunuzda kullanımda Visual Studio'nun birden çok sürüm varsa, bir her sürümü için ayrı bir ağ yükleme paylaşımı oluşturmanız gerekir.

## <a name="download-the-visual-studio-bootstrapper"></a>Visual Studio önyükleyicisini yükleyin

İstediğiniz Visual Studio sürümünü indirin. Tıkladığınızdan emin olun **Kaydet**ve ardından **Klasör Aç**.

Kurulumunuzu yürütülebilir&mdash;veya daha özel bir önyükleyici dosya&mdash;aşağıdakilerden biriyle eşleşmesi gerekir.

::: moniker range="vs-2017"

|Sürüm | İndir|
|-------------|-----------------------|
|Visual Studio Enterprise | [**vs_enterprise.exe**](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=enterprise&rel=15&utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=network+install&utm_content=download+vs2017) |
|Visual Studio Professional | [**vs_professional.exe**](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=professional&rel=15&utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=network+install&utm_content=download+vs2017) |

Desteklenen diğer önyükleyiciler dahil [vs_buildtools.exe](https://aka.ms/vs/15/release/vs_buildtools.exe), [vs_feedbackclient.exe](https://aka.ms/vs/15/release/vs_feedbackclient.exe), [vs_teamexplorer.exe](https://aka.ms/vs/15/release/vs_teamexplorer.exe), [vs_testagent.exe](https://aka.ms/vs/15/release/vs_testagent.exe), [vs_testcontroller.exe](https://aka.ms/vs/15/release/vs_testcontroller.exe), ve [vs_testprofessional.exe](https://aka.ms/vs/15/release/vs_testprofessional.exe).

::: moniker-end

::: moniker range="vs-2019"

|Sürüm | İndir|
|-------------|-----------------------|
|Visual Studio Enterprise | [**vs_enterprise.exe**](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=enterprise&rel=16&utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=network+install&utm_content=download+vs2019) |
|Visual Studio Professional | [**vs_professional.exe**](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=professional&rel=16&utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=network+install&utm_content=download+vs2019) |

Desteklenen diğer önyükleyiciler dahil [vs_buildtools.exe](https://aka.ms/vs/16/release/vs_buildtools.exe), [vs_teamexplorer.exe](https://aka.ms/vs/16/release/vs_teamexplorer.exe), [vs_testagent.exe](https://aka.ms/vs/16/release/vs_testagent.exe), ve [vs_testcontroller.exe](https://aka.ms/vs/16/release/vs_testcontroller.exe).

::: moniker-end

## <a name="create-an-offline-installation-folder"></a>Bir çevrimdışı yükleme klasörü oluşturun

Bu adımı tamamlamak için bir internet bağlantısı olması gerekir. Tüm diller ve tüm özellikleri ile çevrimdışı yükleme oluşturmak için aşağıdaki örnekleri komutlardan birini kullanın.

   > [!IMPORTANT]
   > Visual Studio Düzen tamamlanamadı, en az 35 GB disk alanı gerektirir ve indirmek için biraz zaman alabilir. Bkz: [ağ düzeni özelleştirme](#customize-the-network-layout) bölüm düzeni yalnızca yüklemek istediğiniz bileşenleri oluşturma hakkında ayrıntılar için.
   >
   > [!TIP]
   > İndirme dizininize komutu çalıştırdığınızdan emin olun. Genellikle, bu `C:\Users\<username>\Downloads` Windows 10 çalıştıran bir bilgisayarda.

- Visual Studio Enterprise'ı çalıştırın:

  ```vs_enterprise.exe --layout c:\vsoffline```

- Visual Studio Professional için çalıştırın:

  ```vs_professional.exe --layout c:\vsoffline```

## <a name="modify-the-responsejson-file"></a>Response.json dosyasını değiştirme

Kurulumu çalıştırdığınızda kullanılan varsayılan değerleri ayarlamak için response.json değiştirebilirsiniz.  Örneğin, yapılandırabileceğiniz `response.json` dosyasını otomatik olarak seçilen iş yüklerini belirli bir dizi seçin.
Bkz: [otomatikleştirmek Visual Studio yükleme yanıt dosyası ile](automated-installation-with-response-file.md) Ayrıntılar için.

## <a name="copy-the-layout-to-a-network-share"></a>Düzen bir ağ paylaşımına kopyalayın.

Diğer makinelerden çalıştırılabilir için bir ağ paylaşımındaki düzenini barındırın.

::: moniker range="vs-2017"

Örnek:

```cmd
xcopy /e c:\vsoffline \\server\products\VS2017
```

::: moniker-end

::: moniker range="vs-2019"

```cmd
xcopy /e c:\vsoffline \\server\products\VS2019
```

::: moniker-end

> [!IMPORTANT]
> Bir hatayı önlemek için tam bir düzen yolu 80 karakterden uzun daha az olduğundan emin olun.

## <a name="customize-the-network-layout"></a>Ağ düzeni özelleştirme

Ağ düzeninize özelleştirmek için kullanabileceğiniz birkaç seçenek vardır. Yalnızca belirli bir dizi içeren bir kısmi düzeni oluşturabilirsiniz [dil yerel](use-command-line-parameters-to-install-visual-studio.md#list-of-language-locales), [iş yükleri, bileşenler ve önerilen ya da isteğe bağlı bağımlılıklarını](workload-and-component-ids.md). Bu, yalnızca bir alt iş yüklerinin istemci iş istasyonlarına dağıtacağız olduğunu bildiğiniz durumlarda yararlı olabilir. Düzeni özelleştirmek için tipik komut satırı parametreleri şunlardır:

* `--add` belirtmek için [iş yükü veya Bileşen kimlikleri](workload-and-component-ids.md). <br>Varsa `--add` kullanıldığında, yalnızca bu iş yüklerinin ve bileşenlerin belirtilen `--add` indirilir.  Varsa `--add` değil kullanıldığında, tüm iş yüküne ve bileşenlere indirilir.
* `--includeRecommended` Belirtilen iş yükü kimlikleri için önerilen tüm bileşenleri eklemek için
* `--includeOptional` Belirtilen iş yükü kimlikleri için tüm önerilen ve isteğe bağlı bileşenleri eklemek için.
* `--lang` belirtmek için [dil yerel](use-command-line-parameters-to-install-visual-studio.md#list-of-language-locales).

Özel bir kısmi düzen oluşturma bazı örnekleri aşağıda verilmiştir.

* Tüm iş yükleri ve bileşenler için yalnızca bir dil yüklemek için çalıştırın:

    ```cmd
    vs_enterprise.exe --layout C:\vsoffline --lang en-US
    ```

* Tüm iş yüklerinin ve bileşenlerin birden çok dil için karşıdan yüklemek için şunu çalıştırın:

    ```cmd
    vs_enterprise.exe --layout C:\vsoffline --lang en-US de-DE ja-JP
    ```

* Tüm diller için bir iş yükü indirmek için çalıştırın:

    ```cmd
    vs_enterprise.exe --layout C:\vsoffline --add Microsoft.VisualStudio.Workload.Azure --includeRecommended
    ```

* İki iş yükü ve üç diller için isteğe bağlı bir bileşen yüklemek için şunu çalıştırın:

    ```cmd
    vs_enterprise.exe --layout C:\vsoffline --add Microsoft.VisualStudio.Workload.Azure --add Microsoft.VisualStudio.Workload.ManagedDesktop --add Component.GitHub.VisualStudio --includeRecommended --lang en-US de-DE ja-JP
    ```

* İki iş yükü ve tüm önerilen bileşenleri yüklemek için:

    ```cmd
    vs_enterprise.exe --layout C:\vsoffline --add Microsoft.VisualStudio.Workload.Azure --add Microsoft.VisualStudio.Workload.ManagedDesktop --add Component.GitHub.VisualStudio --includeRecommended
    ```

* İki iş yükü ve tüm önerilen ve isteğe bağlı bileşenleri yüklemek için çalıştırın:

    ```cmd
    vs_enterprise.exe --layout C:\vsoffline --add Microsoft.VisualStudio.Workload.Azure --add Microsoft.VisualStudio.Workload.ManagedDesktop --add Component.GitHub.VisualStudio --includeOptional
    ```

::: moniker range="vs-2017"

### <a name="new-in-version-153"></a>Yeni sürüm 15.3

::: moniker-end

::: moniker range="vs-2019"

### <a name="save-your-layout-options"></a>Düzen seçeneklerinizi Kaydet

::: moniker-end

Bir düzen komutu çalıştırdığınızda, belirttiğiniz seçenekleri (iş yüklerini ve dilleri gibi) kaydedilir. Sonraki Düzen komutları tüm önceki seçenekleri içerir.  Bir iş yüküyle İngilizce için yalnızca bir düzen örneği aşağıda verilmiştir:

```cmd
vs_enterprise.exe --layout c:\VSLayout --add Microsoft.VisualStudio.Workload.ManagedDesktop --lang en-US
```

Bu düzeni daha yeni bir sürüme güncelleştirmek istediğiniz zaman herhangi ek komut satırı parametrelerini belirtmeniz gerekmez. Önceki ayarları kaydedilir ve bu düzen klasördeki herhangi bir sonraki Düzen komut tarafından kullanılır.  Aşağıdaki komut, var olan kısmi düzenini güncelleştirir.

```cmd
vs_enterprise.exe --layout c:\VSLayout
```

Bunu yapmak nasıl bir örneği bir ek yükünün, burada eklemek istediğinizde. Bu durumda, Azure iş yükü ve yerelleştirilmiş dili ekleyeceğiz.  Şimdi, hem yönetilen Masaüstü hem de Azure Bu düzende dahil edilir.  İngilizce ve Almanca dil kaynakları için bu iş yükleri dahil edilir. Düzeni, kullanılabilir en son sürüme güncelleştirilir.

```cmd
vs_enterprise.exe --layout c:\VSLayout --add Microsoft.VisualStudio.Workload.Azure --lang de-DE
```

Varolan bir düzen bir tam düzeni güncelleştirmek istiyorsanız, kullanın all seçeneği, aşağıdaki örnekte gösterildiği gibi.

```cmd
vs_enterprise.exe --layout c:\VSLayout --all
```

## <a name="deploy-from-a-network-installation"></a>Bir ağ yüklemesinden dağıtma

Yöneticiler, bir yükleme betiğinin bir parçası istemci iş istasyonlarında Visual Studio dağıtabilirsiniz. Veya yönetici haklarına sahip kullanıcılar, makinede Visual Studio'yu yüklemek için doğrudan paylaşımından Kurulumu çalıştırın.

* Kullanıcılar, aşağıdaki komutu çalıştırarak yükleyebilirsiniz: <br>

    ```cmd
    \\server\products\VS\vs_enterprise.exe
    ```

* Yöneticiler, katılımsız modda, aşağıdaki komutu çalıştırarak yükleyebilirsiniz:

    ```cmd
    \server\products\VS\vs_enterprise.exe --quiet --wait --norestart
    ```

> [!IMPORTANT]
> Bir hatayı önlemek için tam bir düzen yolu 80 karakterden uzun daha az olduğundan emin olun.
>
> [!TIP]
> Bir toplu iş dosyası bir parçası olarak çalıştırıldığında `--wait` seçeneği sağlar `vs_enterprise.exe` işlem çıkış kodu döndürür önce yükleme işlemi tamamlanana kadar bekler.
>
> Daha fazla tamamlanmış bir yüklemeyi eylemleri gerçekleştirmek Kurumsal Yönetici isterse kullanışlıdır (örneğin, [yüklemenin başarılı olabilmesi için bir ürün anahtarını uygulayan](automatically-apply-product-keys-when-deploying-visual-studio.md)) ancak yükleme işlemek için tamamlanıncaya kadar beklemeniz gerekir Bu yükleme dönüş kodu.
>
> Kullanmıyorsanız, `--wait`, `vs_enterprise.exe` işlem çıkar önce yükleme tamamlandıktan ve yükleme işleminin durumunu temsil etmez, hatalı çıkış kodu döndürür.

Bir düzenden yükleme sırasında düzeninde yüklü içeriği alınır. Düzende olmayan bir bileşen seçtiğinizde, ancak bunu internet'ten gerekilir.  Visual Studio kurulumunu kullanın, düzende eksik herhangi bir içerik indirmesini önlemek istiyorsanız `--noWeb` seçeneği. Varsa `--noWeb` kullanılır ve düzenini seçili yüklenmesi başarısız kurulum için herhangi bir içeriği eksik.

> [!IMPORTANT]
> `--noWeb` Seçeneği, güncelleştirmeleri denetlemesini Visual Studio Kurulumu Durdur değil. Daha fazla bilgi için [ağ tabanlı Visual Studio dağıtımlarına yönelik güncelleştirmeleri denetlemek](controlling-updates-to-visual-studio-deployments.md) sayfası.

### <a name="error-codes"></a>Hata kodları

Kullandıysanız `--wait` parametresi ve ardından işlemi sonucuna bağlı olarak `%ERRORLEVEL%` ortam değişkeni aşağıdaki değerlerden birine ayarlanır:

[!INCLUDE[install-error-codes-md](includes/install-error-codes-md.md)]

## <a name="update-a-network-install-layout"></a>Bir ağ yükleme düzeni güncelleştirme

Ürün güncelleştirmeleri kullanılabilir oldukça isteyebilirsiniz [ağ yükleme düzeni güncelleştirme](update-a-network-installation-of-visual-studio.md) güncelleştirilmiş paket birleştirmek için.

## <a name="how-to-create-a-layout-for-a-previous-visual-studio-release"></a>Önceki bir Visual Studio sürümü için bir düzen oluşturma

::: moniker range="vs-2017"

> [!NOTE]
> Mevcut Visual Studio Önyükleyiciler ile [visualstudio.microsoft.com](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) indirin ve çalıştıkları zaman kullanılabilir en son Visual Studio sürümünü yükleyin.
>
> Bunu, Visual Studio yüklerseniz *önyükleyici* Bugün ve BT altı ay şu andan itibaren önyükleyici çalıştırdığınız anda geçerli olan Visual Studio'nun sürümünü yükler.
>
> Ancak oluşturursanız, bir *Düzen* ve indirip yükleyin, Düzen düzende var. Visual Studio'nun belirli sürümü yükler. Yeni bir sürüme çevrimiçi mevcut olabilecek olsa da, düzeni Visual Studio'nun sürümü alın.

::: moniker-end

::: moniker range="vs-2019"

> [!NOTE]
> Mevcut Visual Studio Önyükleyiciler ile [visualstudio.microsoft.com](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) indirin ve çalıştıkları zaman kullanılabilir en son Visual Studio sürümünü yükleyin.
>
> Bunu, Visual Studio yüklerseniz *önyükleyici* Bugün ve BT altı ay şu andan itibaren önyükleyici çalıştırdığınız anda geçerli olan Visual Studio'nun sürümünü yükler.
>
> Ancak oluşturursanız, bir *Düzen* ve indirip yükleyin, Düzen düzende var. Visual Studio'nun belirli sürümü yükler. Yeni bir sürüme çevrimiçi mevcut olabilecek olsa da, düzeni Visual Studio'nun sürümü alın.

::: moniker-end

Visual Studio'nun daha eski bir sürümü için bir düzen oluşturmanız gerekiyorsa, Git [ https://my.visualstudio.com ](https://my.visualstudio.com) "sabit" sürümlerini Visual Studio Önyükleyiciler ile indirilemedi.

### <a name="how-to-get-support-for-your-offline-installer"></a>Çevrimdışı yükleyicinizi için destek alma

Çevrimdışı yüklemenizle ilgili bir sorun yaşarsanız, bunu bilmek istiyoruz. Bize en iyi yolu kullanmaktır [sorun bildir](../ide/how-to-report-a-problem-with-visual-studio.md) aracı. Bu aracı, bize tanılayın ve sorunu çözmeye yardımcı olmak için ihtiyacımız olan günlükleri ve telemetri gönderebilir.

Ayrıca sunuyoruz bir [ **canlı sohbet** ](https://visualstudio.microsoft.com/vs/support/#talktous) yüklemeyle ilgili sorunlar için destek seçeneği (yalnızca İngilizce).

Diğer destek seçenekleri, çok sahibiz. Bir liste için bkz. bizim [geri bildirim](../ide/feedback-options.md) sayfası.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio Yönetici Kılavuzu](visual-studio-administrator-guide.md)
- [Visual Studio’nun ağ tabanlı yüklemesini güncelleştirme](update-a-network-installation-of-visual-studio.md)
- [Ağ tabanlı Visual Studio dağıtımlarına yönelik güncelleştirmeleri denetleme](controlling-updates-to-visual-studio-deployments.md)
- [Visual Studio ürün yaşam döngüsü ve Bakım](/visualstudio/releases/2019/servicing/)
- [Bakım sırasında temel Visual Studio güncelleştirme](update-servicing-baseline.md)
- [Komut satırı parametrelerini kullanarak Visual Studio'yu yükleme](use-command-line-parameters-to-install-visual-studio.md)
- [Visual Studio iş yükü ve bileşen kimlikleri](workload-and-component-ids.md)
