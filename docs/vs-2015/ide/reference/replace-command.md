---
title: Değiştir komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- edit.replace
helpviewer_keywords:
- Edit.Replace command
- Replace command
ms.assetid: a15767f1-5a3d-44f5-8c77-7b0f1157f340
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f230a2270274f85fd799f86caa278bb98cb5fd46
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54772241"
---
# <a name="replace-command"></a>Değiştir Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Metin dosyalarında bulunan seçenekler kümesini kullanarak değiştirir **dosyalarda Değiştir** sekmesinde **Bul ve Değiştir** penceresi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Edit.Replace findwhat replacewith [/all] [/case]  
[/doc|/proc|/open|/sel] [/hidden] [/options] [/reset] [/up]  
[/wild|/regex] [/word]  
```  
  
## <a name="arguments"></a>Arguments  
 `findwhat`  
 Gerekli. Eşleştirilecek metin.  
  
 `replacewith`  
 Gerekli. Eşleşen metni eklenecek metin.  
  
## <a name="switches"></a>Anahtarlar  
 / all veya /a  
 İsteğe bağlı. Arama metni tüm oluşumlarını değiştirme metni ile değiştirir.  
  
 /Case veya /c  
 İsteğe bağlı. Eşleşme gerçekleşmesi yalnızca zaman büyük ve küçük harfleri tam olarak belirtilen platformlarla eşleşen `findwhat` bağımsız değişken.  
  
 / doc veya /d  
 İsteğe bağlı. Yalnızca geçerli belgede arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.  
  
 / Gizli veya/h  
 İsteğe bağlı. Bir tasarım zamanı denetimi, gizli bir bölge anahatları belirlenmiş bir belge veya bir daraltılmış sınıf veya yöntemin meta verilerini gibi altına gizlenmiş ve daraltılmış metin araması yapar.  
  
 /Open veya /o  
 İsteğe bağlı. Bir belge değilmiş gibi tüm açık belgeleri arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.  
  
 / Options veya /t  
 İsteğe bağlı. Geçerli bulma seçeneği ayarları listesini görüntüler ve arama yapmaz.  
  
 /proc veya /p  
 İsteğe bağlı. Yalnızca geçerli yordamı arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.  
  
 /Regex veya /r  
 İsteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak sabit karakterleriyle yerine metin desenleri temsil eden gösterimler. Normal ifade karakterleri tam bir listesi için bkz. [normal ifadeler](../../ide/using-regular-expressions-in-visual-studio.md).  
  
 Reset veya /e  
 İsteğe bağlı. Bulma seçenekleri varsayılan ayarlarına geri döndürür ve bir arama yapmaz.  
  
 /sel veya /s  
 İsteğe bağlı. Yalnızca geçerli seçimi arar. Kullanılabilir arama kapsamları yalnızca birini belirtin `/doc`, `/proc`, `/open`, veya `/sel`.  
  
 /UP veya /u  
 İsteğe bağlı. Dosyanın üst tarafındaki dosya geçerli konumda arar. Varsayılan olarak, dosya ve İlerle dosyasının en altına doğru geçerli konumu aramaları başlar.  
  
 /wild veya/l  
 İsteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak bir karakter ya da dizi karakteri temsil etmek için gösterimler.  
  
 /Word veya /w  
 İsteğe bağlı. Yalnızca için tam sözcükleri arar.  
  
## <a name="example"></a>Örnek  
 Bu örnekte değiştirir `btnSend` ile `btnSubmit` tüm açık belgeleri.  
  
```  
>Edit.Replace btnSend btnSubmit /open  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Metin bulma ve değiştirme](../../ide/finding-and-replacing-text.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
