---
title: 'Nasıl yapılır: .NET Framework kaynağında hata ayıklama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugging, .NET Framework source
ms.assetid: fc12e472-ac6a-4e77-8e22-a769e13a03b8
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 49b13b8406dc96e8e7ebe5e79e26c5da02e8a53a
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60092116"
---
# <a name="how-to-debug-net-framework-source"></a>Nasıl yapılır: .NET Framework kaynağında hata ayıklama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

En son sürümünü [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] yeni özellikler için sağladığı [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] hata ayıklama. Hata ayıklamak için [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] kaynak kod için hata ayıklama erişimi olması gerekir. İçine adımlamak gerekir [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] kaynak.  
  
 Etkinleştirebilirsiniz [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] atlama ve sembol karşıdan **seçenekleri** iletişim kutusu. Simge indirmeyi etkinleştirdiğinizde, simgeleri hemen indirmeyi veya yalnızca daha sonra indirme seçeneğini etkinleştirmek seçebilirsiniz. Simgeleri hemen karşıdan yüklemezseniz, uygulamanızın hatalarını ayıklama sonraki defa başlattığınızda semboller indirilir. Ayrıca el ile indirilerek yapabilirsiniz **modülleri** penceresi veya **çağrı yığını** penceresi.  
  
### <a name="to-enable-net-framework-source-debugging"></a>.NET Framework kaynak hata ayıklamayı etkinleştirmek için  
  
1. Üzerinde **Araçları** menüsünü tıklatın **seçenekleri**.  
  
2. İçinde **seçenekleri** iletişim kutusu, tıklayın **hata ayıklama** kategorisi.  
  
3. İçinde **genel** kutusunda, ayarlama **.NET Framework etkinleştir** kaynak Adımlamayı.  
  
    1. Yalnızca kendi kodum tablonuz varsa bir uyarı iletişim kutusu, yalnızca kendi kodum şimdi devre dışı olduğunu bildirir. **Tamam**'ı tıklatın.  
  
    2. Bir sembol önbelleği konumunun ayarlanmış yoksa başka bir uyarı iletişim kutusunda varsayılan sembol önbelleği konumunun artık ayarlanmış olduğunu bildirir. **Tamam**'ı tıklatın.  
  
4. Altında **hata ayıklama** kategorisini tıklatın **sembolleri**.  
  
5. Sembolleri değiştirmek istiyorsanız konumu önbelleğe alın:  
  
    1. Açık **hata ayıklama** kutusunda soldaki düğümünün.  
  
    2. Altında **hata ayıklama** düğümünü tıklatın **sembolleri**.  
  
    3. İçinde konumu düzenleyin **sembolleri sembol sunucularından bu dizine önbelleğe** veya **Gözat** bir konum seçin.  
  
6. Simgeleri hemen karşıdan yüklemek isterseniz, **yukarıdaki konumları kullanarak simgeleri Yükle**.  
  
     Bu düğme Tasarım modunda kullanılamaz.  
  
     Sembolleri şimdi karşıdan seçmezseniz, programınızın hatalarını ayıklamayı sonraki defa başlattığınızda semboller otomatik olarak indirilir.  
  
7. Tıklayın **Tamam** kapatmak için **seçenekleri** iletişim kutusu.  
  
### <a name="to-load-framework-symbols-using-the-modules-window"></a>Modüller penceresini kullanarak çerçeve simgeleri yüklemek için  
  
1. İçinde **modülleri** penceresinde, simgelerin yüklenmediği modülü sağ tıklatın. Sembol yüklenmedi veya bakarak değil söyleyebilirsiniz **simge durumu** sütun.  
  
2. İşaret **sembolleri şuradan Yükle** tıklatıp **Microsoft sembol sunucuları** Microsoft ortak semboller sunucusundan semboller indirmek için veya **sembol yolu** bir dizinden yüklemek için daha önce sembolleri depoladığınız.  
  
### <a name="to-load-framework-symbols-using-the-call-stack-window"></a>Çağrı yığını penceresini kullanarak çerçeve simgeleri yüklemek için  
  
1. İçinde **çağrı yığını** penceresinde, simgelerin yüklenmediği Çerçeveyi sağ tıklatın. Çerçeve soluk görünecektir.  
  
2. İşaret **sembolleri şuradan Yükle** tıklatıp **Microsoft sembol sunucuları** veya **sembol yolu**.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yönetilen kodda hata ayıklama](../debugger/debugging-managed-code.md)   
 [Simge (.pdb) ve Kaynak Dosyaları Belirtme](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)
