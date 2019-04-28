---
title: Özel derleme olayları belirtme
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- build events, customizing
ms.assetid: 69e935a5-e208-4bcd-865c-3e5f9b047ca8
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: ace8b173eb20b6e628fbb7066ff9010624cca9e9
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63441954"
---
# <a name="specifying-custom-build-events-in-visual-studio"></a>Visual Studio'da Özel Derleme Olayları Belirtme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Özel derleme olay belirterek, otomatik olarak komutları bir oluşturma başlamadan önce veya bittikten sonra çalıştırabilirsiniz. Örneğin, bir .bat dosyası bir yapıdan önce başlar çalıştırın veya derleme tamamlandıktan sonra yeni dosyalar bir klasöre kopyalayın. Derleme olayları, yalnızca derlemenin yapı işleminde bu noktaları başarıyla ulaşırsa çalıştırın.

 Kullandığınız programlama diline hakkında ayrıntılı bilgi için aşağıdaki konulara bakın:

- Visual Basic--[nasıl yapılır: Derleme olayları belirtme (Visual Basic)](../ide/how-to-specify-build-events-visual-basic.md).

- Görsel C# ve F#--[nasıl yapılır: Derleme olayları belirtme (C#)](../ide/how-to-specify-build-events-csharp.md).

- Visual C++--[derleme olayları belirtme](http://msdn.microsoft.com/library/788a6c18-2dbe-4a49-8cd6-86c1ad7a95cc).

## <a name="syntax"></a>Sözdizimi
 DOS komut aynı söz dizimini derleme olayları izleyin, ancak makroları derleme olayları daha kolay oluşturmak için kullanabilirsiniz. Kullanılabilir makrolar bir listesi için bkz. [derleme öncesi olay/derleme sonrası olay komut satırı iletişim kutusu](../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md).

 En iyi sonuçlar için ipuçları biçimlendirme adımları izleyin:

- Ekleme bir `call` tüm olayları, oluşturmadan önce deyimi, .bat dosyaları çalıştırın.

     Örnek: `call C:\MyFile.bat`

     Örnek: `call C:\MyFile.bat call C:\MyFile2.bat`

- Dosya yolları tırnak içine alın.

     Örnek (için [!INCLUDE[win8](../includes/win8-md.md)]): "% ProgramFiles (x86) %\Microsoft SDKs\Windows\v8.0A\Bin\NETFX 4.0 Tools\gacutil.exe"-, "$(TargetPath)"

- Birden çok komut satır sonları ayırın.

- Gerektiği gibi joker karakterler.

     Örnek: `for %I in (*.txt *.doc *.html) do copy %I c:\` *mydirectory*`\`

    > [!NOTE]
    > `%I` Yukarıdaki kodda kullanılmalıdır `%%I` toplu komut.

## <a name="see-also"></a>Ayrıca Bkz.
 [Derleme ve oluşturma](../ide/compiling-and-building-in-visual-studio.md) [derleme öncesi olay/derleme sonrası olay komut satırı iletişim kutusu](../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md) [MSBuild özel karakterleri](../msbuild/msbuild-special-characters.md) [izlenecek yol: Uygulama Oluşturma](../ide/walkthrough-building-an-application.md)
