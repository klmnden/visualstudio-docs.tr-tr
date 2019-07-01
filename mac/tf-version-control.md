---
title: Team Foundation sürüm denetimi (TFVC)
description: Mac için Visual Studio Team Foundation sürüm denetimi (TFVC) ile Team Foundation Server/Azure DevOps bağlanıyor.
author: conceptdev
ms.author: crdun
ms.date: 06/25/2019
ms.topic: article
ms.technology: vs-ide-general
ms.assetid: 52D3D26A-4D01-4FD1-AAA1-AE7D7BD39746
ms.openlocfilehash: 04a251621af1086c15bafa15b7a9fe01f8dab5a8
ms.sourcegitcommit: 9d3529e40438ca45dcb0b31742c4cd5a89daa61e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/26/2019
ms.locfileid: "67398976"
---
# <a name="connecting-to-team-foundation-version-control"></a>Team Foundation sürüm denetimine bağlama

> [!NOTE]
> MacOS en iyi sürüm denetim deneyimi için Git, Team Foundation sürüm denetimi (TFVC) yerine kullanılmasını öneririz. Git Mac için Visual Studio'da desteklendiği ve Team Foundation Server (TFS) barındırılan depolar için varsayılan seçenek / Azure DevOps. Git, TFS/Azure DevOps ile kullanma hakkında daha fazla bilgi edinmek için [bir Git deposu ayarlama](/visualstudio/mac/set-up-git-repository) makalesi.
> 
> Daha önce TFVC uzantı Önizleme sürümü için Visual Studio Mac için kullandıysanız, Mac için Visual Studio 2019 içinde artık desteklenir

Azure depoları, sürüm denetimi, iki modeli sağlar: [Git](/azure/devops/repos/git/?view=azure-devops), bir dağıtılmış sürüm denetim sistemini ve [Team Foundation sürüm denetimi](/azure/devops/repos/tfvc/index?view=azure-devops) (TFVC) merkezi sürüm denetimi sistemi.

Mac için Visual Studio, Git depoları için tam destek sağlar, ancak TFVC ile çalışmak için bazı geçici çözümler gerektirir. Bugün sürüm denetimi için TFVC kullanıyorsanız, kaynak kodunuzu TFVC'de barındırılan erişmek için kullanabileceğiniz bazı çözümler aşağıda verilmiştir:

