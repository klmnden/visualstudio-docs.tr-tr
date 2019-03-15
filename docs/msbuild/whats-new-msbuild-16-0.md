---
title: Hangi&#39;MSBuild 16,0 da | Microsoft Docs
ms.date: 03/11/2019
ms.topic: conceptual
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
monikerRange: '>=vs-2019'
ms.openlocfilehash: 9fb23c8a48493056c9a37f510cefea3cc3374095
ms.sourcegitcommit: 4c7a0c2d712eb24609216577a793e912a6083eaf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "57987000"
---
# <a name="whats-new-in-msbuild-160"></a>MSBuild 16,0 yenilikler

Bu makalede, güncelleştirilmiş özellikleri ve MSBuild 16,0 özellikleri açıklanmaktadır. Ayrıntılı sürüm notları (yalnızca taslak), bkz: [ MSBuild 16,0](https://gist.github.com/rainersigwald/009627466f03964d0028e16fda633d9c).

## <a name="changed-path"></a>Değiştirilen yolu

 MSBuild yüklü *\Current* Visual Studio'nun her sürümü klasöründedir. Örneğin, *C:\Program Files (x86) \Microsoft Visual Studio\Current\Enterprise\MSBuild*. MSBuild bulmak için aşağıdaki PowerShell modülünü de kullanabilirsiniz: [vssetup.powershell](https://github.com/Microsoft/vssetup.powershell).

## <a name="changed-properties"></a>Özellikleri değiştirilmiş

 Aşağıdaki MSBuild özellikleri nedeniyle yeni sürüm numarası güncelleştirildi.

- `MSBuildToolsVersion` Bu araçlar için "Geçerli" sürümüdür. Derleme sürümü Visual Studio 2017, olduğu gibi 15.1.0.0 olduğu aynıdır.

- `VisualStudioVersion` Bu araçlar için "16,0" sürümüdür

## <a name="updates"></a>Güncelleştirmeler

MSBuild (ve Visual Studio) artık .NET Framework 4.7.2’yi hedeflemektedir. Yeni MSBuild API özelliklerini kullanmak istiyorsanız bütünleştirilmiş kodunuz da yükseltilmelidir, ancak mevcut kod çalışmaya devam eder.

## <a name="see-also"></a>Ayrıca bkz.
- [MSBuild](../msbuild/msbuild.md)
