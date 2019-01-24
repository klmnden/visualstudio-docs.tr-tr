---
title: 'Nasıl yapılır: Görselleştirici kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: devlang-csharp
ms.topic: conceptual
f1_keywords:
- vs.debug.dataviewer
- vs.debug.stringviewer
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- VB
- CSharp
- C++
helpviewer_keywords:
- debugger, visualizers
- visualizers, about visualizers
ms.assetid: d2611385-0134-4387-8c5a-979fe625a462
caps.latest.revision: 37
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 7ec7527e51175b82d06a35ad7a6bc26856acf5dd
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54773645"
---
# <a name="how-to-use-a-visualizer"></a>Nasıl yapılır: Görselleştirici kullanma
Görselleştirici, veri türü için anlamlı bir şekilde bir değişken veya nesne içeriğini görüntülemek için kullanabilirsiniz. Görselleştiriciler dan kullanabileceğiniz **DataTips**, **izleme** penceresinde **Otolar** penceresinde veya **Yereller** penceresi.  
  
 Görselleştiriciler Compact Framework'te desteklenmez.  
  
> [!NOTE]
>  İçinde **Store** uygulamalar, yalnızca standart metin, HTML, XML ve JSON görselleştiriciler desteklenir. Özel (kullanıcı tarafından oluşturulmuş) görselleştiriciler desteklenmez.  
  
### <a name="to-open-a-visualizer"></a>Görselleştirici açmak için  
  
1.  Bir değişken adı ile yanında Büyüteç simgesine tıklayarak **DataTips**, **Watch** penceresinde veya **Otolar**, **Yereller**, veya **Hızlı Bakış** penceresi.  
  
     Görselleştiriciler listesi görüntülenir.  
  
2.  Kullanmak istediğiniz Görselleştirici'a tıklayın.  
  
### <a name="to-use-a-visualizer-for-managed-code-during-remote-debugging"></a>Uzaktan hata ayıklama sırasında yönetilen kod için Görselleştirici kullanmak için  
  
-   Hata ayıklama oturumu başlatmadan önce DLL Görselleştirici, uzak bilgisayara kopyalayın.  
  
     DLL yolu hem uzak ve yerel bilgisayarlardan aynı olmalıdır. Bu yolu aşağıdaki konumlarda olabilir:  
  
     *Visual Studio yükleme yolu* `\Common7\Packages\Debugger\Visualizers`  
  
     -veya-  
  
     `My Documents\Visual Studio 2010\Visualizers` *Visual Studio sürümü* `\Visualizers`  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özel Görselleştiriciler oluşturma](../debugger/create-custom-visualizers-of-data.md)   
 [Nasıl yapılır: Görselleştiriciyi yükleme](../debugger/how-to-install-a-visualizer.md)   
 [Nasıl yapılır: Görselleştirici yazma](../debugger/how-to-write-a-visualizer.md)   
 [Veri İpuçları'ndaki veri değerlerini görüntüleme](../debugger/view-data-values-in-data-tips-in-the-code-editor.md)