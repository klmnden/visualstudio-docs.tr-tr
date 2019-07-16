---
title: Başlangıç | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: b85d0fe9-f67a-4b7c-8d48-7eecf3f2dfe9
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 83dc76e3e92a05f936d94c8cd0f6a2b9b69e4cc1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68192824"
---
# <a name="start"></a>Başlat
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**Başlat** belirtilen profil oluşturma metodu için profil oluşturucuyu başlatır bir VSPerfCmd.exe seçenek bir seçenektir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
VSPerfCmd.exe /Start:Method /Output:FileName [Options]  
```  
  
#### <a name="parameters"></a>Parametreler  
 `Method`  
 Aşağıdaki anahtar sözcükler biri olmalıdır:  
  
- **İzleme** -izleme metodunu belirtir.  
  
- **ÖRNEK** -örnekleme yöntemini belirtir.  
  
- **KAPSAMI** -kod kapsamı belirtir.  
  
- **EŞZAMANLILIK** -kaynak çekişmesi yöntemini belirtir.  
  
## <a name="required-options"></a>Gerekli seçenekleri  
 **Çıkış** seçeneği olmalıdır belirtilen **Başlat** komut satırında belirtilen.  
  
 **Çıkış:** `filename`  
 Çıkış dosyası adını belirtir.  
  
## <a name="exclusive-options"></a>Dışlayan seçenekleri  
 Aşağıdaki seçenekler ile yalnızca kullanılabilir **Başlat** bir komut satırı seçeneği.  
  
 **CrossSession**&#124;**CS**  
 Etkinleştirir çapraz profil oluşturma işlem. Seçenek adları **CrossSession** ve **CS** desteklenen olan iki.  
  
 **Kullanıcı:** [`domain\`]`username`  
 İstemci erişimi belirtilen hesaptan izleyiciye sağlar.  
  
 **WinCounter:** `Path` [**Automark**:`n`]  
 **WinCounter** bir profil oluşturma veri dosyasını işareti olarak eklemek için bir Windows performans sayacı belirtir. **Otomatik işaret zamanının** veri dosyasının koleksiyonları arasındaki milisaniye olarak zaman aralığını belirtir.  
  
## <a name="invalid-options"></a>Geçersiz Seçenekler  
 Aşağıdaki seçenekler kullanılamaz **Başlat** bir komut satırı seçeneği.  
  
 **Status**  
 **Durum** profillenen bu işlemleri için geçerlidir. Bu işlemler, iş parçacıkları ve onların geçerli profil durumlarının (açık/kapalı) listeler. Örneğin, bir işlem durursa, **durumu** raporda belirtmez. **Durum** işlem ya da veya profil oluşturulan olduğunu gösterir.  
  
 **Kapatma**[ **:** `Timeout`]  
 Profil oluşturucuyu devre dışı bırakır.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek VSPerfCmd.exe kullanma işlemini gösterir **Başlat** seçeneği profil oluşturucu başlatılamadı.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)
