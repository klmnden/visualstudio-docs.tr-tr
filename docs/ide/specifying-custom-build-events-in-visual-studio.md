---
title: Özel derleme olayları belirtme
ms.date: 11/04/2016
ms.technology: vs-ide-compile
ms.topic: conceptual
helpviewer_keywords:
- build events, customizing
ms.assetid: 69e935a5-e208-4bcd-865c-3e5f9b047ca8
author: ghogen
ms.author: ghogen
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 620ffa1ea23c2c892e8385bd9e81a07fb640411a
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68918907"
---
# <a name="specify-custom-build-events-in-visual-studio"></a>Visual Studio'da özel derleme olayları belirtme

Özel derleme olay belirterek, otomatik olarak komutları bir oluşturma başlamadan önce veya bittikten sonra çalıştırabilirsiniz. Örneğin, çalıştırabileceğiniz bir *.bat* bir oluşturma başlamadan önce dosya veya derleme tamamlandıktan sonra yeni dosyalar bir klasöre kopyalayın. Derleme olayları, yalnızca derlemenin yapı işleminde bu noktaları başarıyla ulaşırsa çalıştırın.

Kullandığınız programlama diline hakkında ayrıntılı bilgi için aşağıdaki konulara bakın:

- Visual Basic--[nasıl yapılır: Derleme olaylarını belirtin (Visual Basic)](../ide/how-to-specify-build-events-visual-basic.md).

- C#ve F#--[nasıl yapılır: Derleme olaylarını (C#)](../ide/how-to-specify-build-events-csharp.md)belirtin.

- Visual C++--[derleme olayları belirtme](/cpp/build/specifying-build-events).

## <a name="syntax"></a>Sözdizimi

DOS komut aynı söz dizimini derleme olayları izleyin, ancak makroları derleme olayları daha kolay oluşturmak için kullanabilirsiniz. Kullanılabilir makrolar bir listesi için bkz. [derleme öncesi olay/derleme sonrası olay komut satırı iletişim kutusu](../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md).

En iyi sonuçlar için ipuçları biçimlendirme adımları izleyin:

- Ekleme bir `call` tüm çalışan olayları oluşturmadan önce deyimi *.bat* dosyaları.

   Örnek: `call C:\MyFile.bat`

   Örnek: `call C:\MyFile.bat call C:\MyFile2.bat`

- Dosya yolları tırnak içine alın.

   Örnek (için [!INCLUDE[win8](../debugger/includes/win8_md.md)]): "% ProgramFiles (x86) %\Microsoft SDKs\Windows\v8.0A\Bin\NETFX 4.0 Tools\gacutil.exe"-, "$(TargetPath)"

- Birden çok komut satır sonları ayırın.

- Gerektiği gibi joker karakterler.

   Örnek: `for %I in (*.txt *.doc *.html) do copy %I c:\` *mydirectory*`\`

  > [!NOTE]
  > `%I` Yukarıdaki kodda kullanılmalıdır `%%I` toplu komut.

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme ve oluşturma](../ide/compiling-and-building-in-visual-studio.md)
- [Derleme öncesi olay/derleme sonrası olay komut satırı iletişim kutusu](../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md)
- [MSBuild özel karakterleri](../msbuild/msbuild-special-characters.md)
- [İzlenecek yol: Uygulama oluşturma](../ide/walkthrough-building-an-application.md)
