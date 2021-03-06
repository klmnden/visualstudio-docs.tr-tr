---
title: Satırlar görünümü - örnekleme verileri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Lines view
ms.assetid: 46497249-c797-42c5-a02c-3e4bb3b4ee60
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a2e5511e9e2e1c863db8f696a70195573d75429f
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63433866"
---
# <a name="lines-view---sampling-data"></a>Satırlar Görünümü - Örnekleme Verileri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Profil oluşturma örnek toplanmadı olduğunda yürüten deyimleri için performans verilerini örnekleme verileri görünümünü listeler satırları çalıştırın.  
  
> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. Windows Store apps ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
 Bir kaynak dosyasında bir deyimi kaynak dosyasında birden fazla satırı kapsayabilir ve tek bir satır birden fazla deyim içerebilir. Bir deyimi aşağıdaki tarafından tanımlanır:  
  
- Function deyimi içeren kaynak dosyası.  
  
- Deyimi içeren işlev.  
  
- Kaynak satırı deyim başlar.  
  
- Deyim başladığı kaynak satırı karakter.  
  
- Kaynak satırı başlangıçtan deyimini sonlandırır.  
  
- Deyim erdiği kaynak satırı karakter.  
  
  Satır adı sütunu tanımlayıcısı veri sıralanabilir bir birleşimini sağlar.  
  
  Tanımı gereği, diğer işlevler bir deyim çağırmaz. Bu nedenle, yalnızca özel değerler listelenmiştir.  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**İşlem kimliği**|İşlem, profil oluşturma çalışması Kimliğine (PID).|  
|**İşlem adı**|İşlemin adı.|  
|**Modül adı**|İşlev satır içeren modül adı.|  
|**Modül yolu**|İşlev satır içeren modül yolu.|  
|**Kaynak dosyası**|İşlev satır içeren kaynak dosyası.|  
|**İşlev adı**|İşlevin adı.|  
|**İşlevin satır numarası**|Satır numarası kaynak dosyada bu işlevin başlangıcı.|  
|**İşlev adresi**|İşlev başlangıç adresi.|  
|**Kaynak satır başlangıcı**|Bu örnek, toplanan kaynak dosyadaki başlangıç satır numarası.|  
|**Kaynak satır sonu**|Bitiş satır numarası kaynak dosyada, bu örnek toplanmadı.|  
|**Kaynak karakter başlangıcı**|Bu örnek, toplanan kaynak dosya satırında başlangıç karakteri uzaklığı.|  
|**Kaynak karakter sonu**|Bu örnek, toplanan kaynak dosya satırdaki bitiş karakter uzaklığı.|  
|**Satır adı**|Profil Oluşturucu tarafından oluşturulan bir satırın aşağıdaki sözdizimiyle tanıtıcısı:`Source File`**; [**  `Line Number Start` **,**`Character Start`**] ->; [** `Line Number End`**,**`Character End`**]**|  
|**Dışlamalı örnekler**|İşlev satır yürütülürken, toplanan örneklerin toplam sayısı.|  
|**Dışlamalı örnek yüzdesi**|İşlev satır yürütülürken, toplanmış olan profil oluşturma, tüm örneklerin yüzdesi.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Satırlar Görünümü- Örnekleme](../profiling/lines-view-dotnet-memory-sampling-data.md)
