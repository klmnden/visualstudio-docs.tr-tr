---
title: Çağrı Yığınını Listele Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- debug.listcallstack
helpviewer_keywords:
- list call stack command
- Debug.ListCallStack command
ms.assetid: a8b20bf2-81d2-4069-aea8-23e6b15b4347
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a122b9fbc97816b114ba2ff6274756f9e2093eef
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919159"
---
# <a name="list-call-stack-command"></a>Çağrı Yığınını Listele Komutu
Geçerli çağrı yığınını görüntüler.

## <a name="syntax"></a>Sözdizimi

```cmd
Debug.ListCallStack [/Count:number] [/ShowTypes:yes|no]
[/ShowNames:yes|no] [/ShowValues:yes|no] [/ShowModule:yes|no]
[/ShowLineOffset:yes|no] [/ShowByteOffset:yes|no]
[/ShowLanguage:yes|no] [/IncludeCallsAcrossThreads:yes|no]
[/ShowExternalCode:yes|no] [Thread:n] [index]
```

## <a name="arguments"></a>Arguments

`index`\
İsteğe bağlı. Geçerli yığın çerçevesini ayarlar ve çıkış görüntülemez.

## <a name="switches"></a>Anahtarlar
Her anahtar, tamamı ya da kısa bir form kullanılarak çağrılabilir.

/Count:`number` [veya]/c:`number`

İsteğe bağlı. Görüntülenecek en fazla çağrı yığını sayısı. Varsayılan değer sınırsızdır.

/Showtypes:`yes` &#124; `no` [veya]/t:`yes`&#124;`no`

İsteğe bağlı. Parametre türlerinin görüntülenip görüntülenmeyeceğini belirtir. Varsayılan değer `yes`.

/Shownames:`yes` &#124; `no` [veya]/n:`yes`&#124;`no`

İsteğe bağlı. Parametre adlarının görüntülenip görüntülenmeyeceğini belirtir. Varsayılan değer `yes`.

/Showvalues:`yes` &#124; `no` [veya]/v:`yes`&#124;`no`

İsteğe bağlı. Parametre değerlerinin görüntülenip görüntülenmeyeceğini belirtir. Varsayılan değer `yes`.

/Showmodule:`yes` &#124; `no` [veya]/m:`yes`&#124;`no`

İsteğe bağlı. Modül adının görüntülenip görüntülenmeyeceğini belirtir. Varsayılan değer `yes`.

/Showlinekayması:`yes` &#124; `no` [veya]/#:`yes`&#124;`no`

İsteğe bağlı. Çizgi kaydırın görüntülenip görüntülenmeyeceğini belirtir. Varsayılan değer `no`.

/Showbytekayması:`yes` &#124; `no` [veya]/b:`yes`&#124;`no`

İsteğe bağlı. Bayt kaydırının görüntülenip görüntülenmeyeceğini belirtir. Varsayılan değer `no`.

/Showlanguage:`yes` &#124; `no` [veya]/l:`yes`&#124;`no`

İsteğe bağlı. Dilin görüntülenip görüntülenmeyeceğini belirtir. Varsayılan değer `no`.

/Includecallsacrossthreads:`yes` &#124; `no` [veya]/i:`yes`&#124;`no`

İsteğe bağlı. Diğer iş parçacıklarından veya çağrıların eklenip eklenmeyeceğini belirtir. Varsayılan değer `no`.

/ShowExternalCode:`yes`&#124;`no`

İsteğe bağlı. Callstack için Yalnızca kendi kodum gösterilip gösterilmeyeceğini belirtir. Yalnızca kendi kodum kapalıyken, tüm Kullanıcı dışı kod görüntülenir. Yalnızca kendi kodum açık olduğunda, çağrı yığını çıkışında Kullanıcı olmayan kod görüntülenir `[external]` .

Zincirinin`n`

İsteğe bağlı. İş parçacığı `n`için çağrı yığını 'i görüntüler. Hiçbir iş parçacığı belirtilmemişse, geçerli iş parçacığı için çağrı yığınını görüntüler.

## <a name="remarks"></a>Açıklamalar
Bağımsız değişkenlerde veya anahtarlarda yapılan değişiklikler, bu komutun gelecekteki etkinleştirmeleri için geçerlidir. Kendi kendine hata ayıkla. Listcallstackbir sorun varsa, tüm çağrı yığını görüntülenir. Bir dizin belirtirseniz, örneğin

```cmd
Debug.ListCallStack 2
```

sonra geçerli yığın çerçevesi bu çerçeveye ayarlanır (Bu örnekte ikinci kare).

Bu komutu, önceden tanımlanmış bir diğer ad olan KB kullanarak da yazabilirsiniz. Örneğin,

```cmd
kb 2
```

geçerli yığın çerçevesini ikinci çerçeveye ayarlamak için.

## <a name="example"></a>Örnek

```cmd
>Debug.CallStack /Count:4 /ShowTypes:yes
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Ayrıştırılmış Kodu Listele Komutu](../../ide/reference/list-disassembly-command.md)
- [İş Parçacıklarını Listele Komutu](../../ide/reference/list-threads-command.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)