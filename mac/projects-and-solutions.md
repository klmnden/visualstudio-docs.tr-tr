---
title: Projeler ve Çözümler
description: Bu belge, Mac için projeler ve çözümler Visual Studio'da genel bir bakış sağlar
author: heiligerdankgesang
ms.author: dominicn
ms.date: 05/23/2019
ms.assetid: 8254505D-D96E-48BD-8A5E-CF6A917897EA
ms.openlocfilehash: b66a1dfbe0569c501d05b34425e198f1501438ca
ms.sourcegitcommit: 7fbfb2a1d43ce72545096c635df2b04496b0be71
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/09/2019
ms.locfileid: "67691282"
---
# <a name="projects-and-solutions-in-visual-studio-for-mac"></a>Projeler ve çözümler Mac için Visual Studio

Bu makalede bir bakış sunulmaktadır *proje* ve *çözüm* Mac için Visual Studio'da kavramları

> [!NOTE] 
> Bu konu, Mac için Visual Studio için geçerlidir. Windows üzerinde Visual Studio için bkz: [projeler ve çözümler Visual Studio'da](/visualstudio/ide/solutions-and-projects-in-visual-studio).

## <a name="projects"></a>Projeler

Yeni uygulama, Web sitesi, vb. Mac için Visual Studio'da oluştururken, bir proje başlatın. Proje, yürütülebilir dosya, kitaplık veya Web sitesi derlemek için gerekli olan gerekli tüm dosyaları (kaynak kodu, resimler, veri dosyaları, vb.) içeriyor.

Bir proje dosyası tarafından tanımlanır (örneğin, `.csproj` için C# projeler) dosyaları ve derleme ayarları gibi projeye özgü ayarları için dosya ve klasör hiyerarşisi, yolları tanımlayan xml içeriyor.

Bir proje, Mac için Visual Studio tarafından yüklendiğinde çözüm panelinde klasör ve dosyaları projenizde görüntülemek için proje dosyasını kullanır. Derleme sırasında MSBuild yürütülebilir dosyayı oluşturmak için proje dosyasından ayarlarını okur.

## <a name="solutions"></a>Çözümler

A *çözüm* ilgili daha fazla proje ya da bu grupları birlikte bir kapsayıcıdır. Çözüm bir metin dosyası tarafından açıklanan (uzantı `.sln`) kendi benzersiz biçimde; bunu el ile düzenlenmesi kullanılmaya yönelik değildir.

## <a name="managing-projects-in-the-solution-pad"></a>Çözüm panelinde projeleri yönetme

Bir proje oluşturulacak veya yüklenecek sonra çözüm bölmesi, proje veya çözüm ve içerdiği dosyaları görüntülemek ve yönetmek için kullanabilirsiniz. Aşağıdaki çizimde, iki proje içeren bir .NET Core çözümü ile çözüm bölmesi gösterir:

![Örnek çözüm birden çok proje ile](media/solution-example.png)

Proje veya çözüm adına çift tıklayarak veya sağ tıklayıp seçme hem proje ve çözüm özelliklerini yönetme **seçenekleri**.

Bu seçenekler hakkında daha fazla bilgi sağlanır [yönetme çözüm ve proje özelliklerini](managing-solutions-and-project-properties.md) makalesi.

## <a name="see-also"></a>Ayrıca bkz.

- [Çözümler ve projeler Visual Studio'da (Windows)](/visualstudio/ide/solutions-and-projects-in-visual-studio)
