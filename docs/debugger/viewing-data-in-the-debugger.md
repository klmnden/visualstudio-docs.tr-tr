---
title: Hata ayıklayıcıda verilerin özel görünümlerini oluşturma | Microsoft Docs
ms.date: 01/09/2019
ms.topic: conceptual
f1_keywords:
- vs.debug
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- debugging [Visual Studio], inspecting programs
- debugger, viewing data
ms.assetid: 13e1105f-f987-402e-9108-ec6ac12be042
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 32b3fddd13bd16ac2c846f02f54596ec846374b9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62930000"
---
# <a name="create-custom-views-of-data-in-the-visual-studio-debugger-c-visual-basic-c"></a>Visual Studio hata ayıklayıcıda verilerin özel görünümlerini oluşturma (C#, Visual Basic, C++)

[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] İncelemek ve programınızın durumunu değiştirmek için hata ayıklayıcı birçok araç sağlar. Bu araçlar işlevi yalnızca kesme modunda çoğunu.

## <a name="create-custom-views-of-data-in-variable-windows-and-datatips"></a>Değişken pencereler ve DataTips verilerin özel görünümlerini oluşturma

 Çoğu [windows hata ayıklayıcı](../debugger/debugger-windows.md), gibi **Otolar** ve **izleme** windows, değişkenleri inceleyebilir izin verir. Özelleştirebileceğiniz nasıl C++ türleri, yönetilen nesneleri ve kendi türlerinizi gösterilen hata ayıklayıcı değişken pencerelerinde ve [DataTips](../debugger/view-data-values-in-data-tips-in-the-code-editor.md). Daha fazla bilgi için [özel görünümlerini oluşturma C++ nesneleri](../debugger/create-custom-views-of-native-objects.md) ve [nesnelerin özel görünümlerini oluşturma](../debugger/create-custom-views-of-dot-managed-objects.md).

## <a name="create-custom-visualizers"></a>Özel görselleştiriciler oluşturma

 Görselleştiriciler, bir nesnenin veya değişkenin içeriklerini anlamlı bir şekilde görüntülemek etkinleştirin. Visual Studio hata ayıklayıcısının Görselleştirici Büyüteç'i kullanarak açabilirsiniz farklı windows başvuruyor ![VisualizerIcon](../debugger/media/dbg-tips-visualizer-icon.png "Görselleştirici simgesi") simgesi. Örneğin, nasıl bir HTML dizesi yorumlanır ve bir tarayıcıda görüntülenen HTML görselleştiriciyi gösterir. Görselleştiriciler ipuçlarından erişebileceğiniz **izleme** penceresinde **Otolar** penceresinde ve **Yereller** penceresi. **QuickWatch** iletişim kutusu Görselleştirici de sağlar. Daha fazla bilgi için [özel görselleştiriciler oluşturma](../debugger/create-custom-visualizers-of-data.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)
- [Komut penceresi](../ide/reference/command-window.md)
- [Hata ayıklayıcısı güvenliği](../debugger/debugger-security.md)