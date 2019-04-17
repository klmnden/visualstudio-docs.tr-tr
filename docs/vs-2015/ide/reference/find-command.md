---
title: Bul komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- edit.find
helpviewer_keywords:
- Find command
- Edit.Find command
ms.assetid: f0c705dc-2b97-423d-abbf-5584d4827208
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: ee744a8ab3a22d640f3d48e7291b546f36415d24
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59667293"
---
# <a name="find-command"></a>Bul Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Dosyaları bulunan seçenekler kümesini kullanarak arar **dosyalarda Bul** sekmesinde **Bul ve Değiştir** penceresi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Edit.Find findwhat [/case] [/doc | /proc | /open | /sel]   
[/markall] [/options] [/reset] [/up] [/wild | /regex] [/word]  
```  
  
## <a name="arguments"></a>Arguments  
 `findwhat`  
 Gerekli. Eşleştirilecek metin.  
  
## <a name="switches"></a>Anahtarlar  
 /Case veya /c  
 İsteğe bağlı. Eşleşme gerçekleşmesi yalnızca büyük ve küçük harfleri tam olarak belirtilen platformlarla eşleşen `findwhat` bağımsız değişken.  
  
 / doc veya /d  
 İsteğe bağlı. Yalnızca geçerli belgede arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.  
  
 /markall veya /m  
 İsteğe bağlı. Geçerli belge içinde bir arama eşleşme içeren her satırda bir grafik yerleştirir.  
  
 /Open veya /o  
 İsteğe bağlı. Bir belge değilmiş gibi tüm açık belgeleri arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.  
  
 / Options veya /t  
 İsteğe bağlı. Geçerli bulma seçeneği ayarları listesini görüntüler ve arama yapmaz.  
  
 /proc veya /p  
 İsteğe bağlı. Yalnızca geçerli yordamı arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.  
  
 Reset veya /e  
 İsteğe bağlı. Bulma seçenekleri varsayılan ayarlarına geri döndürür ve bir arama yapmaz.  
  
 /sel veya /s  
 İsteğe bağlı. Yalnızca geçerli seçimi arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.  
  
 /UP veya /u  
 İsteğe bağlı. Dosyanın başına doğru dosyasındaki geçerli konumda arar. Varsayılan olarak geçerli konumda dosyanın sonuna doğru arar ve dosya aramaları başlar.  
  
 /Regex veya /r  
 İsteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak sabit karakterleriyle yerine metin desenleri temsil eden gösterimler. Normal ifade karakterleri tam bir listesi için bkz. [normal ifadeler](../../ide/using-regular-expressions-in-visual-studio.md).  
  
 /wild veya/l  
 İsteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak bir karakter ya da dizi karakteri temsil etmek için gösterimler.  
  
 /Word veya /w  
 İsteğe bağlı. Yalnızca için tam sözcükleri arar.  
  
## <a name="example"></a>Örnek  
 Bu örnek, şu anda seçili kod bölümünde "somestring" sözcüğü için büyük küçük harfe duyarlı bir arama gerçekleştirir.  
  
```  
>Edit.Find somestring /sel /case  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
