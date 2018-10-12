---
title: 'Nasıl yapılır: Görselleştiriciyi yükleme | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
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
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d5539b17ee4d10f603f1adfe2ce7e459332181cf
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49250230"
---
# <a name="how-to-install-a-visualizer"></a>Nasıl Yapılır: Görselleştiriciyi Yükleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Görselleştirici oluşturduktan sonra kullanıma sunulacak böylece görselleştiricisi yüklemelisiniz [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Görselleştirici yükleme basit bir işlemdir.  
  
> [!NOTE]
>  İçinde **Store** uygulamalar, yalnızca standart metin, HTML, XML ve JSON görselleştiriciler desteklenir. Özel (kullanıcı tarafından oluşturulmuş) görselleştiriciler desteklenmez.  
  
### <a name="to-install-a-visualizer"></a>Görselleştirici yüklemek için  
  
1.  Derlediğiniz görselleştiricisi içeren DLL bulun.  
  
2.  DLL aşağıdaki konumlardan birini kopyalayın:  
  
    -   *VisualStudioInstallPath* `\Common7\Packages\Debugger\Visualizers`  
  
    -   `My Documents\` *VisualStudioVersion* `\Visualizers`  
  
3.  Uzaktan hata ayıklama için yönetilen Görselleştirici kullanmak istiyorsanız, DLL uzak bilgisayarda aynı yoluna kopyalayın.  
  
4.  Hata ayıklama oturumunu yeniden başlatın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özel Görselleştiriciler oluşturma](../debugger/create-custom-visualizers-of-data.md)   
 [Nasıl Yapılır: Görselleştirici Yazma](../debugger/how-to-write-a-visualizer.md)



