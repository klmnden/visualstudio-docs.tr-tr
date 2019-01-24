---
title: 'Nasıl yapılır: Oluşturma bir. Vsct mevcut bir dosya. Cto dosya | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: devlang-csharp
ms.topic: conceptual
helpviewer_keywords:
- VSCT files, creating based on a .cto file
ms.assetid: 847717c9-477d-4ac9-8b2c-2da878912478
caps.latest.revision: 11
manager: jillfra
ms.openlocfilehash: 91c1527de5a5af57602350f317507f97bac53810
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54754999"
---
# <a name="how-to-create-a-vsct-file-from-an-existing-cto-file"></a>Nasıl yapılır: Oluşturma bir. Vsct mevcut bir dosya. Cto dosyası
Var olan bir ikili .cto dosyasından bir XML tabanlı .vsct dosyası oluşturabilirsiniz. Bunun yapılması, yeni komut tablosu derleyici biçimi yararlanmak sağlar. Bu işlem, .cto dosya .ctc dosyasından derlenen bile çalışır. Düzenle ve başka bir .cto dosyasına .vsct dosyası derleme.  
  
### <a name="to-create-a-vsct-file-from-a-cto-file"></a>Bir .cto dosyasından .vsct dosyası oluşturmak için  
  
1.  .Cto dosyası ve karşılık gelen .ctsym dosyası bir kopyasını edinin.  
  
2.  Dosyaları vsct.exe derleyici ile aynı dizine koyun.  
  
3.  Visual Studio komut isteminde .cto ve .ctsym dosyaları içeren dizine gidin.  
  
4.  Tür **vsct.exe** _ctofilename_**.cto** _vsctfilename_**.vsct -S**  _symfilename_**.ctsym**.  
  
     `ctofilename` .cto dosyanın adıdır `vsctfilename` oluşturmak istediğiniz vsct dosya adıdır ve `symfilename` .ctsym dosyanın adıdır.  
  
     Bu işlem yeni bir .vsct XML komut tablosu derleyici dosyası oluşturur. Düzenle ve diğer .vsct dosyası gibi dosya vsct.exe, vsct derleyici ile derleyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Oluşturma bir. Vsct dosyası](../extensibility/internals/how-to-create-a-dot-vsct-file.md)   
 [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)