---
title: 'Nasıl Yapılır: Ekleme listesi güvenliğini yapılandırma'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- permissions [Office development in Visual Studio
- inclusion lists [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: b13084a0010bef21283dc7890dd5b1064392e1b2
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53647741"
---
# <a name="how-to-configure-inclusion-list-security"></a>Nasıl Yapılır: Ekleme listesi güvenliğini yapılandırma
  Yönetici izinleriniz varsa, yapılandırabileceğiniz [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] denetlemek için son kullanıcıların Office çözümlerine güven kararı listesine kaydederek yükleme seçeneğiniz verilip verilmediğini güven istemi. Ekleme listeleri hakkında daha fazla bilgi için bkz. [ekleme listelerini kullanarak Office güven çözümleri](../vsto/trusting-office-solutions-by-using-inclusion-lists.md).  
  
 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]  
  
 Her beş bölgelerinin olan çözümler için aşağıdaki seçenekleri ayarlayabilirsiniz:  
  
-   Etkinleştirme [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] güven istemi anahtarını ve ekleme listesi. Son kullanıcıların herhangi bir sertifika ile imzalanmış Office çözümlerine güven verme izin verebilirsiniz.  
  
-   Kısıtlama [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] güven istemi anahtarını ve ekleme listesi. Yayımcı tanımlar, ancak zaten güvenilir değil bir sertifikayla imzalanmış Office çözümlerini yüklemek son kullanıcılara izin verebilirsiniz.  
  
-   Devre dışı [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] güven istemi anahtarını ve ekleme listesi. Son kullanıcılara açıkça güvenilir bir sertifika ile imzalanmamış herhangi bir Office çözümünü yüklenmesini engelleyebilir.  
  
## <a name="enable-the-inclusion-list"></a>Ekleme listesini etkinleştir  
 Bu bölgeden gelen herhangi bir Office çözümü çalıştırma ve yükleme seçeneğiyle sunulan son kullanıcıların istediğinizde bir bölgenin ekleme listesi etkinleştirin.  
  
### <a name="to-enable-the-inclusion-list-by-using-the-registry-editor"></a>Kayıt Defteri Düzenleyicisi'ni kullanarak ekleme listesini etkinleştirmek için  
  
1.  Kayıt Defteri Düzenleyicisi'ni açın:  
  
    1.  Tıklayın **Başlat**ve ardından **çalıştırma**.  
  
    2.  İçinde **açık** kutusuna **regedt32.exe**ve ardından **Tamam**.  
  
2.  Aşağıdaki kayıt defteri anahtarını bulun:  
  
     **\HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\\. NETFramework\Security\TrustManager\PromptingLevel**  
  
     Anahtar mevcut değilse oluşturun.  
  
3.  Aşağıdaki alt olarak eklemeniz **dize değeri**, zaten ilişkili değerleri mevcut değil.  
  
    |Dize değeri alt anahtarı|Değer|  
    |-------------------------|-----------|  
    |**Internet**|**AuthenticodeRequired**|  
    |**UntrustedSites**|**Devre dışı**|  
    |**Bilgisayarım**|**Etkin**|  
    |**LocalIntranet**|**Etkin**|  
    |**TrustedSites**|**Etkin**|  
  
     Varsayılan olarak, **Internet** değerine sahip **AuthenticodeRequired** ve **UntrustedSites** değerine sahip **devre dışı bırakılmış**.  
  
### <a name="to-enable-the-inclusion-list-programmatically"></a>Ekleme listelerini programlı olarak etkinleştirmek için  
  
1.  Visual Basic veya Visual oluşturma C# konsol uygulaması.  
  
2.  Açık *Program.vb* veya *Program.cs* dosya düzenleme için ve aşağıdaki kodu ekleyin.  
  
    ```vb  
    Dim key As Microsoft.Win32.RegistryKey  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\MICROSOFT\.NETFramework\Security\TrustManager\PromptingLevel")  
    key.SetValue("MyComputer", "Enabled")  
    key.SetValue("LocalIntranet", "Enabled")  
    key.SetValue("Internet", "AuthenticodeRequired")  
    key.SetValue("TrustedSites", "Enabled")  
    key.SetValue("UntrustedSites", "Disabled")  
    key.Close()  
    ```  
  
    ```csharp  
    Microsoft.Win32.RegistryKey key;  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\\MICROSOFT\\.NETFramework\\Security\\TrustManager\\PromptingLevel");  
    key.SetValue("MyComputer", "Enabled");  
    key.SetValue("LocalIntranet", "Enabled");  
    key.SetValue("Internet", "AuthenticodeRequired");  
    key.SetValue("TrustedSites", "Enabled");  
    key.SetValue("UntrustedSites", "Disabled");  
    key.Close();  
    ```  
  
3.  Derleme ve uygulamayı çalıştırın.  
  
## <a name="restrict-the-inclusion-list"></a>Ekleme listesini kısıtlamak  
 Ekleme listesi kısıtlayabilirsiniz, böylece çözümleri kullanıcılar için bir güven karar istenmeden önce kimlik bilinen Authenticode sertifikalar ile imzalanması gerekir.  
  
### <a name="to-restrict-the-inclusion-list"></a>Ekleme listesini kısıtlamak için  
  
1.  Kayıt Defteri Düzenleyicisi'ni açın:  
  
    1.  Tıklayın **Başlat**ve ardından **çalıştırma**.  
  
    2.  İçinde **açık** kutusuna **regedt32.exe**ve ardından **Tamam**.  
  
2.  Aşağıdaki kayıt defteri anahtarını bulun:  
  
     **\HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\\. NETFramework\Security\TrustManager\PromptingLevel**  
  
     Anahtar mevcut değilse oluşturun.  
  
3.  Aşağıdaki alt olarak eklemeniz **dize değeri**, zaten ilişkili değerleri mevcut değil.  
  
    |Dize değeri alt anahtarı|Değer|  
    |-------------------------|-----------|  
    |**UntrustedSites**|**Devre dışı**|  
    |**Internet**|**AuthenticodeRequired**|  
    |**Bilgisayarım**|**AuthenticodeRequired**|  
    |**LocalIntranet**|**AuthenticodeRequired**|  
    |**TrustedSites**|**AuthenticodeRequired**|  
  
     Varsayılan olarak, **Internet** değerine sahip **AuthenticodeRequired** ve **UntrustedSites** değerine sahip **devre dışı bırakılmış**.  
  
### <a name="to-restrict-the-inclusion-list-programmatically"></a>Program aracılığıyla ekleme listesini kısıtlamak için  
  
1.  Visual Basic veya Visual oluşturma C# konsol uygulaması.  
  
2.  Açık *Program.vb* veya *Program.cs* dosya düzenleme için ve aşağıdaki kodu ekleyin.  
  
    ```vb  
    Dim key As Microsoft.Win32.RegistryKey  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\MICROSOFT\.NETFramework\Security\TrustManager\PromptingLevel")  
    key.SetValue("MyComputer", "AuthenticodeRequired")  
    key.SetValue("LocalIntranet", "AuthenticodeRequired")  
    key.SetValue("Internet", "AuthenticodeRequired")  
    key.SetValue("TrustedSites", "AuthenticodeRequired")  
    key.SetValue("UntrustedSites", "Disabled")  
    key.Close()  
    ```  
  
    ```csharp  
    Microsoft.Win32.RegistryKey key;  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\\MICROSOFT\\.NETFramework\\Security\\TrustManager\\PromptingLevel");  
    key.SetValue("MyComputer", "AuthenticodeRequired");  
    key.SetValue("LocalIntranet", "AuthenticodeRequired");  
    key.SetValue("Internet", "AuthenticodeRequired");  
    key.SetValue("TrustedSites", "AuthenticodeRequired");  
    key.SetValue("UntrustedSites", "Disabled");  
    key.Close();  
    ```  
  
3.  Derleme ve uygulamayı çalıştırın.  
  
## <a name="disable-the-inclusion-list"></a>Ekleme listelerini devre dışı bırak  
 Son kullanıcılar yalnızca güvenilir ve bilinen bir sertifikayla imzalanmış çözümleri yükleyebilir, böylece ekleme listesi devre dışı bırakabilirsiniz.  
  
### <a name="to-disable-the-inclusion-list"></a>Ekleme listelerini devre dışı bırakmak için  
  
1.  Kayıt Defteri Düzenleyicisi'ni açın:  
  
    1.  Tıklayın **Başlat**ve ardından **çalıştırma**.  
  
    2.  İçinde **açık** kutusuna **regedt32.exe**ve ardından **Tamam**.  
  
2.  Bu zaten mevcut değilse, aşağıdaki kayıt defteri anahtarı oluşturun:  
  
     **\HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\\. NETFramework\Security\TrustManager\PromptingLevel**  
  
3.  Aşağıdaki alt olarak eklemeniz **dize değeri**, zaten ilişkili değerleri mevcut değil.  
  
    |Dize değeri alt anahtarı|Değer|  
    |-------------------------|-----------|  
    |**UntrustedSites**|**Devre dışı**|  
    |**Internet**|**Devre dışı**|  
    |**Bilgisayarım**|**Devre dışı**|  
    |**LocalIntranet**|**Devre dışı**|  
    |**TrustedSites**|**Devre dışı**|  
  
### <a name="to-disable-the-inclusion-list-programmatically"></a>Ekleme listelerini program aracılığıyla devre dışı bırakmak için  
  
1.  Visual Basic veya Visual oluşturma C# konsol uygulaması.  
  
2.  Açık *Program.vb* veya *Program.cs* dosya düzenleme için ve aşağıdaki kodu ekleyin.  
  
    ```vb  
    Dim key As Microsoft.Win32.RegistryKey  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\MICROSOFT\.NETFramework\Security\TrustManager\PromptingLevel")  
    key.SetValue("MyComputer", "Disabled")  
    key.SetValue("LocalIntranet", "Disabled")  
    key.SetValue("Internet", "Disabled")  
    key.SetValue("TrustedSites", "Disabled")  
    key.SetValue("UntrustedSites", "Disabled")  
    key.Close()  
    ```  
  
    ```csharp  
    Microsoft.Win32.RegistryKey key;  
    key = Microsoft.Win32.Registry.LocalMachine.CreateSubKey("SOFTWARE\\MICROSOFT\\.NETFramework\\Security\\TrustManager\\PromptingLevel");  
    key.SetValue("MyComputer", "Disabled");  
    key.SetValue("LocalIntranet", "Disabled");  
    key.SetValue("Internet", "Disabled");  
    key.SetValue("TrustedSites", "Disabled");  
    key.SetValue("UntrustedSites", "Disabled");  
    key.Close();  
  
    ```  
  
3.  Derleme ve uygulamayı çalıştırın.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Ekleme listelerini kullanarak Office çözümlerine güven](../vsto/trusting-office-solutions-by-using-inclusion-lists.md)   
 [Office çözümleri güvenliğini sağlama](../vsto/securing-office-solutions.md)  
  
  