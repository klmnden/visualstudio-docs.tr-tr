---
title: Günlük komut penceresi komut çıktı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- tools.logcommandwindowoutput
helpviewer_keywords:
- log Command window output command
- View.LogCommandWindowOutput command
ms.assetid: d4ecec35-5af4-4954-8d60-2cd24583fbb4
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: be51445940816f0feffcbc7ba0e542e94d0f0648
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54791608"
---
# <a name="log-command-window-output-command"></a>Command penceresi çıktısı günlüğü tut komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Tüm giriş ve çıkış kopyaları **komut** penceresine bir dosya.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Tools.LogCommandWindowOutput [filename] [/on|/off] [/overwrite]  
```  
  
## <a name="arguments"></a>Arguments  
 `filename`  
 İsteğe bağlı. Günlük dosyasının adı. Varsayılan olarak, kullanıcı profili klasöründe bir dosya oluşturulur. Dosya adı zaten varsa, günlük varolan dosyanın sonuna eklenir. Dosya yok belirtilirse, belirtilen son dosya kullanılır. Önceki dosya varsa, cmdline.log adlı varsayılan günlük dosyası oluşturulur.  
  
> [!TIP]
>  Günlük dosyasına kaydedildiği konumu değiştirmek için yol boşluk içeriyorsa tırnak işareti içine alınmış dosyanın tam yolunu girin.  
  
## <a name="switches"></a>Anahtarlar  
 /on  
 İsteğe bağlı. Günlüğü başlar **komut** belirtilen dosya penceresinde ve yeni bilgiler ile dosya ekler.  
  
 / Kapalı  
 İsteğe bağlı. Günlüğü durdurur **komut** penceresi.  
  
 / overwrite  
 İsteğe bağlı. Dosyanın içinde belirtilen `filename` bağımsız değişken var olan bir dosya ile eşleşen, dosyanın üzerine yazılır.  
  
## <a name="remarks"></a>Açıklamalar  
 Dosya yok belirtilirse, dosya cmdline.log varsayılan olarak oluşturulur. Varsayılan olarak, bu komut için diğer ad günlüktür.  
  
## <a name="examples"></a>Örnekler  
 Bu örnek, yeni bir günlük dosyası cmdlog, oluşturur ve komut günlük başlatır.  
  
```  
>Tools.LogCommandWindowOutput cmdlog  
```  
  
 Bu örnek, oturum açma komutları durdurur.  
  
```  
>Tools.LogCommandWindowOutput /off  
```  
  
 Bu örnek komut daha önce kullanılan günlük dosyasında günlük sürdürür.  
  
```  
>Tools.LogCommandWindowOutput /on  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