* [Visual Studio Code ve Azure depoları uzantısı için bir grafik kullanıcı Arabirimi kullanın.](#use-visual-studio-code-and-the-azure-repos-extension)
* [Team Explorer Everywhere komut satırı istemcisini (CLC TEE) kullanarak deponuza bağlanma](#connecting-using-the-team-explorer-everywhere-command-line-client)

Bu makalenin geri kalanında, yukarıda listelenen seçenekler açıklanmaktadır.

## <a name="requirements"></a>Gereksinimler

* Visual Studio Community, Professional veya Mac 7,8 ve sonraki sürümleri için Enterprise.
* Azure DevOps Hizmetleri, Team Foundation Server 2013 ve üzeri ya da Azure DevOps sunucu 2018 ve üzeri.
* Azure DevOps Services veya Team Foundation Server/Azure DevOps Team Foundation sürüm denetimi kullanmak üzere yapılandırılmış sunucusu, bir proje.

## <a name="use-visual-studio-code-and-the-azure-repos-extension"></a>Visual Studio Code ve Azure depoları uzantısını kullanma

Sürüm denetiminde dosyalarınızı yönetmek için bir grafik arabirim çalışmak istiyorsanız, Visual Studio Code için Azure depoları uzantısı Microsoft tarafından desteklenen bir çözüm sağlar. Başlamak için Yükle [Visual Studio Code](https://code.visualstudio.com) ve daha sonra öğrenin nasıl [Azure depoları uzantısını yapılandırmak](https://marketplace.visualstudio.com/items?itemName=ms-vsts.team).

## <a name="connecting-using-the-team-explorer-everywhere-command-line-client"></a>Team Explorer Everywhere komut satırı istemcisini kullanarak bağlanma

MacOS Terminal, ardından Team Explorer Everywhere komut satırı istemcisini kullanarak hakimseniz (TEE CLC) TFVC kaynak bağlanmak için desteklenen bir yol sağlar.

TFVC ve değişiklikleri bağlantınızı kurmak için aşağıdaki adımları izleyebilirsiniz.

### <a name="setting-up-the-tee-clc"></a>TEE CLC ayarlama

TEE CLC kuruluma almanın iki yolu vardır.

* İstemcisini yüklemek için Homebrew kullanın veya
* İstemcisini indirme ve el ile yükleme

En kolay çözümdür **HomeBrew kullanarak**, macOS için Paket Yöneticisi olan. Bu yöntemi kullanarak yüklemek için:

1. MacOS Terminal uygulamasını başlatın.
1. Terminal ve yönergeleri kullanarak Homebrew yükleme [Homebrew giriş sayfası](https://brew.sh/).
1. Homebrew yüklendikten sonra terminalde aşağıdaki komutu çalıştırın: `brew install tee-clc`

İçin **TEE CLC el ile Kurulum**:

1. [Tee clc en son sürümünü indirin](https://github.com/Microsoft/team-explorer-everywhere/releases) sürümleri sayfasından Team Explorer Everywhere GitHub deposunun (örn: t-clc-14.134.0.zip bu makalenin yazıldığı sırada).
1. Diskteki bir klasöre .zip içeriğini ayıklayın.
1. MacOS Terminal uygulamasını açın ve kullanmak `cd` önceki adımda kullanılan klasöre değiştirmek için komutu.
1. Klasör içinde çalıştırılan komut `./tf` komut satırı istemci çalıştırabileceğiniz test etmek için Java veya diğer bağımlılıkları yüklemeniz istenebilir.

TEE CLC yüklendikten sonra komutu çalıştırabilirsiniz `tf eula` görüntülemek ve istemcisi için lisans sözleşmesini kabul edin.

Son olarak, TFS/Azure DevOps ortamınız ile kimlik doğrulamak için sunucuda bir kişisel erişim belirteci oluşturma gerekecektir. Daha fazla bilgi edinin [kişisel erişim belirteçleri ile kimlik doğrulaması](https://docs.microsoft.com/azure/devops/integrate/get-started/authentication/pats?view=azure-devops). TFVC ile kullanmak için kişisel erişim belirteci oluştururken, belirteç yapılandırırken tam erişim sağlamak üzere emin olun.

### <a name="using-the-tee-clc-to-connect-to-your-repo"></a>TEE CLC kullanarak deponuza bağlanma

Kaynak kodunuzu bağlanmak için önce kullanarak bir çalışma alanı oluşturmak için ihtiyacınız `tf workspace` komutu. Örneğin, aşağıdaki komutları bir kuruluşta Azure DevOps "MyOrganization" olarak adlandırılan hizmetleri bağlanın: 

```bash
export TF_AUTO_SAVE_CREDENTIALS=1
tf workspace -new MyWorkspace -collection:https://dev.azure.com/MyOrganization
```

`TF_AUTO_SAVE_CREDENTIALS` Ortam ayarını, bunları birden çok kez girmeniz istenmez böylece kimlik bilgilerinizi kaydetmek için kullanılır. Bir kullanıcı adı için istendiğinde, önceki bölümde oluşturduğunuz kişisel erişim belirteci kullanın ve boş bir parola kullanın.

Kaynak dosyalarını yerel bir klasöre ilişkin bir eşleme oluşturmak için kullanacağınız `tf workfold` komutu. Aşağıdaki örnek "MyRepository" TFVC gelen "WebApp.Services" adlı bir klasör eşler proje ve yerel ~/Projects/ klasörüne (yani "Projeler" klasöründeki bir klasörün geçerli kullanıcı giriş) kopyalanacak ayarlayın.

```bash
tf workfold -map $/MyRepository/WebApp.Services -workspace:MyWorkspace ~/Projects/
```

Son olarak, kaynak dosyaları sunucudan almak ve yerel olarak kopyalamak için aşağıdaki komutu kullanın:

```bash
tf get
```

### <a name="committing-changes-using-the-tee-clc"></a>TEE CLC kullanarak değişiklikler işleniyor

Mac için Visual Studio dosyalarında değişiklik yaptıktan sonra yaptığınız düzenlemeleri denetlemek için Terminal geri dönebilirsiniz. `tf add` Komut dosyaları bekleyen değişiklikler iade edilecek listesine eklemek için kullanılır ve `tf checkin` gerçek iade sunucuya komutu gerçekleştirir. `checkin` Komut yorum ekleyebilir ya da bir ilgili iş öğesini ilişkilendirmek için parametreleri içerir. Aşağıdaki kod parçacığında, tüm dosyaları bir `WebApp.Services` klasör eklenir, yinelemeli olarak iade etme için. Ardından, kod bir yorum ile işaretli ve "42" Kimliğine sahip bir iş öğesi ile ilişkilendirilmiş.

```bash
cd WebApp.Services
tf add * /recursive
tf checkin -comment:"Replaced 'Northwand' typos with the correct word Northwind" -associate:42
```

Burada belirtilen komutları veya diğerleri hakkında daha fazla bilgi için terminalde aşağıdaki komutu kullanabilirsiniz:

`tf help`

### <a name="see-also"></a>Ayrıca bkz.

- [Geliştirin ve kodunuzu Visual Studio (Windows üzerinde) kullanarak tfvc'de paylaşma](/azure/devops/repos/tfvc/share-your-code-in-tfvc-vs)