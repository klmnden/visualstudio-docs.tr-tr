---
title: VSPackage geliştirme için Devenv komut satırı anahtarları | Microsoft Docs
ms.date: 12/10/2018
ms.topic: conceptual
helpviewer_keywords:
- /Setup command line switch
- /ResetSkipPkgs command line switch
- /RootSuffix command line switch
- /SafeMode command line switch
- /Splash command line switch
- command-line switches
- registry, Visual Studio SDK
- command line, switches
- Visual Studio SDK, command-line switches
ms.assetid: d65d2c04-dd84-42b0-b956-555b11f5a645
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: dd95fe31949b51c7167337ad21c51251e84a19a7
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56705537"
---
# <a name="devenv-command-line-switches-for-vspackage-development"></a>VSPackage geliştirme için Devenv komut satırı anahtarları

Visual Studio geliştiriciler yürütülürken komut satırından görevlerini otomatikleştirmek tanır `devenv.exe`, Visual Studio IDE başlatıldığında dosya.

 Görevler aşağıdakileri içerir:

- IDE dışında tasarlanmış yapılandırmalardan uygulamalarda dağıtılıyor.

- Otomatik olarak önayarını kullanarak proje oluşturma, derleme ayarları veya hata ayıklama yapılandırması.

- IDE dışında tüm gelen belirli yapılandırmalar, IDE'de yükleniyor. IDE başlatma sonrasında de özelleştirebilirsiniz.

## <a name="guidelines-for-switches"></a>Anahtarlar için yönergeler

Visual Studio belgeleri açıklayan kullanıcı düzeyi `devenv` komut satırı anahtarları. Daha fazla bilgi için [Devenv komut satırı anahtarları](../ide/reference/devenv-command-line-switches.md). `devenv` Aracı VSPackage geliştirme, dağıtım ve hata ayıklama için yararlı olan ek komut satırı anahtarları da destekler.

| Komut satırı anahtarı | Açıklama |
|---------------------| - |
| `/ResetSkipPkgs` | Sorunlu VSPackage yükleme engellemek istiyorsanız, sonra Visual Studio başlatılır kullanıcılar tarafından eklenen tüm Atla yükleme seçenekleri temizler. SkipLoading etiketinin varlığını VSPackage yüklenmesini devre dışı bırakır. Etiket temizleme VSPackage yükleme yeniden etkinleştirir.<br /><br /> Bu anahtar hiçbir bağımsız değişkeni alır. |
| `/RootSuffix` | Visual Studio, alternatif bir konuma kullanarak başlatır. Visual Studio SDK'sı yükleyicisi tarafından oluşturulan kısayol olarak aşağıdaki komutu çalıştırın:<br /><br /> `devenv /RootSuffix exp`<br /><br /> Bu durumda, `exp` belirli bir sonek konumuyla tanımlar (örneğin, `10.0Exp` yerine `10.0`). Deneysel örneği ayrı ayrı kod yazmak için kullandığınız Visual Studio'nun örneğinden VSPackage hatalarını ayıklamanızı sağlar.<br /><br /> Bu anahtar VSRegEx.exe kullanarak oluşturduğunuz bir konumu tanımlayan bir dize alabilir. Daha fazla bilgi için [deneysel örneğinde](../extensibility/the-experimental-instance.md). |
| `/SafeMode` | Visual Studio, yalnızca varsayılan IDE ve servisler yüklenirken güvenli modda başlatır. `/SafeMode` Anahtarı tüm üçüncü taraf VSPackages kararlı yürütme sağlayarak Visual Studio başladığında yüklenmesini engeller.<br /><br /> Bu anahtar hiçbir bağımsız değişkeni alır. |
| `/Setup` | Menüleri, araç çubukları ve tüm kullanılabilir VSPackages komut gruplarından tanımlayan kaynak meta verileri birleştirmek için Visual Studio zorlar. Bu gibi durumlarda, bu komut yalnızca bir yönetici olarak çalıştırabilirsiniz. <br /><br /> Bu anahtar hiçbir bağımsız değişkeni alır. `devenv /Setup` Komut genellikle yükleme işleminin son adımı verilir. Kullanım `/Setup` anahtar IDE başlamıyor.|
| `/Splash` | Visual Studio Karşılama ekranında, her zamanki şekilde ve ana IDE göstermeden önce sonra gösterir bir ileti kutusu gösterir. İleti kutusu, çalışma ekranı (örneğin, bir VSPackage ürün simgesi denetlemek için) sağlar.<br /><br /> Bu anahtar hiçbir bağımsız değişkeni alır. |

## <a name="see-also"></a>Ayrıca bkz.

- [Komut satırı anahtarları ekleme](../extensibility/adding-command-line-switches.md)
- [Devenv komut satırı anahtarları](../ide/reference/devenv-command-line-switches.md)