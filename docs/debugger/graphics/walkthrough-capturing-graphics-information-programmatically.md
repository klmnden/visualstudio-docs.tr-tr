---
title: 'İzlenecek yol: Grafik bilgilerini programlama yoluyla yakalama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 187328e4ef4d1de0c865120400f84e65385160fc
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71252889"
---
# <a name="walkthrough-capturing-graphics-information-programmatically"></a>İzlenecek yol: Grafik Bilgilerini Program Aracılığıyla Yakalama
Direct3D uygulamasından grafik [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] bilgilerini programlı bir şekilde yakalamak için grafik tanılama kullanabilirsiniz.

Programlı yakalama, gibi senaryolarda faydalıdır:

- Grafik uygulamanız, bir dokusunu oluştururken olduğu gibi swapzincirini kullanmazsa programlı olarak yakalamayı başlatın.

- Uygulamanız, hesaplamalar gerçekleştirmek için DirectCompute kullandığında olduğu gibi, uygulama hiç işlenmezse, programlı olarak yakalamayı başlatın.

- Bir işleme sorunu, el ile test sırasında tahmin etmek ve yakalamak zor olduğunda,ancakçalışmazamanındauygulamanındurumuhakkındabilgilerkullanılarakprogramlıbirşekildetahminedilebilir.`CaptureCurrentFrame`

## <a name="CaptureDX11_2"></a>Windows 10 ' da programlı yakalama
Bu izlenecek yolda, güçlü yakalama yöntemini kullanan Windows 10 ' da DirectX 11,2 API kullanan uygulamalarda Programlı yakalama gösterilmektedir.

Bu bölümde bu görevlerin nasıl yapılacağı gösterilmektedir:

- Uygulamanızı programlı yakalama kullanacak şekilde hazırlama

- IDXGraphicsAnalysis arabirimini alma

- Graf bilgilerini yakalama

> [!NOTE]
> Programlı yakalama 'nın önceki uygulamaları, Yakalama işlevselliği sağlamak için [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] için Visual Studio için uzak Araçlar güvendi.

### <a name="preparing-your-app-to-use-programmatic-capture"></a>Uygulamanızı programlı yakalama kullanacak şekilde hazırlama
Uygulamanızda Programlı yakalama 'yı kullanmak için gereken üst bilgileri içermesi gerekir. Bu üstbilgiler Windows 10 SDK 'sının bir parçasıdır.

##### <a name="to-include-programmatic-capture-headers"></a>Programlı yakalama üstbilgilerini dahil etmek için

- Bu üst bilgileri IDXGraphicsAnalysis arabirimini tanımlayabileceğiniz kaynak dosyasına ekleyin:

    ```cpp
    #include <DXGItype.h>
    #include <dxgi1_2.h>
    #include <dxgi1_3.h>
    #include <DXProgrammableCapture.h>
    ```

    > [!IMPORTANT]
    > Windows 10 uygulamalarınızda Programlı yakalama gerçekleştirmek için Windows 8,0 ve önceki sürümlerde Programlı yakalamayı destekleyen vsgcapture. h başlık dosyasını eklemeyin. Bu üstbilgi DirectX 11,2 ile uyumsuzdur. Bu dosya d3d11_2. h üst bilgisi eklendikten sonra varsa, derleyici bir uyarı verir. Vsgcapture. h, d3d11_2. h öncesinde varsa, uygulama başlatılmaz.

    > [!NOTE]
    > Makinenizde Haziran 2010 DirectX SDK 'sı yüklüyse ve projenizin içerme yolu içeriyorsa `%DXSDK_DIR%includex86`, bunu ekleme yolunun sonuna taşıyın. Kitaplık yolunuzda aynısını yapın.

### <a name="getting-the-idxgraphicsanalysis-interface"></a>IDXGraphicsAnalysis arabirimini alma
DirectX 11,2 ' den grafik bilgilerini yakalamadan önce DXGI hata ayıklama arabirimini almanız gerekir.

> [!IMPORTANT]
> Programlı yakalama kullanırken, uygulamanızı hala grafik tanılama (alt + F5 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]) altında veya [komut satırı yakalama aracı](command-line-capture-tool.md)altında çalıştırmanız gerekir.

##### <a name="to-get-the-idxgraphicsanalysis-interface"></a>IDXGraphicsAnalysis arabirimini almak için

- DXGI hata ayıklama arabirimine IDXGraphicsAnalysis arabirimini bağlamak için aşağıdaki kodu kullanın.

  ```cpp
  IDXGraphicsAnalysis* pGraphicsAnalysis;
  HRESULT getAnalysis = DXGIGetDebugInterface1(0, __uuidof(pGraphicsAnalysis), reinterpret_cast<void**>(&pGraphicsAnalysis));
  ```

  Kullanmadan önce geçerli bir arabirim `HRESULT` aldığınızdan emin olmak için [DXGIGetDebugInterface1](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1) tarafından döndürülen ' i kontrol ettiğinizden emin olun:

  ```cpp
  if (FAILED(getAnalysis))
  {
      // Abort program or disable programmatic capture in your app.
  }
  ```

  > [!NOTE]
  > ( `DXGIGetDebugInterface1` `E_NOINTERFACE` [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]) Döndürürse, uygulamanın grafik tanılama (alt + F5) altında çalıştığından emin olun.`error: E_NOINTERFACE No such interface supported`

### <a name="capturing-graphics-information"></a>Graf bilgilerini yakalama
Artık geçerli `IDXGraphicsAnalysis` bir arabiriminiz olduğuna göre, grafik bilgilerini yakalamak için `EndCapture` ve kullanabilirsiniz `BeginCapture` .

##### <a name="to-capture-graphics-information"></a>Grafik bilgilerini yakalamak için

- Grafik bilgilerini yakalamaya başlamak için şunu kullanın `BeginCapture`:

    ```cpp
    ...
    pGraphicsAnalysis->BeginCapture();
    ...
    ```

    Yakalama çağrıldığında hemen `BeginCapture` başlar; sonraki çerçevenin başlamasını beklemez. Yakalama, geçerli çerçeve sunulduktan sonra ya da çağırdığınızda `EndCapture`:

    ```cpp
    ...
    pGraphicsAnalysis->EndCapture();
    ...
    ```

- Çağrısından `EndCapture`sonra grafik nesnesini serbest bırakın.

## <a name="next-steps"></a>Sonraki Adımlar
Bu kılavuzda grafik bilgilerinin programlı bir şekilde nasıl yakalanacağı gösterilmiştir. Sonraki adım olarak bu seçeneği göz önünde bulundurun:

- Grafik Tanılama araçlarını kullanarak yakalanan grafik bilgilerini çözümlemeyi öğrenin. Bkz. [genel bakış](overview-of-visual-studio-graphics-diagnostics.md).

## <a name="see-also"></a>Ayrıca Bkz.
- [İzlenecek yol: Grafik Bilgilerini Yakalama](walkthrough-capturing-graphics-information.md)
- [Grafik Bilgilerini Yakalama](capturing-graphics-information.md)
- [Komut satırı Yakalama Aracı](command-line-capture-tool.md)
