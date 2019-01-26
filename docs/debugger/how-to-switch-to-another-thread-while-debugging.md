---
title: Hata ayıklarken başka bir iş parçacığına geçme
ms.custom: seodec18
ms.date: 04/27/2017
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- threads, switching [debugging]
ms.assetid: 5cd76c52-76fa-4fcc-b37e-e9f0ecac0e9e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 163d14de4880ed1c5e2ae6a3170ec5ae1ae47485
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55005195"
---
# <a name="how-to-switch-to-another-thread-while-debugging-in-visual-studio-c-visual-basic-c"></a>Nasıl yapılır: Visual Studio'da hata ayıklarken başka bir iş parçacığına geçiş (C#, Visual Basic, C++)
Çok iş parçacıklı uygulamada hata ayıklaması yaparken, başka bir iş parçacığına çalıştığınız iş parçacığına geçmek için birkaç yöntemden birini kullanabilirsiniz.

> [!NOTE]
> Hangi iş parçacığı yürütme sırasını denetlemek istiyorsanız, yapmanız [dondurma ve iş parçacıklarını çözme](../debugger/get-started-debugging-multithreaded-apps.md).

Kod Düzenleyicisi ve farklı birden çok iş parçacıklı hata ayıklama windows iş parçacıklarında incelediğinizde, sarı ok geçerli iş parçacığı gösterir. Kıvrık kuyruklu yeşil bir ok, geçerli olmayan bir iş parçacığı geçerli hata ayıklayıcı bağlam sahip olduğunu gösterir.
  
### <a name="to-switch-to-any-thread-that-appears"></a>Görünen tüm iş parçacığına geçiş yapmak için 
  
-   İçinde **iş parçacıkları** veya **paralel izleme** penceresinde iş parçacığını çift tıklayın.  
  
### <a name="to-switch-to-a-thread-in-a-source-window"></a>Bir kaynak penceresinde bir iş parçacığına geçiş yapmak için  
  
-   Sol kanaldaki içinde bir iş parçacığı işaret simgesine sağ tıklayın ![iş parçacığı işaret](../debugger/media/dbg-thread-marker.png "ThreadMarker"), işaret **geçin**, tıkladıktan sonra geçiş yapmak istediğiniz o iş parçacığı adı . Yalnızca bu belirli bir konumdaki iş parçacıkları kısayol menüsünü gösterir.  
  
     Hiçbir iş parçacığı işaretçileri görünüyorsa, sağ **iş parçacıkları** penceresi doğrulayın **kaynak iş parçacıklarını Göster** seçilir.  
  
### <a name="to-switch-to-a-thread-in-the-debug-location-toolbar"></a>Hata ayıklama konumu araç çubuğunda bir iş parçacığına geçiş yapmak için  
  
1.  Üzerinde **hata ayıklama konumu** araç çubuğunda tıklatın **iş parçacığı** listesi.  
  
2.  Listede, geçiş yapmak istediğiniz iş parçacığı tıklayın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çok İş Parçacıklı Uygulamaların Hatalarını Ayıklama](../debugger/debug-multithreaded-applications-in-visual-studio.md)
