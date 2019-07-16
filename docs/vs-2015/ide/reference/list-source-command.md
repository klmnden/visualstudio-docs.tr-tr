---
title: Liste kaynağı komutu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- Debug.ListSource
helpviewer_keywords:
- Debug.ListSource command
- list source command
- ListSource command
ms.assetid: e45f08d2-f4a3-49c3-9452-aa60508e2f74
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: e0a4a8482dc1c2c66a45902f2f3382b179b46b13
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68199124"
---
# <a name="list-source-command"></a>Kaynağı Listele Komutu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Belirtilen kaynak kodu satırlarını görüntüler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Debug.ListSource [/Count:number] [/Current] [/File:filename]  
[/Line:number] [/ShowLineNumbers:yes|no]  
```  
  
## <a name="switches"></a>Anahtarlar  
 / Sayısı:`number`  
 İsteğe bağlı. Görüntülenecek satır sayısını belirtir.  
  
 / Geçerli  
 İsteğe bağlı. Geçerli satırı gösterir.  
  
 / Dosya:`filename`  
 İsteğe bağlı. Gösterilecek dosyasının yolu. Dosya adı belirtilmezse, komut satırı geçerli deyimin için kaynak kodunu gösterir.  
  
 / Çizgi:`number`  
 İsteğe bağlı. Belirli bir satır numarasına gösterir.  
  
 / ShowLineNumbers:`yes|no`  
 İsteğe bağlı. Satır numaraları görüntülenip görüntülenmeyeceğini belirtir.  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="example"></a>Örnek  
 Bu örnekte, kaynak kodu satır numaralarını görünür olan Form1.vb, dosyanın 4 satırından listeler.  
  
```  
Debug.ListSource /File:"C:\Visual Studio Projects\Form1.vb" /Line:4 /ShowLineNumbers:yes  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut Penceresi](../../ide/reference/command-window.md)
