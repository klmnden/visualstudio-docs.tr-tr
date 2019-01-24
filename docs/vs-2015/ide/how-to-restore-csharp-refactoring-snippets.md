---
title: 'Nasıl yapılır: Geri yükleme C# yeniden düzenleme kod parçacıklarını | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- unsafe expansion
- expansions, unsafe
ms.assetid: 12114273-7f2f-43d0-abcb-2d4711a3a68d
caps.latest.revision: 24
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: c9ebd6b96a24b10601257d5eefc58014ef7058c9
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54782602"
---
# <a name="how-to-restore-c-refactoring-snippets"></a>Nasıl yapılır: Geri yükleme C# yeniden düzenleme kod parçacıklarını
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

C# yeniden düzenleme işlemleri aşağıdaki dizinde bulunan kod parçacıkları dayanır:  
  
 *Yükleme dizini*\Microsoft Visual Studio 14.0\VC#\Snippets\\*dil kimliği*\Refactoring  
  
 Bu yeniden düzenleme dizin ya da bu dizindeki tüm dosyaları silindi veya bozulmuş, ardından C# yeniden düzenleme işlemleri IDE içinde çalışmayabilir. Aşağıdaki yordamlar, C# yeniden düzenleme kod parçacıklarını geri yüklemenize yardımcı olabilir.  
  
### <a name="to-verify-c-refactoring-snippets-are-available-through-the-code-snippet-manager"></a>C# doğrulamak için yeniden düzenleme kod parçacıklarını kod parçacığı Yöneticisi aracılığıyla kullanılabilir  
  
1.  İçinde **Araçları** menüsünde **kod parçacığı Yöneticisi**.  
  
2.  İçinde **kod parçacığı Yöneticisi** iletişim kutusunda **Visual C#** gelen **dil** aşağı açılan listesi.  
  
     A **yeniden düzenleme** klasör ağaç görünümü klasörü listede görünür.  
  
### <a name="to-restore-refactoring-see-comment-in-code-snippet-manager"></a>Yeniden düzenleme geri yüklemek için kod parçacığı Yöneticisi'nde açıklama bkz:  
  
1.  Varsa **yeniden düzenleme** klasörü değil ağaç görünümü klasörü kod parçacığı Yöneticisi'nin listede, ardından yeniden düzenleme kod parçacıklarını geri kod parçacığı Yöneticisi olarak eklemek için bu yordamı kullanın.  
  
2.  İçinde **Araçları** menüsünde **kod parçacığı Yöneticisi**.  
  
3.  İçinde **kod parçacığı Yöneticisi** iletişim kutusunda **Visual C#** gelen **dil** aşağı açılan listesi.  
  
4.  **Ekle**'yi tıklatın. **Kod parçacıkları dizini** bulun ve geri kod parçacığı Yöneticisi olarak eklemek için dizin belirtmenize yardımcı olur, iletişim kutusu görüntülenir.  
  
5.  Bulun **yeniden düzenleme** klasörü dizin yolu:  
  
     *Yükleme dizini*\Microsoft Visual Studio 14.0\VC#\Snippets\\*dil kimliği*\Refactoring  
  
     Gerçek yolu, bir varsayılan yükleme için aşağıdakine benzer:  
  
     C:\Program Files\Microsoft Visual Studio 14.0\VC#\Snippets\1033\Refactoring.  
  
6.  Tıklayın **açık** içinde **kod parçacıkları dizini** iletişim kutusunu ve ardından **Tamam** kod parçacıkları Yöneticisi'nde.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual C# kod parçacıkları](../ide/visual-csharp-code-snippets.md)   
 [Yeniden düzenlemesi (C#)](../csharp-ide/refactoring-csharp.md)   
 [Kod Parçacıkları](../ide/code-snippets.md)
