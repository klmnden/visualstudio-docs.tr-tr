---
title: Projeler ve Çözümler
description: Bu belge Mac için Visual Studio içindeki projelere ve çözümlere genel bir bakış sağlar.
ms.topic: overview
author: heiligerdankgesang
ms.author: dominicn
ms.date: 05/23/2019
ms.assetid: 8254505D-D96E-48BD-8A5E-CF6A917897EA
ms.openlocfilehash: 92e7a47f7ea2b931c0b923d10e115843d315d024
ms.sourcegitcommit: cf8c0fef2b9690595e99ce3802586cdd55fd37c2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70107815"
---
# <a name="projects-and-solutions-in-visual-studio-for-mac"></a>Mac için Visual Studio projeler ve çözümler

Bu makalede, Mac için Visual Studio *Proje* ve *çözüm* kavramlarıyla bir genel bakış sunulmaktadır.

> [!NOTE] 
> Bu konu Mac için Visual Studio için geçerlidir. Windows üzerinde Visual Studio için bkz. [Visual Studio 'Da projeler ve çözümler](/visualstudio/ide/solutions-and-projects-in-visual-studio).

## <a name="projects"></a>Projeler

Mac için Visual Studio yeni bir uygulama, Web sitesi, vb. oluştururken bir proje ile başlar. Proje çalıştırılabilir, kitaplık veya Web sitesini derlemek için gereken tüm dosyaları (kaynak kodu, görüntüler, veri dosyaları vb.) içerir.

Proje, dosya ve klasör hiyerarşisini tanımlayan XML içeren bir dosya `.csproj` ( C# Örneğin, projeler için), dosya yolları ve derleme ayarları gibi projeye özel ayarlar tarafından tanımlanır.

Mac için Visual Studio tarafından bir proje yüklendiğinde Çözüm Bölmesi, projenizdeki dosyaları ve klasörleri göstermek için proje dosyasını kullanır. Derleme sırasında MSBuild, çalıştırılabilir dosyayı oluşturmak için proje dosyasındaki ayarları okur.

## <a name="solutions"></a>Çözümler

Bir *çözüm* , bir veya daha fazla ilgili projeyi birlikte gruplandıran bir kapsayıcıdır. Çözümler, kendi benzersiz biçimiyle bir metin dosyası ( `.sln`uzantı) tarafından tanımlanır; el ile düzenlenmesi amaçlanmamıştır.

## <a name="managing-projects-in-the-solution-pad"></a>Çözüm Bölmesi projeleri yönetme

Proje oluşturulduktan veya yüklendikten sonra proje veya çözümü ve içinde bulunan dosyaları görüntülemek ve yönetmek için Çözüm Bölmesi kullanabilirsiniz. Aşağıdaki çizimde, iki proje içeren bir .NET Core çözümüne sahip Çözüm Bölmesi gösterilmektedir:

![Birden çok projeyle örnek çözüm](media/solution-example.png)

Proje veya çözüm adına çift tıklayarak ya da sağ tıklayıp **Seçenekler**' i seçerek hem projelerin hem de çözümlerin özelliklerini yönetebilirsiniz.

Bu seçenekler hakkında daha fazla bilgi, [çözümleri ve proje özelliklerini yönetme](managing-solutions-and-project-properties.md) makalesinde sunulmaktadır.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio 'da çözümler ve projeler (Windows)](/visualstudio/ide/solutions-and-projects-in-visual-studio)
