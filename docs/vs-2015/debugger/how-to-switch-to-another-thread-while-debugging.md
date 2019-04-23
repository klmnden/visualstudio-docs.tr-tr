---
title: 'Nasıl yapılır: Hata ayıklarken başka bir iş parçacığına geçiş | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- threads, switching [debugging]
ms.assetid: 5cd76c52-76fa-4fcc-b37e-e9f0ecac0e9e
caps.latest.revision: 29
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 8f481a0b1cb2142dc7dbfe11e17ac627753cebf0
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60052447"
---
# <a name="how-to-switch-to-another-thread-while-debugging"></a>Nasıl yapılır: Hata ayıklarken başka bir iş parçacığına geçiş
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Çok iş parçacıklı uygulamada hata ayıklaması yaparken, başka bir iş parçacığına çalıştığınız iş parçacığı bağlamdan geçiş yapmak için birkaç yöntemden birini kullanabilirsiniz.  
  
### <a name="to-switch-to-any-thread-that-appears-in-the-threads-window"></a>İş parçacıkları penceresinde görüntülenen herhangi bir iş parçacığına geçiş yapmak için  
  
- İş parçacığını çift tıklayın.  
  
### <a name="to-switch-to-a-thread-in-a-source-window"></a>Bir kaynak penceresinde bir iş parçacığına geçiş yapmak için  
  
- Sol kanaldaki iş parçacığı göstergesi sağ tıklayın, fareyle **geçin**ve sonra geçiş yapmak istediğiniz o iş parçacığı adına tıklayın. Yalnızca bu belirli bir konumdaki iş parçacıkları kısayol menüsünü gösterir.  
  
     Hiçbir göstergeleri görünmüyorsa, sağ **iş parçacıkları** penceresi doğrulayın **kaynak iş parçacıklarını Göster** seçilir.  
  
### <a name="to-switch-to-a-thread-in-the-debug-location-toolbar"></a>Hata ayıklama konumu araç çubuğunda bir iş parçacığına geçiş yapmak için  
  
1. Üzerinde **hata ayıklama konumu** araç çubuğunda tıklatın **iş parçacığı** kutusu.  
  
2. Listede, geçiş yapmak istediğiniz iş parçacığı tıklayın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çok İş Parçacıklı Uygulamaların Hatalarını Ayıklama](../debugger/debug-multithreaded-applications-in-visual-studio.md)
