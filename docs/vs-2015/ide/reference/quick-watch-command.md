---
title: Hızlı Bakış komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- debug.quickwatch
helpviewer_keywords:
- Quick Watch command
- Debug.Quickwatch command
ms.assetid: 9670ac3a-8f2f-4874-974d-cb87d3b0cde1
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: d8ee0de9cad23b6208c9b015c65a8d9494821eae
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54789823"
---
# <a name="quick-watch-command"></a>Hızlı Bakış Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
İfade alanında seçilen veya belirtilen metni görüntüler [QuickWatch iletişim kutusu](http://msdn.microsoft.com/library/ffaee1dd-e5ce-4ef2-9401-d28329398867). Bir değişkenin veya ifadenin hata ayıklayıcı veya bir kaydın içeriğini tarafından tanınan geçerli değerini hesaplamak için bu iletişim kutusunu kullanabilirsiniz. Ayrıca, herhangi bir sabit olmayan değişken değeri veya herhangi bir kayıt içeriğini değiştirebilirsiniz.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Debug.QuickWatchq [text]  
```  
  
## <a name="arguments"></a>Arguments  
 `text`  
 İsteğe bağlı. Eklenecek metin **QuickWatch** iletişim kutusu.  
  
## <a name="remarks"></a>Açıklamalar  
 Varsa `text` olan atlanırsa, seçili durumdaki metni veya word imlecin İzle penceresine eklenir.  
  
## <a name="example"></a>Örnek  
  
```  
>Debug.QuickWatch  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: QuickWatch iletişim kutusunu kullanın](http://msdn.microsoft.com/library/ffaee1dd-e5ce-4ef2-9401-d28329398867)   
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
