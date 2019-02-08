---
title: Kabuk Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- tools.shell
helpviewer_keywords:
- exe files
- Shell command
- Tools.Shell command
- executables, running from Visual Studio
- .exe files
- Shell, launching exe files
- Visual Studio, executables from
ms.assetid: 737fda23-b852-45c4-a9fe-41cbce6ba70f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cc571c40dfcc1074b157b850c8b6f3f5e4649563
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55924519"
---
# <a name="shell-command"></a>Kabuk Komutu
Yürütülebilir programlar içinden başlatır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

## <a name="syntax"></a>Sözdizimi

```cmd
Tools.Shell [/command] [/output] [/dir:folder] path [args]
```

## <a name="arguments"></a>Arguments
 `path`

 Gerekli. Yürütülecek dosyayı veya belgeyi açmak için yol ve dosya adı. Belirtilen dosya PATH ortam değişkenine dizinler birinde değilse, bir tam yol gereklidir.

 `args`

 İsteğe bağlı. Çağrılan programa geçirilecek herhangi bir bağımsız değişken.

## <a name="switches"></a>Anahtarlar
 /CommandWindow [ya da] / Command [ya da] /c [veya] / cmd

 İsteğe bağlı. Yürütülebilir dosyası için çıkış görüntülendiğini belirtir **komut** penceresi.

 /dir:`folder` [veya] / d: `folder`

 İsteğe bağlı. Programı çalıştırdığınızda ayarlanacak çalışma dizini belirtir.

 / OutputWindow [veya] / Output [ya da] / out [veya] /o

 İsteğe bağlı. Yürütülebilir dosyası için çıkış görüntülendiğini belirtir **çıkış** penceresi.

## <a name="remarks"></a>Açıklamalar
 Hemen sonra /dir /o /c anahtarları belirtilmelidir `Tools.Shell`. Hiçbir şey yürütülebilir dosya adı için komut satırı bağımsız değişkenleri geçirilir sonra belirtilen.

 Önceden tanımlanmış bir diğer ad `Shell` yerine kullanılan `Tools.Shell`.

> [!CAUTION]
> Varsa `path` bağımsız değişkeni, dosya adının yanı sıra dizin yolu sağlar, tüm yol adını değişmez değer tırnak içine alın ("" "), aşağıdaki gibi:


```cmd
Tools.Shell """C:\Program Files\SomeFile.exe"""
```

 Her dizi üç çift tırnak ("" ") tarafından yorumlanır `Shell` işlemci tek çift tırnak işareti karakteri. Bu nedenle, yukarıdaki örnek aşağıdaki yol dizesini gerçekten geçirir `Shell` komutu:

```cmd
"C:\Program Files\SomeFile.exe"
```

> [!CAUTION]
> Yol dizesi değişmez değer tırnak işaretleri içine almayın varsa ("" "), Windows kadar ilk alanı yalnızca dize bölümünü kullanır. Örneğin, yukarıdaki yol dizesi düzgün alıntılanmadı değil, Windows "Program C:\ kök dizininde bulunan" adlı bir dosya için görünür. C:\Program.exe yürütülebilir dosya kullanılabileceğinden, hatta bir gerçekleşiyorsa kurcalama tarafından yüklü Windows istenen "c:\Program Files\SomeFile.exe" program yerine bu program yürütülmeye çalışıyordu.


## <a name="example"></a>Örnek
 Aşağıdaki komut dosyasını kopyalamak için xcopy.exe kullanır `MyText.txt` içine `Text` klasör. Xcopy.exe çıktısı her ikisinde de görüntülenir **komut penceresi** ve **çıkış** penceresi.

```cmd
>Tools.Shell /o /c xcopy.exe c:\MyText.txt c:\Text\MyText.txt
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Çıktı Penceresi](../../ide/reference/output-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)