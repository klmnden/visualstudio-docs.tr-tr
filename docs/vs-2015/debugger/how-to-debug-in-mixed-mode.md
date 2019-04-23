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
ms.openlocfilehash: 5e4a20faa34e8d0dd1018cb4cb5ee0a6df098177
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60107196"
---
# <a name="how-to-debug-in-mixed-mode"></a>Nasıl yapılır: Karışık modda hata ayıklama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Aşağıdaki yordamlarda, karma mod hata ayıklama olarak da bilinir, hem yönetilen hem de yerel kod hatalarını ayıklamak açıklanır. Olup DLL ya da uygulama yerel kod halinde yazılmış bağlı olarak bunu yapmak için iki senaryo vardır:  
  
- DLL'nizi çağıran arama uygulaması yerel kodda yazılır. Bu durumda, DLL yönetilir ve hem yönetilen hem de yerel hata ayıklayıcıları hem de hata ayıklamak için etkinleştirilmesi gerekir. Bu iade  **\<Proje > özellik sayfaları** iletişim kutusu. Bunu nasıl yapacağınız mı DLL projesi veya çağıran uygulama projesinden hata ayıklamaya başladığınızda üzerinde bağlıdır.  
  
- DLL'nizi çağıran arama uygulaması yönetilen kodda yazılır ve DLL dosyanızı yerel kodda yazılır.  
  
> [!NOTE]
>  Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### <a name="to-enable-mixed-mode-debugging"></a>Karışık mod hata ayıklamayı etkinleştirmek için  
  
1. İçinde **Çözüm Gezgini**, projeyi seçin.  
  
2. Üzerinde **görünümü** menüsünü tıklatın **özellik sayfaları**.  
  
3. İçinde  **\<Proje > özellik sayfaları** iletişim kutusunda **yapılandırma özellikleri** düğümüne tıklayın ve ardından **hata ayıklama**.  
  
4. Ayarlama **hata ayıklayıcı türü** için **karma** veya **otomatik**.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: DLL Projesinde hata ayıklama](../debugger/how-to-debug-from-a-dll-project.md)
