---
title: -Upgrade (devenv.exe)
ms.date: 12/10/2018
ms.topic: reference
helpviewer_keywords:
- /upgrade Devenv switch
- Devenv, /upgrade switch
- upgrade Devenv switch
ms.assetid: 3468045c-5cc9-4157-9a9d-622452145d27
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f7ca13af8cd6b1a144ee3202165908f1d282ca81
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55924077"
---
# <a name="upgrade-devenvexe"></a>/Upgrade (devenv.exe)

Çözüm dosyasını ve tüm proje dosyalarından veya bu dosyalar için geçerli Visual Studio biçimlerinde belirtilen proje dosyasını güncelleştirir.

## <a name="syntax"></a>Sözdizimi

```shell
devenv {SolutionFile|ProjectFile} /Upgrade [/Out OutputFilename]
```

## <a name="arguments"></a>Arguments

- *SolutionFile*

  Tüm bir çözümü ve projelerini yükseltme yapıyorsanız, gerekli. Çözüm dosyasının adı ve yolu. Yalnızca çözüm dosyasının veya tam yol adı ve çözüm dosyasının adını girebilirsiniz. Adlandırılmış klasör veya dosya henüz yoksa, oluşturulur.

- *ProjectFile*

  Tek bir projeyi yükseltiyorsanız gereklidir. Çözüm içindeki bir proje dosyasının adı ve yolu. Yalnızca proje dosyasının veya tam yol adını ve proje dosyasının adını girebilirsiniz. Adlandırılmış klasör veya dosya henüz yoksa, oluşturulur.

- `/Out` *OutputFilename*

  İsteğe bağlı. Aracı göndermek istediğiniz bir dosya adı için çıkış. Dosya zaten varsa, aracı çıkış dosyasının sonuna ekler.

## <a name="remarks"></a>Açıklamalar

Yedeklemeleri otomatik olarak oluşturulur ve geçerli dizinde oluşturulan Backup adlı dizine kopyalanır.

Yükseltilebilmesi için önce kaynağı denetlenen çözümlerin veya projelerin kullanıma alınması gerekir.

Kullanarak `/Upgrade` anahtar, Visual Studio başlamıyor. Yükseltmenin sonuçları, çözüm veya projenin geliştirme dilinin yükseltme Raporu'nda görülebilir. Hiçbir hata veya kullanım bilgisi döndürülür. Visual Studio'da projelerini yükseltme hakkında daha fazla bilgi için bkz. [bağlantı noktası, geçirme ve yükseltme Visual Studio projeleri](../../porting/port-migrate-and-upgrade-visual-studio-projects.md).

## <a name="example"></a>Örnek

Bu örnekte, "MyProject.sln" adlı bir çözüm dosyasını yükseltir.

```shell
devenv "%USERPROFILE%\source\repos\MyProject\MyProject.sln" /upgrade
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)