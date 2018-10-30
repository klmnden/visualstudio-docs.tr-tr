---
title: 'Nasıl yapılır: .NET Framework kaynağında hata ayıklama | Microsoft Docs'
ms.custom: ''
ms.date: 02/23/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- debugging, .NET Framework source
ms.assetid: fc12e472-ac6a-4e77-8e22-a769e13a03b8
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: c06a2328987201198bc2d5d15a4788d2a821d7b6
ms.sourcegitcommit: d462dd10746624ad139f1db04edd501e7737d51e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50219126"
---
# <a name="how-to-debug-net-framework-source"></a>Nasıl Yapılır: .NET Framework Kaynağında Hata Ayıklama
.NET Framework kaynağında hata ayıklamak için kod için hata ayıklama için erişimi olmalıdır. Ayrıca .NET Framework kaynağına ilerlemesine adımlamak gerekir.  
  
 .NET Framework etkinleştirebilirsiniz atlama ve sembol karşıdan **seçenekleri** iletişim kutusu. Simge indirmeyi etkinleştirdiğinizde, simgeleri hemen indirmeyi veya yalnızca daha sonra indirme seçeneğini etkinleştirmek seçebilirsiniz. Simgeleri hemen karşıdan yüklemezseniz, uygulamanızın hatalarını ayıklama sonraki defa başlattığınızda semboller indirilir. Ayrıca el ile indirilerek yapabilirsiniz **modülleri** penceresi veya **çağrı yığını** penceresi.  
  
### <a name="to-enable-net-framework-source-debugging"></a>.NET Framework kaynak hata ayıklamayı etkinleştirmek için  
  
1.  Üzerinde **Araçları** menüsünü tıklatın **seçenekleri**.  
  
2.  İçinde **seçenekleri** iletişim kutusu, tıklayın **hata ayıklama** kategorisi.  
  
3.  İçinde **genel** kutusu olarak ayarlayın **etkinleştirme .NET Framework kaynak Adımlamayı.**  
  
    1.  Yalnızca kendi kodum tablonuz varsa bir uyarı iletişim kutusu, yalnızca kendi kodum şimdi devre dışı olduğunu bildirir. **Tamam**'ı tıklatın.  
  
    2.  Bir sembol önbelleği konumunun ayarlanmış yoksa başka bir uyarı iletişim kutusunda varsayılan sembol önbelleği konumunun artık ayarlanmış olduğunu bildirir. **Tamam**'ı tıklatın.  
  
4.  Altında **hata ayıklama** kategorisini tıklatın **sembolleri**.  
  
5.  Sembol önbellek konumunu değiştirmek istiyorsanız, içinde konumu düzenleyin **önbellek sembolleri bu dizinde** veya **Gözat** bir konum seçin.  
  
6.  Simgeleri hemen karşıdan yüklemek isterseniz, **yukarıdaki konumları kullanarak simgeleri Yükle**.  
  
     Bu düğme Tasarım modunda mevcut değildir, ancak hata ayıklarken kullanılabilir.  
  
     Sembolleri şimdi karşıdan seçmezseniz, programınızın hatalarını ayıklamayı sonraki defa başlattığınızda semboller otomatik olarak indirilir.  
  
7.  Tıklayın **Tamam** kapatmak için **seçenekleri** iletişim kutusu.  
  
### <a name="to-load-framework-symbols-using-the-modules-window"></a>Modüller penceresini kullanarak çerçeve simgeleri yüklemek için  
  
1.  İçinde **modülleri** penceresini (hata ayıklama sırasında seçin **hata ayıklama** > **Windows** > **modülleri**), bir modül için semboller yüklü olmadığından sağ tıklayın. Sembol yüklenmedi veya bakarak değil söyleyebilirsiniz **simge durumu** sütun.  
  
2.  İşaret **sembol ayarları** tıklatıp **Microsoft sembol sunucuları** Microsoft ortak semboller sunucusundan semboller indirmek için. Modülü sağ tıklatın ve seçin **yük sembolleri** daha önce depoladığınız sembolleri bir dizinden yüklemek için.  
  
### <a name="to-load-framework-symbols-using-the-call-stack-window"></a>Çağrı yığını penceresini kullanarak çerçeve simgeleri yüklemek için  
  
1.  İçinde **çağrı yığını** penceresinde, simgelerin yüklenmediği Çerçeveyi sağ tıklatın. Çerçeve soluk görünecektir.  
  
2.  İşaret **sembol ayarları** tıklatıp **Microsoft sembol sunucuları**, modülü sağ tıklatın ve seçin **sembol yolu**.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yönetilen kodda hata ayıklama](../debugger/debugging-managed-code.md)   
 [Simge (.pdb) ve Kaynak Dosyaları Belirtme](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)