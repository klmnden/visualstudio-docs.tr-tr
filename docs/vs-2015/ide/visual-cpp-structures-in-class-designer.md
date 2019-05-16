---
title: Sınıf tasarımcısında Visual C++ yapılandırmaları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- Class Designer [Visual Studio], structures
ms.assetid: bad18ab6-d956-47a6-a413-811cc26db5f5
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: ed47509467bd8691b6f81dbd52fac47cf21c3715
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65698189"
---
# <a name="visual-c-structures-in-class-designer"></a>Sınıf Tasarımcısında Visual C++ Yapılandırmaları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Sınıf Tasarımcısı, anahtar sözcüğü ile bildirilen C++ yapıları destekleyen `struct`. Bir örneği verilmiştir:  
  
```  
struct MyStructure  
{  
   char a;  
   int i;  
   long j;  
};  
```  
  
 Kullanma hakkında daha fazla bilgi için `struct` yazın, bkz: [yapı](https://msdn.microsoft.com/library/3c6ba273-e248-4ff1-8c69-d2abcf1263c6).  
  
 Sınıf diyagramında C++ yapı şeklinde görünür ve etiketi dışında sınıf şeklinin gibi çalışır **yapı** ve yuvarlak köşeler yerine dörtgen köşelerine sahiptir.  
  
|Kod öğesi|Sınıf Tasarımcısı görünümü|  
|------------------|-------------------------|  
|`struct StructureName {};`|**StructureName**<br /><br /> Yapı|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual C++ kodu (Sınıf Tasarımcısı) ile çalışma](../ide/working-with-visual-cpp-code-class-designer.md)   
 [Sınıflar ve yapılar](https://msdn.microsoft.com/library/516dd496-13fb-4f17-845a-e9ca45437873)   
 [struct](https://msdn.microsoft.com/library/3c6ba273-e248-4ff1-8c69-d2abcf1263c6)
