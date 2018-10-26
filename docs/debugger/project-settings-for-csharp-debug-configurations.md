---
title: Proje ayarları C# hata ayıklama yapılandırmaları için | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debug configurations, C#
- project settings [Visual Studio], debug configurations
- debug builds, project settings
- projects [Visual Studio], debug configurations
- project configurations, debug
- debugging [C#], debugger settings
ms.assetid: e30ca810-66e9-4d6e-9cf6-9f285cd0b100
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: a65928e8a5a734e84d51cbb4368c7346ba8c2edb
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49896347"
---
# <a name="project-settings-for--c-debug-configurations"></a>C# Hata Ayıklama Yapılandırması Proje Ayarları
Bir C# hata ayıklama yapılandırması proje ayarları değiştirebilirsiniz **özellik sayfaları** anlatıldığı gibi penceresinde [hata ayıklama ve yayın yapılandırmaları](../debugger/how-to-set-debug-and-release-configurations.md). Aşağıdaki tablolarda, hata ayıklayıcı ile ilgili ayarların nerede bulunacağı gösterilmektedir **özellik sayfaları** penceresi.  
  
> [!WARNING]
>  Bu konu, UWP uygulamaları için geçerli değil. Bkz: [(VB, C#, C++ ve XAML) bir hata ayıklama oturumu başlatın](../debugger/start-a-debugging-session-for-a-store-app-in-visual-studio-vb-csharp-cpp-and-xaml.md)  
  
##  <a name="BKMK_Debug_tab"></a> Hata ayıklama sekmesi  
  
| **Ayarı** | **Açıklama** |
|-------------------------------------| - |
| **Yapılandırma** | Uygulama derlemek için modu ayarlar. Arasından seçim **etkin (hata ayıklama)**, **hata ayıklama**, **yayın**, **yapılandırmalarında**. |
| **Başlatma eylemi** | Bu grubu denetimleri, hata ayıklama menüsünden Başlangıç meydana gelir eylemi belirtir.<br /><br /> -   **Proje başlangıç** varsayılandır ve hata ayıklama için başlangıç projesi başlatır. Daha fazla bilgi için [başlangıç projesi seçme](/previous-versions/visualstudio/visual-studio-2010/0s590bew(v=vs.100)).<br />-   **Harici program Başlat** başlatmak ve olmayan bir programa ekledikten sağlayan parçası olan bir [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] proje. Daha fazla bilgi için [çalışan programa ekleme](/previous-versions/visualstudio/visual-studio-2010/c6wf8e4z(v=vs.100)).<br />-   **URL'de tarayıcı başlatmak** bir Web uygulaması ayıklamanızı sağlar. |
| **Komut satırı bağımsız değişkenleri** | Ayıklanacak programın komut satırı bağımsız değişkenlerini belirtir. Komut başlangıç dış program içinde belirtilen program adı addır. Başlatma eylemi için başlangıç URL'si olarak ayarlanırsa, komut satırı bağımsız değişkenleri belirtilemez. |
| **Çalışma dizini** | Ayıklanan programın çalışma dizini belirtir. İçinde [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)], çalışma dizini uygulama \bin\debug varsayılan olarak başlatıldığında dizindir. |
| **Uzak makine kullanma** | Hata ayıklama amacıyla nerede uygulamanın çalışacağı uzak bir makine adı veya bir [Msvsmon sunucu adı](../debugger/remote-debugging.md). Uzak makinede EXE konumunu, yapılandırma özellikleri klasöründe, yapı kategori çıkış yolu özelliği tarafından belirtilir. Konum, uzak makinede paylaşılabilir bir dizin olmalıdır. |
| **Yönetilmeyen kodun hata ayıklamasını etkinleştir** | Yerel (yönetilmeyen) Win32 koddaki çağrıları yönetilen uygulamanızın hatalarını ayıklamanızı sağlar. |
| **SQL Server hata ayıklamayı etkinleştir** | SQL Server veritabanı nesnelerini hata ayıklamasını sağlar. |
  
##  <a name="BKMK_Build_tab"></a> Derleme sekmesi  
  
|Ayar|Açıklama|  
|-------------|-----------------|  
|**Koşullu derleme simgeleri:**|Hata ayıklama ve izleme sabitler burada tanımlanır.<br /><br /> Bu sabitler koşullu derlenmesini etkinleştirmek [hata ayıklama sınıfı](/dotnet/api/system.diagnostics.debug) ve [izleme sınıfı](/dotnet/api/system.diagnostics.trace). Tanımlanan Bu sabitler ile hata ayıklama ve izleme sınıfı yöntemleri oluşturmak için çıkış [çıkış penceresine](../ide/reference/output-window.md). Bu sabitler olmadan hata ayıklama ve izleme sınıfı yöntemleri derlenmemiş ve hiçbir çıktı oluşturulur.<br /><br /> -Debug normalde bir program hata ayıklama sürümünde tanımlanır ve sürümde tanımlanmamış.<br />-İzleme, hem hata ayıklama ve yayın sürümleri normal olarak tanımlanır.|  
|**Kodu En İyileştir**|Yalnızca en iyi duruma getirilmiş kodda görüntülenen bir hatayı Bul sürece, bu ayar hata ayıklama sürümünde devre dışı bırakmanız gerekir. En iyi duruma getirilmiş kodu doğrudan deyimlerinde kaynak windows için yönergeler karşılık gelmediğinden hata ayıklamak zordur.|  
|**Çıkış yolu:**|Genellikle bin\Debug hata ayıklama için ayarlayın.|

> [!NOTE]
> Bulma, hata ayıklama seçenekleri hakkında daha fazla bilgi için **Gelişmiş** düğmesi, bkz: [Gelişmiş derleme Ayarları iletişim kutusu (C#)](../ide/reference/advanced-build-settings-dialog-box-csharp.md). Taşınabilir sembol (.pdb) dosyaları için en son platformlar arası .NET Core için biçimdir. 
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklayıcısı Ayarları ve Hazırlığı](../debugger/debugger-settings-and-preparation.md)