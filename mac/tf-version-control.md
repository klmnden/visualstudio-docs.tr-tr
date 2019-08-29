---
title: Team Foundation Sürüm Denetimi (TFVC)
description: Team Foundation Sürüm Denetimi (TFVC) ile Mac için Visual Studio Team Foundation Server/Azure DevOps 'a bağlanma.
author: jmatthiesen
ms.author: jomatthi
ms.date: 06/25/2019
ms.technology: vs-ide-general
ms.assetid: 52D3D26A-4D01-4FD1-AAA1-AE7D7BD39746
ms.openlocfilehash: 4d0de2b9d91458a4baa7d0ed6498fbc7f65b2fb1
ms.sourcegitcommit: cf8c0fef2b9690595e99ce3802586cdd55fd37c2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70108084"
---
# <a name="connecting-to-team-foundation-version-control"></a>Team Foundation Sürüm Denetimi bağlanılıyor

> [!NOTE]
> MacOS üzerinde en iyi sürüm denetimi deneyimi için Team Foundation Sürüm Denetimi (TFVC) yerine git kullanmanız önerilir. Git Mac için Visual Studio desteklenir ve Team Foundation Server (TFS)/Azure DevOps içinde barındırılan depolar için varsayılan seçenektir. Git 'i TFS/Azure DevOps ile kullanma hakkında daha fazla bilgi edinmek için [Git deposu ayarlama](/visualstudio/mac/set-up-git-repository) makalesini inceleyin.
> 
> Mac için Visual Studio için TFVC uzantısının önizleme sürümünü daha önce kullandıysanız, artık Mac için Visual Studio 2019 ' de desteklenmemektedir.

Azure Repos sürüm denetimi için iki model sağlar: Bir merkezi sürüm denetim sistemi olan [Git](/azure/devops/repos/git/?view=azure-devops), dağıtılmış sürüm denetim sistemi ve [Team Foundation sürüm denetimi](/azure/devops/repos/tfvc/index?view=azure-devops) (TFVC).

Mac için Visual Studio, git depoları için tam destek sağlar, ancak TFVC ile çalışmak için bazı geçici çözümler gerektirir. Sürüm denetimi için TFVC 'yi bugün kullanıyorsanız, TFVC 'de barındırılan kaynak kodunuza erişmek için kullanabileceğiniz bazı çözümler aşağıda verilmiştir:

