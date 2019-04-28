---
title: Test aracılarını ve test denetleyicilerini yükleme
ms.date: 04/17/2019
ms.topic: conceptual
helpviewer_keywords:
- configure test agents, test lab
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c6597c47fd272beec2c82f7d4c2644291b168b5f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62965421"
---
# <a name="install-test-agents-and-test-controllers"></a>Test aracılarını ve test denetleyicilerini yükleme

Visual Studio ve Azure Test planları veya Team Foundation Server (TFS) test senaryoları için bir test denetleyicisine ihtiyacınız yoktur. Visual Studio için Agents Azure Test planları veya TFS ile iletişim kurarak düzenleme işleyin. Bir senaryo, derleme için sürekli testleri çalıştırın ve Azure Test planları veya TFS akışlarında yayın olabilir.

Kullanmak daha faydalı olup olmadığını düşünebilirsiniz [derleme veya sürüm Yönetimi](use-build-or-rm-instead-of-lab-management.md) Laboratuvar Yönetimi yerine.

## <a name="system-requirements"></a>Sistem gereksinimleri

Visual Studio test aracısı veya test denetleyicisi yüklemek için sistem gereksinimleri aşağıdaki tabloda gösterilmiştir:

| Öğe | Gereksinimler |
| ---- | ------------ |
| **Aracı** | Windows 10<br />Windows 8, Windows 8.1<br />Windows 7 Service Pack 1<br />Windows Server 2016 Standard ve Datacenter<br />Windows Server 2012 R2 |
| **Denetleyici** | Windows 10<br />Windows 8, Windows 8.1<br />Windows 7 Service Pack 1<br />Windows Server 2016 Standard ve Datacenter<br />Windows Server 2012 R2 |
| **.NET Framework** | .NET Framework 4.5 |

## <a name="install-the-test-controller-and-test-agents"></a>Test denetleyicisi ve test aracılarını yükleme

Visual Studio için agents indirebileceğiniz [visualstudio.microsoft.com](https://visualstudio.microsoft.com/downloads/?q=agents). Ara *aracıları için Visual Studio 2019*, şunlardan birini seçin *aracı* veya *denetleyicisi*ve ardından *indirme*. Denetleyici ve test aracısını yüklemek için indirdiğiniz yürütebilen dosyayı çalıştırın.

Visual Studio 2017, Visual Studio 2015 ve Visual Studio 2013'ten aracılarını indirin [eski indirmeler](https://visualstudio.microsoft.com/vs/older-downloads/) sayfası.

Bu yükleyici, sanal makinelerde kolay yükleme yapmak için ISO dosyalarını olarak kullanılabilir.

## <a name="compatible-versions-of-tfs-microsoft-test-manager-the-test-controller-and-test-agent"></a>TFS, Microsoft Test Yöneticisi, test denetleyicisi ve test aracısının uyumlu sürümleri

TFS, Microsoft Test Yöneticisi, test denetleyicisi ve test aracısını farklı sürümleri aşağıdaki tabloya göre karıştırabilirsiniz:

| TFS | Microsoft Test Yöneticisi ile Laboratuvar Merkezi | Denetleyici | Aracı |
| --- | -------------------------------------- | ---------- | ----- |
| 2017: 2015'den yükseltme ya da yeni yükleyin | 2017 | 2017 | 2017 |
| 2017: 2015'den yükseltme ya da yeni yükleyin | 2017 | 2013 güncelleştirme 5 | 2013 güncelleştirme 5 |
| 2017: 2015'den yükseltme ya da yeni yükleyin | 2015 | 2013 güncelleştirme 5 | 2013 güncelleştirme 5 |
| 2015: 2013'den yükseltme | 2013 | 2013 |2013 |
| 2015: yeni bir yükleme | 2013 | 2013 | 2013 |
| 2015: 2013'den yükseltme ya da yeni yükleyin | 2015 | 2013 | 2013 |
| 2013 | 2015 | 2013 | 2013 |

> [!NOTE]
> Laboratuvar Yönetimi senaryoları DevOps Hizmetleri ve TFS 2018'de kullanım dışı bırakılmıştır. Daha fazla bilgi için [TFS 2018 sürüm notları](/visualstudio/releasenotes/tfs2018-relnotes#--removing-support-for-lab-center-and-automated-testing-flows-in-microsoft-test-manager).

## <a name="upgrade-from-visual-studio-2013-test-agents"></a>Visual Studio 2013'ün test aracılarını yükseltme

Tüm yeni otomatikleştirilmiş test senaryolarına Visual Studio için agents kullanmanızı öneririz. Kullanabileceğiniz *Test aracıları dağıtmak* indirin ve makinenizde test aracılarını yüklemek için bir derleme işlem hattı görevi.

Aşağıdaki tabloda, aracıları tarafından Visual Studio 2013 ve alternatifleri için Team Foundation Server (TFS) 2015 ve Azure Test planları için desteklenen senaryolar gösterilmektedir:

| Visual Studio 2013 için Agents tarafından desteklenen senaryoları | Diğer TFS ve Azure Test planları |
| - | - |
| Visual Studio yapı-dağıtma-Test iş akışı | Kullanıcılar bir [derleme işlem hattı](/azure/devops/pipelines/index?view=vsts) (XAML derleme değil) için derleme, dağıtma ve test senaryolarında TFS'de. |
| Yük testi (performans testi) kullanarak uzak makinelere şirket | Kullanım Test denetleyicisi ve Test aracısı 2013 güncelleştirme 5 yük testlerini şirket içinde çalıştırmak için. |
| Otomatik testler Microsoft Test laboratuvar ortamı kullanma yöneticisinden, uzaktan yürütme | Şu anda bu senaryo için bir alternatif yoktur. İşlevsel testleri çalıştırma görevini derlemede kullanma ve yayın tanımları (değil, bir XAML derleme) öneririz. testleri uzaktan yürütün. |
| Geliştiriciler Visual Studio'da uzaktan testleri çalıştırma | Artık desteklenmiyor. |
