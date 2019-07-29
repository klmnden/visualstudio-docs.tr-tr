---
title: İletileri çıkış penceresine gönder | Microsoft Docs
ms.date: 11/08/2018
ms.topic: conceptual
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
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 47b563f58d08a732ec224bb8bbf47ad807c4e81d
ms.sourcegitcommit: ce1ab8a25c66a83e60eab80ed8e1596fe66dd85c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/29/2019
ms.locfileid: "68605384"
---
# <a name="send-messages-to-the-output-window"></a>Çıkış penceresine ileti gönderme

Çalışma zamanı iletilerini **Çıkış** penceresine, sınıf kitaplığının parçası <xref:System.Diagnostics.Debug> <xref:System.Diagnostics> olan sınıfını veya <xref:System.Diagnostics.Trace> sınıfını kullanarak yazabilirsiniz. Yalnızca programınızın *hata ayıklama* sürümünde çıkış istiyorsanız sınıfınıkullanın.<xref:System.Diagnostics.Debug> Hem hata *ayıklama* hem de *Sürüm* sürümlerinde çıkış istiyorsanız sınıfınıkullanın.<xref:System.Diagnostics.Trace>

## <a name="output-methods"></a>Çıkış yöntemleri
 <xref:System.Diagnostics.Trace> Ve<xref:System.Diagnostics.Debug> sınıfları aşağıdaki çıkış yöntemlerini sağlar:

- Farklı `Write` Yöntemler, önemli bir yürütme olmadan bilgi çıktı. Bu yöntemler Visual Basic önceki `Debug.Print` sürümlerinde kullanılan yöntemi değiştirir.

- <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=fullName>ve <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=fullName> belirli bir koşul başarısız olursa yürütme ve çıkış bilgilerini kesen Yöntemler. Varsayılan olarak, `Assert` yöntemi bilgileri bir iletişim kutusunda görüntüler. Daha fazla bilgi için bkz. [Yönetilen koddaki Onaylamalar](../debugger/assertions-in-managed-code.md).

- Yürütme ve <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=fullName> çıkış bilgilerini her zaman kesen veyöntemleri.<xref:System.Diagnostics.Debug.Fail%2A?displayProperty=fullName> Varsayılan olarak, `Fail` Yöntemler bilgileri bir iletişim kutusunda görüntüler.

**Çıkış** penceresinde hakkında bilgi de görüntülenebilir:

- Hata ayıklayıcı tarafından yüklenen veya yüklenmeyen modüller.

- Oluşturulan özel durumlar.

- Çıkış işlemi.

- Çıkış yapan iş parçacıkları.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcısı güvenliği](../debugger/debugger-security.md)
- [Çıkış penceresi](../ide/reference/output-window.md)
- [İzleme ve araç uygulamaları](/dotnet/framework/debug-trace-profile/tracing-and-instrumenting-applications)
- [C#, F#ve Visual Basic proje türleri](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)
- [Yönetilen kodda hata ayıklama](../debugger/debugging-managed-code.md)
