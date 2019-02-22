---
title: 'Nasıl yapılır: Başvuru Windows bilgi simgesi | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- performance tools, symbol servers
- servers, symbol servers
- profiling tools, symbol servers
- symbol servers
ms.assetid: b7c67318-6be2-4b1e-a161-077b1f4a7c30
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 347b35a1ed47236c0d6e6c187224ee50fd79852c
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56619894"
---
# <a name="how-to-reference-windows-symbol-information"></a>Nasıl yapılır: Başvuru Pencereleri sembol bilgileri
Visual Studio profil oluşturma araçları simgesini kullanın (. *pdb*) dosyaları gibi sembolik adları çözümlemek için işlev adlarını program ikili dosyaları. Otomatik olarak indirip doğru güncelleştirmek için aşağıdaki adımları izleyebilirsiniz. *pdb* dosyaları yerel bilgisayarda Windows sürümü için.

> [!NOTE]
>  Bu ayar, var olan raporların etkilemez. Sembol sunucusu belirttikten sonra oluşturulan raporlar sembol bilgilerini sahip olur.

 Daha fazla bilgi için [belirtin simge (. *pdb*) ve kaynak dosyaları](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md).

### <a name="to-use-the-microsoft-symbol-server"></a>Microsoft sembol sunucusu kullanmak için

1.  C:\SymbolCache gibi sembol dosyası bilgilerini içeren bir klasör oluşturun.

2.  Üzerinde **Araçları** menüsünü tıklatın **seçenekleri**.

     **Seçenekleri** iletişim kutusu görüntülenir.

3.  Genişletin **hata ayıklama** ağaç ve ardından **sembolleri**.

4.  İçinde **sembol dosyası (.pdb) konumlar**seçin **Microsoft sembol sunucuları**

5.  İçinde **semboller sembol sunucusundan bu dizine önbelleğe**, örneğin, 1. adımda oluşturduğunuz klasör yolunu yazın:

     **C:\SymbolCache**

     Üç nokta düğmesine de tıklayabilirsiniz (**...** ) seçip bir dizinden **klasöre Gözat** iletişim kutusu.

## <a name="see-also"></a>Ayrıca bkz.
- [Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)
- [Nasıl yapılır: Sembol bilgilerini seri hale getirme](../profiling/how-to-serialize-symbol-information.md)