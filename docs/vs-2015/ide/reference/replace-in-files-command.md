---
title: Dosyalarda Değiştir komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- edit.replaceinfiles
helpviewer_keywords:
- Edit.ReplaceInFiles command
- Replace In Files command
- ReplaceInFiles command
ms.assetid: f116066a-4f65-4f2c-94ef-12cbd8cfb598
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 8398f07cf6fa6bd2702b2d84ab0d29dcd614ed32
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68157798"
---
# <a name="replace-in-files-command"></a>Dosyalarda Değiştir Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Metin dosyalarında bulunan seçenekler kümesini kullanarak değiştirir **dosyalarda Değiştir** sekmesinde **Bul ve Değiştir** penceresi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Edit.ReplaceinFiles findwhat replacewith [/all] [/case]  
[/ext:extensions] [/keep] [/lookin:searchpath] [/options] [/regex]  
[/reset] [/stop] [/sub] [/text2] [/wild] [/word]  
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
  
 /ext: `extensions`  
 İsteğe bağlı. Aratılmak üzere dosyalar için dosya uzantılarını belirtir.  
  
 /Keep veya /k  
 İsteğe bağlı. Tüm değiştirilen dosyaları açık bırakılan olduğunu belirtir.  
  
 /lookin: `searchpath`  
 İsteğe bağlı. Aranacak dizini. Yol boşluklar içeriyorsa, yolun tamamını tırnak içine alın.  
  
 / Options veya /t  
 İsteğe bağlı. Geçerli bulma seçeneği ayarları listesini görüntüler ve arama yapmaz.  
  
 /Regex veya /r  
 İsteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak sabit karakterleriyle yerine metin desenleri temsil eden gösterimler. Normal ifade karakterleri tam bir listesi için bkz. [normal ifadeler](../../ide/using-regular-expressions-in-visual-studio.md).  
  
 Reset veya /e  
 İsteğe bağlı. Bulma seçenekleri varsayılan ayarlarına geri döndürür ve bir arama yapmaz.  
  
 / stop  
 İsteğe bağlı. Devam eden ise geçerli arama işlemini durdurur. Değiştir, diğer tüm bağımsız değişkenleri göz ardı eder, `/stop` belirtilmedi. Örneğin, geçerli değişiklik durdurmak için aşağıdaki girmeniz gerekir:  
  
```  
>Edit.ReplaceinFiles /stop  
```  
  
 / Sub seçeneklerini veya /s  
 İsteğe bağlı. Alt klasörleri içinde /lookin belirtilen dizin içinde arar:`searchpath` bağımsız değişken.  
  
 /text2 veya /2  
 İsteğe bağlı. Değiştirme işleminde sonuçlarını görüntüler **Bul sonuçları 2** penceresi.  
  
 /wild veya/l  
 İsteğe bağlı. Önceden tanımlanmış özel karakterleri kullanan `findwhat` bağımsız değişken olarak bir karakter ya da dizi karakteri temsil etmek için gösterimler.  
  
 /Word veya /w  
 İsteğe bağlı. Yalnızca tam sözcükleri arar.  
  
## <a name="example"></a>Örnek  
 Bu örnekte arar `btnCancel` ve ile değiştirir `btnReset` tüm .cls dosyaları, "visual studio Projelerim" klasöründe ve değiştirilen bilgileri görüntüler **Bul sonuçları 2** penceresi.  
  
```  
>Edit.ReplaceinFiles btnCancel btnReset /lookin:"c:/my visual studio projects" /ext:.cls /text2  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Metin bulma ve değiştirme](../../ide/finding-and-replacing-text.md)   
 [Dosyalarda Değiştir](../../ide/replace-in-files.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
