---
title: Çıkış penceresindeki tanılama iletileri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.output
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- diagnostic messages [C#]
- System.Diagnostics.Debug class, Output window
- messages, diagnostic
- Debug.Print replacements
- diagnosis
- Output window, diagnostic messages
- System.Diagnostics.Trace class, Output window
- Trace class, diagnostic messages
- diagnostics
- debugger, Output window
- debugging [Visual Studio], diagnostic messages in Output window
- Debug class
ms.assetid: 386e9524-be17-4573-83fb-4f7c5cae0be0
caps.latest.revision: 19
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 6cf5025fdbb640b9f77e0782a7db77503fc618a4
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54769469"
---
# <a name="diagnostic-messages-in-the-output-window"></a>Çıkış Penceresindeki Tanılama İletileri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Hata ayıklama sınıfı veya izleme sınıfını kullanarak çıkış penceresinde çalışma zamanı iletileri yazabileceğiniz bir parçası olan <xref:System.Diagnostics> sınıf kitaplığı. Programınızın hata ayıklama sürümünde yalnızca çıktısını alırsanız hata ayıklama sınıfını kullanın. Hata ayıklama ve yayın sürümleri çıktısında istiyorsanız izleme sınıfını kullanın.  
  
## <a name="output-methods"></a>Çıkış yöntemleri  
 <xref:System.Diagnostics.Trace> Ve <xref:System.Diagnostics.Debug> sınıfları aşağıdaki çıktı yöntemlerini sağlar:  
  
- Çeşitli `Write` yürütme bozmadan bilgi çıkış yöntemleri. Bu yöntemler yerine `Debug.Print` Visual Basic'in önceki sürümlerinde kullanılan yöntem.  
  
- <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=fullName> ve <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=fullName> belirtilen bir koşulu başarısız olursa, yürütme ve çıkış bilgileri sonu yöntemleri. Varsayılan olarak, `Assert` yöntemi bilgileri iletişim kutusu içinde görüntüler. Daha fazla bilgi için [yönetilen koddaki onaylar](../debugger/assertions-in-managed-code.md).  
  
- <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=fullName> Ve <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=fullName> her zaman yürütmeyi keser ve bilgi yöntemleri. Varsayılan olarak, `Fail` yöntemleri bilgileri iletişim kutusu içinde görüntüler.  
  
  Programı, uygulamanızın yanı sıra **çıkış** penceresi hakkında bilgileri görüntüleyebilirsiniz:  
  
- Modüller hata ayıklayıcı yüklü veya kaldırılmış.  
  
- Oluşan özel durumlar.  
  
- Çıkış işlemleri.  
  
- Çıkış iş parçacıkları.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklayıcısı güvenliği](../debugger/debugger-security.md)   
 [Çıkış penceresi](../ide/reference/output-window.md)   
 [İzleme ve İşaretleme uygulamaları](http://msdn.microsoft.com/library/773b6fc4-9013-4322-b728-5dec7a72e743)   
 [İzlemeye giriş](http://msdn.microsoft.com/e924e57c-33cf-4b0e-9e7f-a45d13e38f2c)   
 [C#, F#ve Visual Basic proje türleri](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)   
 [Yönetilen Kodda Hata Ayıklama](../debugger/debugging-managed-code.md)
