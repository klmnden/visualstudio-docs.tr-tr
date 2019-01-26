---
title: Modülleri Listele Komutu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- debug.listmodules
helpviewer_keywords:
- Debug.ListModules command
- ListModules command
- list modules command
ms.assetid: 3cb73774-6ac0-43b2-b781-75ed47175bfd
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b9bf23375f4be979c8cd5ea5dd44913746840ce6
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54972894"
---
# <a name="list-modules-command"></a>Modülleri Listele Komutu
Geçerli işlem için modülleri listeler.

## <a name="syntax"></a>Sözdizimi

```
Debug.ListModules [/Address:yes|no] [/Name:yes|no] [/Order:yes|no]
[/Path:yes|no] [/Process:yes|no] [/SymbolFile:yes|no]
[/SymbolStatus:yes|no] [/Timestamp:yes|no] [/Version:yes|no]
```

#### <a name="parameters"></a>Parametreler
 / Adres:`yes|no`

 İsteğe bağlı. Modül bellek adresleri gösterilip gösterilmeyeceğini belirtir. Varsayılan değer `yes`.

 / Name:`yes|no`

 İsteğe bağlı. Modül adlarını gösterilip gösterilmeyeceğini belirtir. Varsayılan değer `yes`.

 / Order:`yes|no`

 İsteğe bağlı. Modüller sırasını gösterilip gösterilmeyeceğini belirtir. Varsayılan değer `no`.

 / Yolu:`yes|no`

 İsteğe bağlı. Modül yolları gösterilip gösterilmeyeceğini belirtir. Varsayılan değer `yes`.

 / Process:`yes|no`

 İsteğe bağlı. Modüller işlemlerinin gösterilip gösterilmeyeceğini belirtir. Varsayılan değer `no`.

 / SymbolFile:`yes|no`

 İsteğe bağlı. Sembol dosyaları modüllerinin gösterilip gösterilmeyeceğini belirtir. Varsayılan değer `no`.

 / SymbolStatus:`yes|no`

 İsteğe bağlı. Modül sembolü durumları gösterilip gösterilmeyeceğini belirtir. Varsayılan değer `yes`.

 / Zaman damgası:`yes|no`

 İsteğe bağlı. Zaman damgaları modüllerinin gösterilip gösterilmeyeceğini belirtir. Varsayılan değer `no`.

 / VERSION:`yes|no`

 İsteğe bağlı. Modül sürümlerini gösterilip gösterilmeyeceğini belirtir. Varsayılan değer `no`.

## <a name="example"></a>Örnek
 Bu örnekte, modül adlarını, adresleri ve geçerli işlem için zaman damgalarını listeler.

```
Debug.ListModules /Address:yes /Name:yes /Order:no /Path:no /Process:no /SymbolFile:no /SymbolStatus:no /Timestamp:yes /Version:no
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Nasıl yapılır: Modüller Penceresini Kullanma](../../debugger/how-to-use-the-modules-window.md)