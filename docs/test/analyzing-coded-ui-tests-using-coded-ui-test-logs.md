---
title: Kodlanmış UI Test Günlüklerini Kullanarak Kodlanmış UI Testlerini Çözümleme
ms.date: 11/04/2016
ms.topic: conceptual
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 76aac39d50dc724916bca3d863c71bacf53407d9
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/11/2019
ms.locfileid: "67824490"
---
# <a name="analyzing-coded-ui-tests-using-coded-ui-test-logs"></a>Kodlanmış UI test günlüklerini çözümleme kodlanmış UI testleri kullanarak

Kodlanmış UI test günlüklerini filtre ve kayıt kodlanmış UI testleri hakkında önemli bilgiler çalıştırır. Günlükler, sorunları hızlı bir şekilde hata ayıklama için izin veren bir biçiminde gösterilir.

[!INCLUDE [coded-ui-test-deprecation](includes/coded-ui-test-deprecation.md)]

## <a name="step-1-enable-logging"></a>1\. Adım: Günlü kaydını etkinleştir

Senaryonuza bağlı olarak, günlüğü etkinleştirmek için aşağıdaki yöntemlerden birini kullanın:

- Yoksa hiçbir *App.config* test projenizde mevcut dosya:

   1. Belirleyen *QTAgent\*.exe* testinizi çalıştırdığınızda işlemi başlatıldı. Yapmanın bir yolu izlemek için budur **ayrıntıları** Windows sekmede **Görev Yöneticisi'ni**.
   
   2. Buna karşılık gelen açın *.config* dosya *% ProgramFiles (x86) %\Microsoft Visual Studio\\\<sürüm >\\\<sürümü > \Common7\IDE* klasör. Örneğin, işlemi çalıştıran ise *QTAgent_40.exe*açın *QTAgent_40.exe.config*.

   2. Değerini değiştirmek **gt;System.Diagnostics** istediğiniz günlük düzeyi.
   
      ```xml
      <!-- You must use integral values for "value".
           Use 0 for off, 1 for error, 2 for warn, 3 for info, and 4 for verbose. -->
      <add name="EqtTraceLevel" value="4" />
      ```

   3. Dosyayı kaydedin.

- Varsa bir *App.config* test projenizde mevcut dosya:

  - Açık *App.config* dosya projede ve yapılandırma düğümü altında aşağıdaki kodu ekleyin:

    ```xml
    <system.diagnostics>
      <switches>
        <add name="EqtTraceLevel" value="4" />
      </switches>
    </system.diagnostics>`
    ```

- Test kodu günlüğünü etkinleştir:

   ```csharp
   Microsoft.VisualStudio.TestTools.UITesting.PlaybackSettings.LoggerOverrideState = HtmlLoggerState.AllActionSnapshot;
   ```

## <a name="step-2-run-your-coded-ui-test-and-view-the-log"></a>2\. Adım: Kodlanmış UI testleri çalıştırmak ve günlüğünü görüntüleyin

Yapılan değişiklikler ile kodlanmış UI testi çalıştırdığınızda *QTAgent\*. exe.config* dosya, yerinde bağlantısını bir çıktı görmeniz **Test Gezgini** sonuçları. Günlük dosyalarını izleme düzeyini ayarlandığında değil yalnızca test de başarılı testlerde başarısız olduğunda oluşturulan **ayrıntılı**.

1. Üzerinde **Test** menüsünde seçin **Windows** seçip **Test Gezgini**.

2. Üzerinde **derleme** menüsünde seçin **Çözümü Derle**.

3. İçinde **Test Gezgini**, kodlanmış UI testi çalıştırmak için kısayol menüsünü açın ve ardından istediğiniz seçin **seçili Testleri Çalıştır**.

     Otomatikleştirilmiş testleri çalıştırın ve geçti veya başarısız olmadığını gösterir.

    > [!TIP]
    > Görüntülenecek **Test Gezgini**, seçin **Test** > **Windows**ve ardından **Test Gezgini**.

4. Seçin **çıkış** bağlantısını **Test Gezgini** sonuçları.

     ![Test Gezgininde çıkış bağlantı](../test/media/cuit_htmlactionlog1.png)

     Bu eylem günlüğü bağlantısını içeren test için çıktıyı görüntüler.

     ![Sonuçları ve kodlanmış UI testi çıkış bağlantıları](../test/media/cuit_htmlactionlog2.png)

5. Seçin *UITestActionLog.html* bağlantı.

     Günlük, web tarayıcınızda görüntülenir.

     ![Kodlanmış UI testi günlüğü dosyası](../test/media/cuit_htmlactionlog3.png)

## <a name="see-also"></a>Ayrıca bkz.

- [UI otomasyonunu kullanarak kodunuzu test etme](../test/use-ui-automation-to-test-your-code.md)
- [Nasıl yapılır: Microsoft Visual Studio'dan testler çalıştırma](https://msdn.microsoft.com/Library/1a1207a9-2a33-4a1e-a1e3-ddf0181b1046)
