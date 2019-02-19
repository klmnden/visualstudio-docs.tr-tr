---
title: Varolan öğeyi Ekle komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- project.addexistingitem
helpviewer_keywords:
- File.AddExistingItem command
- Add Existing Item command
ms.assetid: 41f56131-d4c7-4f81-83b7-bdac713ea870
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 7686c4db4984188a4f8c4a52343f1386e9edd909
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54797843"
---
# <a name="add-existing-item-command"></a>Varolan Öğeyi Ekle Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Geçerli çözüme var olan bir dosya ekler ve onu açar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
File.AddExistingItem filename [/e:editorname]  
```  
  
## <a name="arguments"></a>Arguments  
 `filename`  
 Gerekli. Tam yol ve dosya adı, geçerli çözüme eklenecek öğe uzantısına sahip. Dosya yolu veya dosya adı boşluk içeriyorsa, yolun tamamını tırnak içine alın.  
  
## <a name="switches"></a>Anahtarlar  
 / e: `editorname`  
 İsteğe bağlı. Dosyanın açılmasını düzenleyicinin adı. Bağımsız değişken belirtildi, ancak hiçbir Düzenleyici adı verilmesi, **birlikte Aç** iletişim kutusu görüntülenir.  
  
 / E:`editorname` bağımsız değişkeni sözdizimini kullanan Düzenleyicisi adları gibi görünürler **ile iletişim kutusunu açma**tırnak işareti içine alınan. Örneğin, bir stil sayfası Kaynak Kod Düzenleyicisi'nde açmak için / e: şunları girersiniz`editorname` bağımsız değişken.  
  
```  
/e:"Source Code (text) Editor"  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Otomatik Tamamlama, doğru yol ve dosya adı, türü bulmaya çalışır.  
  
## <a name="example"></a>Örnek  
 Bu örnek dosyayı Form1.frm, geçerli çözüme ekler.  
  
```  
>File.AddExistingItem "C:\public\solution files\Form1.frm"  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
