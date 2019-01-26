---
title: Microsoft Visual Studio hata ayıklayıcısı (özel durum oluştu) iletişim kutusu | Microsoft Docs
titleSuffix: ''
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.exceptions.thrown
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Microsoft Visual Studio Debugger (Exception Thrown) dialog box
- exception handling, during debugging
- debugger, exceptions
- throwing exceptions, during debugging
ms.assetid: 1fe98d10-c8f9-4b39-a920-99169bfd542e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 01ccb091163e3b70c90eaa9b1b6d3b7256a20d4e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54954377"
---
# <a name="microsoft-visual-studio-debugger-exception-thrown-dialog-box"></a>Microsoft Visual Studio Hata Ayıklayıcısı (Özel Durum Oluştu) İletişim Kutusu
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
 [Özel durumlar için en iyi yöntemler](/dotnet/standard/exceptions/best-practices-for-exceptions)   
 [Özel Durum İşleme](/cpp/windows/exception-handling-cpp-component-extensions)