---
title: 'Nasıl Yapılır: Görselleştiriciyi yükleme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- debugger, visualizers
- visualizers, installing
ms.assetid: 3310ef43-515c-4d97-b0f9-51047247d3da
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e62637581fbb65eb8efd20e048cc364895cfbcdc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53914577"
---
# <a name="how-to-install-a-visualizer"></a>Nasıl Yapılır: Görselleştiriciyi yükleme
Görselleştirici oluşturduktan sonra kullanıma sunulacak böylece görselleştiricisi yüklemelisiniz [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Görselleştirici yükleme basit bir işlemdir.  
  
> [!NOTE]
>  UWP uygulamalarında, yalnızca standart metin, HTML, XML ve JSON görselleştiriciler desteklenir. Özel (kullanıcı tarafından oluşturulmuş) görselleştiriciler desteklenmez.  
  
### <a name="to-install-a-visualizer"></a>Görselleştirici yüklemek için  
  
1.  Derlediğiniz görselleştiricisi içeren DLL bulun.  
  
2.  DLL aşağıdaki konumlardan birini kopyalayın:  
  
    -   *VisualStudioInstallPath* `\Common7\Packages\Debugger\Visualizers`  
  
    -   `My Documents\` *VisualStudioVersion* `\Visualizers`  
  
3.  Uzaktan hata ayıklama için yönetilen Görselleştirici kullanmak istiyorsanız, DLL uzak bilgisayarda aynı yoluna kopyalayın.  
  
4.  Hata ayıklama oturumunu yeniden başlatın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özel Görselleştiriciler oluşturma](../debugger/create-custom-visualizers-of-data.md)   
 [Nasıl yapılır: Görselleştirici yazma](/visualstudio/debugger/create-custom-visualizers-of-data)