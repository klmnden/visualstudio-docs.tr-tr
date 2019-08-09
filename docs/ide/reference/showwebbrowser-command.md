---
title: ShowWebBrowser Komutu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- view.showwebbrowser
helpviewer_keywords:
- ShowWebBrowser command
- View.ShowWebBrowser command
ms.assetid: c6a4fbd6-8e9d-45cc-8b2f-93990d065e78
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 14e2d6f2c753c56d1628d20e921b7dff2aa83471
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926016"
---
# <a name="showwebbrowser-command"></a>ShowWebBrowser Komutu

Tümleşik geliştirme ortamı (IDE) veya IDE dışında içindeki bir web tarayıcı penceresinde belirttiğiniz URL'yi görüntüler.

## <a name="syntax"></a>Sözdizimi

```cmd
View.ShowWebBrowser URL [/new][/ext]
```

## <a name="arguments"></a>Arguments
`URL`

Gerekli. Web sitesi için URL (Tekdüzen Kaynak Konum Belirleyicisi).

## <a name="switches"></a>Anahtarlar
/Yeni

İsteğe bağlı. Sayfanın, Web tarayıcısının yeni bir örneğinde göründüğünü belirtir.

/ext

İsteğe bağlı. Sayfanın IDE dışında varsayılan Web tarayıcısında göründüğünü belirtir.

## <a name="remarks"></a>Açıklamalar
**ShowWebBrowser** komutunun diğer adı **Git** veya **Gezinti**' dir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, Microsoft Docs giriş sayfasını IDE dışında bir Web tarayıcısında görüntüler. Web tarayıcısının bir örneği zaten açıksa, kullanılır; Aksi halde yeni bir örnek başlatılır.

```cmd
>View.ShowWebBrowser https://docs.microsoft.com /ext
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio Komutları](../../ide/reference/visual-studio-commands.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Bul/Komut Kutusu](../../ide/find-command-box.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)