---
title: Bul-komut kutusu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
f1_keywords:
- vs.findcommandbox
helpviewer_keywords:
- Find/Command box
ms.assetid: c81736dd-7a26-4e11-95c8-c2a2e56d7a41
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: b8bddc27eb4a59b65796c7837ae4561e5d56a5d5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68160666"
---
# <a name="findcommand-box"></a>Bul/Komut Kutusu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Arama metni ve Visual Studio komutları çalıştırmak **Bul/komut** kutusu. **Bul/komut** kutusu araç çubuğu denetimi olarak hala kullanılabilir, ancak artık varsayılan olarak görünür. Görüntüleyebileceğiniz **Bul/komut** kutusunu **Düğme Ekle veya Kaldır** üzerinde **standart** araç çubuğu ve ardından **Bul**.  
  
 Çalıştırılacak bir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] komutu, büyüktür (>) işareti ile başlayın.  
  
 **Bul/komut** kutusuna girilen son 20 öğe korur ve bunları bir aşağı açılan listede görüntüler. Listede ilerleyin ok tuşlarını seçerek gidebilirsiniz.  
  
 ![Bulma&#47;komut kutusu](../ide/media/findcommandbox.png "FindCommandBox")  
Bul/Komut Kutusu  
  
## <a name="searching-for-text"></a>Metin arama  
 Varsayılan olarak metin belirttiğinizde **Bul/komut** kutusuna ve ardından ENTER TUŞUNA basın anahtar, Visual Studio içinde belirtilen seçenekleri kullanarak geçerli belge veya araç penceresinin arar **dosyalardaBul**iletişim kutusu. Daha fazla bilgi için [bulma ve değiştirme metnini](../ide/finding-and-replacing-text.md).  
  
## <a name="entering-commands"></a>Komutlar girme  
 Kullanılacak **Bul/komut** tek bir sorun için onay kutusunu [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] komutunu ya da diğer adı yerine arama için metin girin [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] büyüktür (>) bir simgeyle başında komutu. Örneğin:  
  
```  
>File.NewFile c:\temp\MyFile /t:"General\Text File"  
```  
  
 Alternatif olarak, girin ve tek veya birden çok komut yürütmek için komut penceresini kullanabilirsiniz. Bazı komutlar veya diğer adlar girilen ve kendileri tarafından yürütülen; diğerleri kendi sözdizimi değişkenlerinde gerek duyarlar. Bağımsız değişkenlere sahip komutları listesi için bkz. [Visual Studio komutları](../ide/reference/visual-studio-commands.md).  
  
## <a name="escape-characters"></a>Kaçış karakterleri  
 Aşağıdaki yerine birebir yorumlandığı bir denetim karakteri olarak yorumlanır hemen komut satırında bir şapka (^) karakter, karakter anlamına gelir. Bu anahtar adları dışında bir parametre veya anahtar değerine düz tırnak ("), boşluk, önde gelen eğik çizgiler, düzeltme işaretleri veya diğer bir hazır bilgi karakterleri katıştırmak için kullanılabilir. Örneğin,  
  
```  
>Edit.Find ^^t /regex  
```  
  
 İç veya dış tırnak işaretleri olup olmadığını şapka işareti aynı şekilde çalışır. Şapka işareti satırdaki son karakterse, yoksayılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Komut penceresi](../ide/reference/command-window.md)   
 [Metin Bulma ve Değiştirme](../ide/finding-and-replacing-text.md)
