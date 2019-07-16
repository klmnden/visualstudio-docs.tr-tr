---
title: Bellek komut listesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- debug.listmemory
helpviewer_keywords:
- Debug.ListMemory command
- ListMemory command
- list memory command
ms.assetid: a84de361-a6a6-4f6d-96aa-a0d4a424371e
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 884dda624d5405ec017b544afd223be0bebc97e9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68199166"
---
# <a name="list-memory-command"></a>Belleği Listele Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Belirtilen bellek aralığının içeriklerini görüntüler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Debug.ListMemory [/ANSI|Unicode] [/Count:number] [/Format:formattype]  
[/Hex|Signed|Unsigned] [expression]  
```  
  
## <a name="arguments"></a>Arguments  
 `expression`  
 İsteğe bağlı. Bellek görüntüleme başlayacağı bellek adresi.  
  
## <a name="switches"></a>Anahtarlar  
 / ANSI&#124;Unicode  
 İsteğe bağlı. Bellek, bellek, ANSI veya Unicode bayt için karşılık gelen karakter olarak görüntüler.  
  
 / Sayısı:`number`  
 İsteğe bağlı. Başlangıç belleği görüntülemek için kaç bayt belirler `expression`.  
  
 / Biçimi:`formattype`  
 İsteğe bağlı. Biçim türü bellek bilgileri görüntülemek için **bellek** penceresi; Mayıs OneByte, TwoBytes, FourBytes, EightBytes olabilir, Float (32-bit) veya çift (64-bit). OneByte kullanılıyorsa `/Unicode` kullanılamıyor.  
  
 / Onaltılık&#124;imzalı&#124;işaretsiz  
 İsteğe bağlı. Numaraları görüntüleme biçimini belirtir: olarak işaretli, imzasız veya onaltılık.  
  
## <a name="remarks"></a>Açıklamalar  
 Eksiksiz bir yazmak yerine **Debug.ListMemory** komut tüm anahtarların ile önceden tanımlanmış diğer adlar için belirtilen değerler önceden belirli anahtarları komutu çağırır. Örneğin, girmek yerine:  
  
```  
>Debug.ListMemory /Format:float /Count:30 /Unicode  
```  
  
 şunu yazabilirsiniz:  
  
```  
>df /Count:30 /Unicode  
```  
  
 İşte bir listesi için kullanılabilir diğer adlar, **Debug.ListMemory** komutu:  
  
|Alias|Komut ve anahtarlar|  
|-----------|--------------------------|  
|**d**|Debug.ListMemory|  
|**da**|Debug.ListMemory /Ansi|  
|**DB**|Debug.ListMemory /Format:OneByte|  
|**DC**|Debug.ListMemory /Format:FourBytes /Ansi|  
|**dd**|Debug.ListMemory /Format:FourBytes|  
|**SD**|Debug.ListMemory /Format:Float|  
|**dq**|Debug.ListMemory /Format:EightBytes|  
|**DU**|Debug.ListMemory / Unicode|  
  
## <a name="example"></a>Örnek  
  
```  
>Debug.ListMemory /Format:float /Count:30 /Unicode  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çağrı yığınını Listele komutu](../../ide/reference/list-call-stack-command.md)   
 [İş parçacıklarını Listele komutu](../../ide/reference/list-threads-command.md)   
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
