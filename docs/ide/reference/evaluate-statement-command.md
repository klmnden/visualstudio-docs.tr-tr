---
title: Deyimi Değerlendir Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- debug.evaluatestatement
helpviewer_keywords:
- Debug.EvaluateStatement command
- Evaluate Statement command
ms.assetid: 032039bc-9477-4f93-9b9d-66d4be0e90f4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 98bdaf41aa34367d656e2bfb5694f3b615dbe3b8
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55911747"
---
# <a name="evaluate-statement-command"></a>Deyimi Değerlendir Komutu
Değerlendirir ve verilen deyimi görüntüler.

## <a name="syntax"></a>Sözdizimi

```cmd
Debug.EvaluateStatement text
```

## <a name="arguments"></a>Arguments
 `text` Gerekli. Değerlendirilecek ifade.

## <a name="remarks"></a>Açıklamalar
 Girmek için kullanılan pencere **EvaluateStatement** komut belirleyen bir eşittir işareti (=) karşılaştırma işleci veya bir atama işleci olarak yorumlanır.

 İçinde **komut** penceresinde, eşittir işareti (=) karşılaştırma işleci yorumlanır. Örneğin, bu nedenle, değişkenlerin değerleri `a` ve `b` farklı, sonra komutu

```cmd
>Debug.EvaluateStatement(a=b)
```

 bir değeri döndürür `false`.

 İçinde **hemen** penceresinde, aksine, eşittir işareti (=) bir atama işleci yorumlanır. Bunu, örneğin, komut

```cmd
>Debug.EvaluateStatement(a=b)
```

 atar `a` değişkenin değerini `b`.

## <a name="example"></a>Örnek

```cmd
>Debug.EvaluateStatement(a+b)
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Yazdır Komutu](../../ide/reference/print-command.md)
- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)