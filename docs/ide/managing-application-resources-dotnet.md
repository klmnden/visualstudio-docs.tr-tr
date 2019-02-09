---
title: Uygulama kaynaklarını yönetme (.NET)
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- msvse_resedit.dlg.SetCustomTool
- msvse_settingsdesigner.err.formatvalue
- msvse_resedit.err.nameblank
- msvse_resedit.err.duplicatename
helpviewer_keywords:
- Resource Designer
- resources [Visual Studio]
- Resources page in Project Designer
- application resources [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 48dbd24ba98ad3f1b4f24a68c9775b1022ea08f6
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55970315"
---
# <a name="manage-application-resources-net"></a>Uygulama kaynaklarını yönetme (.NET)

Derlenmemiş, ancak bir uygulamanın parçası olan dosyalar için örnek simge dosyaları ya da ses dosyaları kaynak dosyalarıdır. Bu dosyaları derleme işleminin bir parçası olmadığından, ikili dosyalarınızı yeniden derlemenize gerek kalmadan değiştirebilirsiniz. Uygulamanızı yerelleştirmek planlıyorsanız, tüm dizeler ve uygulamanızı yerelleştirdiğiniz zaman değiştirilmesi gereken diğer kaynaklar için kaynak dosyaları kullanmalısınız.

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [(Mac için Visual Studio) uygulama kaynaklarını yönetme](/visualstudio/mac/managing-app-resources).

.NET Masaüstü uygulamalarındaki kaynaklar hakkında daha fazla bilgi için bkz: [masaüstü uygulamalarında kaynakların](/dotnet/framework/resources/index).

## <a name="work-with-resources"></a>Kaynakları ile çalışma

Yönetilen kod projesi içinde proje özellikleri penceresini açın. Özellikler penceresinde ya da açabilirsiniz:

- ' Nde proje düğümüne sağ tıklayarak **Çözüm Gezgini** seçerek **özellikleri**
- "Proje özelliklerinde" yazarak **hızlı başlatma** penceresi
- Seçme **Alt**+**girin** içinde **Çözüm Gezgini**

Seçin **kaynakları** sekmesi. Ekleyebileceğiniz bir *.resx* projenizi değil bir zaten içeren, ekleyin ve farklı türde kaynakların silme ve var olan kaynakları değiştirmek dosyası.

## <a name="resources-in-other-project-types"></a>Kaynaklar diğer proje türleri

Kaynaklar, farklı .NET projeleri diğer proje türleri içinde yönetilir. Kaynaklar hakkında daha fazla bilgi için:

- Evrensel Windows Platformu (UWP) uygulamaları görmek [uygulama kaynaklarını ve kaynak yönetim sistemi](/windows/uwp/app-resources/)
- C++ projeleri için bkz: [kaynak dosyalarıyla çalışmak](/cpp/windows/working-with-resource-files) ve [nasıl yapılır: Kaynak Oluştur](/cpp/windows/how-to-create-a-resource)

## <a name="see-also"></a>Ayrıca bkz.

- [(.NET Framework) Masaüstü uygulamalarındaki kaynaklar](/dotnet/framework/resources/index)
- [(Mac için Visual Studio) uygulama kaynaklarını yönetme](/visualstudio/mac/managing-app-resources)