* [Grafik Kullanıcı arabirimi için Visual Studio Code ve Azure Repos uzantısını kullanın](#use-visual-studio-code-and-the-azure-repos-extension)
* [Team Explorer Everywhere komut satırı Istemcisini (t-CLC) kullanarak depoya bağlanma](#connecting-using-the-team-explorer-everywhere-command-line-client)

Bu makalenin geri kalanında yukarıda listelenen seçeneklere adım adım yol gösterilir.

## <a name="requirements"></a>Gereksinimler

* Mac için Visual Studio Community, Professional veya Enterprise sürüm 7,8 ve üzeri.
* Azure DevOps Services, Team Foundation Server 2013 ve üzeri ya da 2018 ve üzeri Azure DevOps Server.
* Azure DevOps Services veya Team Foundation Server/Azure DevOps Server bir proje Team Foundation Sürüm Denetimi kullanacak şekilde yapılandırıldı.

## <a name="use-visual-studio-code-and-the-azure-repos-extension"></a>Visual Studio Code ve Azure Repos uzantısını kullanın

Sürüm denetimindeki dosyalarınızı yönetmek için bir grafik arabirimle çalışmak isterseniz, Visual Studio Code için Azure Repos uzantısı Microsoft tarafından desteklenen bir çözüm sağlar. Başlamak için [Visual Studio Code](https://code.visualstudio.com) indirin ve [Azure Repos uzantısının nasıl yapılandırılacağını](https://marketplace.visualstudio.com/items?itemName=ms-vsts.team)öğrenin.

## <a name="connecting-using-the-team-explorer-everywhere-command-line-client"></a>Team Explorer Everywhere komut satırı Istemcisini kullanarak bağlanma

MacOS terminalini rahat kullanıyorsanız, Team Explorer Everywhere komut satırı Istemcisi (t-CLC), TFVC 'de kaynağınıza bağlanmak için desteklenen bir yol sağlar.

TFVC bağlantısını kurmak ve değişiklikleri kaydetmek için aşağıdaki adımları izleyebilirsiniz.

### <a name="setting-up-the-tee-clc"></a>T-CLC ayarlanıyor

T-CLC ile kurulum almanın iki yolu vardır.

* İstemcisini yüklemek için homebrew kullanın veya
* İstemciyi indirip el ile yükleme

En kolay çözüm, macOS için bir paket yöneticisi olan **HomeBrew**' ı kullanmaktır. Bu yöntemi kullanarak yüklemek için:

1. MacOS Terminal uygulamasını başlatın.
1. Terminal ve [homebrew giriş sayfasındaki](https://brew.sh/)yönergeleri kullanarak Homebrew 'ı yükler.
1. Homebrew yüklendikten sonra Terminalinizden aşağıdaki komutu çalıştırın:`brew install tee-clc`

**T-CLC ' i el ile ayarlamak**için:

1. Team Explorer Everywhere GitHub deposunun yayınlar sayfasından [t-CLC ' nin en son sürümünü indirin](https://github.com/Microsoft/team-explorer-everywhere/releases) (örneğin, tee-CLC-14.134.0. zip bu yazma sırasında).
1. . Zip içeriğini diskteki bir klasöre ayıklayın.
1. MacOS Terminal uygulamasını açın ve önceki adımda kullandığınız `cd` klasöre geçmek için komutunu kullanın.
1. Klasörü içinden komut satırı istemcisinin çalıştıracağınızı sınamak `./tf` için komutunu çalıştırın, Java veya başka bağımlılıklar yüklemek isteyip istemediğiniz sorulur.

T-CLC yüklendikten sonra, istemcinin lisans sözleşmesini görüntülemek ve kabul etmek `tf eula` için komutunu çalıştırabilirsiniz.

Son olarak, TFS/Azure DevOps ortamınızdan kimlik doğrulamak için sunucuda bir kişisel erişim belirteci oluşturmanız gerekir. [Kişisel erişim belirteçleriyle kimlik doğrulama](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/pats?view=azure-devops)hakkında daha fazla bilgi edinin. TFVC ile kullanmak için bir kişisel erişim belirteci oluştururken, belirteci yapılandırırken tam erişim sağladığınızdan emin olun.

### <a name="using-the-tee-clc-to-connect-to-your-repo"></a>Depoya bağlanmak için t-CLC kullanma

Kaynak kodunuza bağlanmak için, önce `tf workspace` komutunu kullanarak bir çalışma alanı oluşturmanız gerekir. Örneğin, aşağıdaki komutlar "Myorganleştirme" adlı Azure DevOps Services bir kuruluşa bağlanır: 

```bash
export TF_AUTO_SAVE_CREDENTIALS=1
tf workspace -new MyWorkspace -collection:https://dev.azure.com/MyOrganization
```

`TF_AUTO_SAVE_CREDENTIALS` Ortam ayarı, kimlik bilgilerinizi birden çok kez girmeniz istenmeyecek şekilde kaydetmek için kullanılır. Bir Kullanıcı adı sorulduğunda, önceki bölümde oluşturduğunuz kişisel erişim belirtecini kullanın ve boş bir parola kullanın.

Kaynak dosyalarınızın bir yerel klasöre eşlenmesini oluşturmak için `tf workfold` komutunu kullanırsınız. Aşağıdaki örnekte "WebApp. Services" adlı bir klasör "MyRepository" TFVC projesinden eşlenir ve yerel ~/Projects/klasörüne (yani geçerli kullanıcıların giriş klasöründeki "projeler" klasörü) kopyalanmak üzere ayarlanır.

```bash
tf workfold -map $/MyRepository/WebApp.Services -workspace:MyWorkspace ~/Projects/
```

Son olarak, kaynak dosyaları sunucudan almak ve yerel olarak kopyalamak için aşağıdaki komutu kullanın:

```bash
tf get
```

### <a name="committing-changes-using-the-tee-clc"></a>T-CLC kullanarak değişiklikler yürütülüyor

Mac için Visual Studio dosyalarınızda değişiklikler yaptıktan sonra, düzenlemelerinizi denetlemek için terminale geri dönebilirsiniz. Komut, iade edilecek bekleyen değişiklikler listesine dosya eklemek için kullanılır `tf checkin` ve komut sunucuda gerçek iade işlemini gerçekleştirir. `tf add` Komut `checkin` , bir yorum eklemek veya ilgili bir iş öğesini ilişkilendirmek için parametreler içerir. Aşağıdaki kod parçacığında, bir `WebApp.Services` klasördeki tüm dosyalar, iade etme için yinelemeli olarak eklenir. Ardından, kod bir yorum ile iade edilir ve "42" KIMLIĞINE sahip bir iş öğesiyle ilişkilendirilir.

```bash
cd WebApp.Services
tf add * /recursive
tf checkin -comment:"Replaced 'Northwand' typos with the correct word Northwind" -associate:42
```

Burada bahsedilen komutlar veya diğerleri hakkında daha fazla bilgi edinmek için terminalde aşağıdaki komutu kullanabilirsiniz:

`tf help`

### <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio kullanarak (Windows 'da) kodunuzu TFVC 'de geliştirme ve paylaşma](/azure/devops/repos/tfvc/share-your-code-in-tfvc-vs)