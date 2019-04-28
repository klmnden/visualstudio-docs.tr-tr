---
title: 'Nasıl yapılır: Görselleştiriciyi yükleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
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
- visualizers, installing
ms.assetid: 3310ef43-515c-4d97-b0f9-51047247d3da
caps.latest.revision: 29
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5726cea8b2e81c53b5f3fff963357946f26b199f
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63438222"
---
# <a name="how-to-install-a-visualizer"></a>Nasıl yapılır: Görselleştiriciyi yükleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Görselleştirici oluşturduktan sonra kullanıma sunulacak böylece görselleştiricisi yüklemelisiniz [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Görselleştirici yükleme basit bir işlemdir.  
  
> [!NOTE]
> İçinde **Store** uygulamalar, yalnızca standart metin, HTML, XML ve JSON görselleştiriciler desteklenir. Özel (kullanıcı tarafından oluşturulmuş) görselleştiriciler desteklenmez.  
  
### <a name="to-install-a-visualizer"></a>Görselleştirici yüklemek için  
  
1. Derlediğiniz görselleştiricisi içeren DLL bulun.  
  
2. DLL aşağıdaki konumlardan birini kopyalayın:  
  
    - *VisualStudioInstallPath* `\Common7\Packages\Debugger\Visualizers`  
  
    - `My Documents\` *VisualStudioVersion* `\Visualizers`  
  
3. Uzaktan hata ayıklama için yönetilen Görselleştirici kullanmak istiyorsanız, DLL uzak bilgisayarda aynı yoluna kopyalayın.  
  
4. Hata ayıklama oturumunu yeniden başlatın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özel Görselleştiriciler oluşturma](../debugger/create-custom-visualizers-of-data.md)   
 [Nasıl yapılır: Görselleştirici Yazma](../debugger/how-to-write-a-visualizer.md)
