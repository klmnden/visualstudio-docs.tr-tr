---
title: 'Nasıl yapılır: Karışık modda hata ayıklama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- debugging DLLs
- debugging [Visual Studio], mixed-mode
- mixed-mode debugging
ms.assetid: 2859067d-7fcc-46b0-a4df-8c2101500977
caps.latest.revision: 32
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 9939c3eef0c2037e02c23573e246dd12d8934a3c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54790603"
---
# <a name="how-to-debug-in-mixed-mode"></a>Nasıl yapılır: Karışık modda hata ayıklama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Aşağıdaki yordamlarda, karma mod hata ayıklama olarak da bilinir, hem yönetilen hem de yerel kod hatalarını ayıklamak açıklanır. Olup DLL ya da uygulama yerel kod halinde yazılmış bağlı olarak bunu yapmak için iki senaryo vardır:  
  
-   DLL'nizi çağıran arama uygulaması yerel kodda yazılır. Bu durumda, DLL yönetilir ve hem yönetilen hem de yerel hata ayıklayıcıları hem de hata ayıklamak için etkinleştirilmesi gerekir. Bu iade  **\<Proje > özellik sayfaları** iletişim kutusu. Bunu nasıl yapacağınız mı DLL projesi veya çağıran uygulama projesinden hata ayıklamaya başladığınızda üzerinde bağlıdır.  
  
-   DLL'nizi çağıran arama uygulaması yönetilen kodda yazılır ve DLL dosyanızı yerel kodda yazılır.  
  
> [!NOTE]
>  Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### <a name="to-enable-mixed-mode-debugging"></a>Karışık mod hata ayıklamayı etkinleştirmek için  
  
1.  İçinde **Çözüm Gezgini**, projeyi seçin.  
  
2.  Üzerinde **görünümü** menüsünü tıklatın **özellik sayfaları**.  
  
3.  İçinde  **\<Proje > özellik sayfaları** iletişim kutusunda **yapılandırma özellikleri** düğümüne tıklayın ve ardından **hata ayıklama**.  
  
4.  Ayarlama **hata ayıklayıcı türü** için **karma** veya **otomatik**.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: DLL Projesinde hata ayıklama](../debugger/how-to-debug-from-a-dll-project.md)
