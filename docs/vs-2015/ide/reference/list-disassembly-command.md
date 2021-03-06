---
title: Ayrıştırılmış kodu komut listesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- debug.listdisassembly
helpviewer_keywords:
- Debug.ListDisassembly command
- list disassembly command
ms.assetid: eb363e35-e86a-4121-966f-991210c27e2a
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: d361e5231d72df81fae164818bbe8341442c9f89
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68199180"
---
# <a name="list-disassembly-command"></a>Ayrıştırılmış Kodu Listele Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklama işlemini başlatır ve hataların nasıl işleneceğini belirtmenizi sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Debug.ListDisassembly [/count:number] [/endaddress:expression]  
[/codebytes:yes|no] [/source:yes|no] [/symbolnames:yes|no]  
[/linenumbers:yes|no]  
```  
  
## <a name="switches"></a>Anahtarlar  
 Her anahtar, formun tamamını veya bir kısa biçim kullanılarak çağrılabilir.  
  
 / count: `number` [veya] / c: `number` [veya] /length: `number` [veya] / l: `number`  
 İsteğe bağlı. Görüntülenecek yönerge sayısı. Varsayılan değer 8'dir.  
  
 /endaddress: `expression` [veya] / e: `expression`  
 İsteğe bağlı. Ayrıştırılmış kod durdurmak hangi adresi.  
  
 /codebytes:`yes` &#124; `no` [veya] /bytes:`yes` &#124; `no` [veya] / b:`yes`&#124;`no`  
 İsteğe bağlı. Kod baytlarını görüntülenip görüntülenmeyeceğini gösterir. Varsayılan değer `no`.  
  
 / source:`yes` &#124; `no` [veya] / s:`yes`&#124;`no`  
 İsteğe bağlı. Kaynak kodu görüntülenip görüntülenmeyeceğini gösterir. Varsayılan değer `no`.  
  
 /symbolnames:`yes` &#124; `no` [veya] /names:`yes` &#124; `no` [veya] / n:`yes`&#124;`no`  
 İsteğe bağlı. Sembol adları görüntülenip görüntülenmeyeceğini gösterir. Varsayılan değer `yes`.  
  
 [/ lınenumbers:`yes`&#124;`no`]  
 İsteğe bağlı. Kaynak koduyla ilişkili satır numaralarını görüntülemesini sağlar. / Source switch değerini içermelidir. `yes` /linenumbers anahtar kullanacak şekilde.  
  
## <a name="example"></a>Örnek  
  
```  
>Debug.ListDisassembly  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çağrı yığınını Listele komutu](../../ide/reference/list-call-stack-command.md)   
 [İş parçacıklarını Listele komutu](../../ide/reference/list-threads-command.md)   
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
