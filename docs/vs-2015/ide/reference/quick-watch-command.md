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
ms.openlocfilehash: c9ac805ebea19604343d561bf553448fff2ca575
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65701741"
---
# <a name="quick-watch-command"></a>Hızlı Bakış Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

İfade alanında seçilen veya belirtilen metni görüntüler [QuickWatch iletişim kutusu](https://msdn.microsoft.com/library/ffaee1dd-e5ce-4ef2-9401-d28329398867). Bir değişkenin veya ifadenin hata ayıklayıcı veya bir kaydın içeriğini tarafından tanınan geçerli değerini hesaplamak için bu iletişim kutusunu kullanabilirsiniz. Ayrıca, herhangi bir sabit olmayan değişken değeri veya herhangi bir kayıt içeriğini değiştirebilirsiniz.  
  
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
 [Nasıl yapılır: QuickWatch iletişim kutusunu kullanın](https://msdn.microsoft.com/library/ffaee1dd-e5ce-4ef2-9401-d28329398867)   
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
