---
title: Microsoft Visual Studio hata ayıklayıcısı (özel durum oluştu) iletişim kutusu | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.exceptions.thrown
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- Microsoft Visual Studio Debugger (Exception Thrown) dialog box
- exception handling, during debugging
- debugger, exceptions
- throwing exceptions, during debugging
ms.assetid: 1fe98d10-c8f9-4b39-a920-99169bfd542e
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5c3ce3a3362c657d4302ba919c866d4a32055423
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49226174"
---
# <a name="microsoft-visual-studio-debugger-exception-thrown-dialog-box"></a>Microsoft Visual Studio Hata Ayıklayıcısı (Özel Durum Oluştu) İletişim Kutusu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Programınızda bir özel durum oluştu. Bu iletişim kutusunu oluşan özel durumun türünü bildirir. Bu özel durumu işlemek kodunuzu gerekir. Özel durum işleme için aşağıdaki seçenekler arasından seçim yapabilirsiniz:  
  
 **sonu**  
 Hata ayıklayıcıyı durdurmak için yürütmeye izin verir. Özel durum işleyicisini break önce çağrılır. Aradan devam ederseniz, özel durum işleyicisi çağrılır.  
  
 **Continue**  
 Özel durum işleyicisi özel durumu işlemek üzere bir fırsat vermek yürütme işleminin devam etmesini sağlar. Bu seçenek, belirli türdeki özel durumlar için kullanılamaz. **Devam** devam etmek uygulama izin verir. Yerel bir uygulamada yeniden oluşturulabilir için özel durum neden olur. Yönetilen bir uygulamada sonlandırmak için program veya bir barındırma uygulaması tarafından işlenmek üzere özel durum ya da neden olur.  
  
> [!NOTE]
>  Yönetilen kodda işlenmemiş özel durumdan sonra devam edemiyor. Seçme **devam** sonra hata ayıklamayı durdurmaya yönetilen kodda işlenmemiş bir özel durum neden olur.  
  
 **Yoksay**  
 Özel durum işleyicisini çağırarak olmadan devam etmek için yürütmeye izin verir. Özel durum işleyicisi çağrılmaz çünkü bu ek özel durumlar ve hatalar dahil olmak üzere daha fazla sonuçlara yol açabilir. Bu seçenek, belirli türdeki özel durumlar için kullanılamaz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özel durumları hata ayıklayıcısı ile yönetme](../debugger/managing-exceptions-with-the-debugger.md)   
 [Özel durumlar için en iyi yöntemler](http://msdn.microsoft.com/library/f06da765-235b-427a-bfb6-47cd219af539)   
 [Özel Durum İşleme](http://msdn.microsoft.com/library/ccb11fe8-6938-41ac-b477-a183e85865b9)



