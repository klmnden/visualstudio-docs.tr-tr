---
title: Anlık görüntü hata ayıklama ile ilgili SSS | Microsoft Docs
ms.date: 11/07/2017
ms.topic: reference
helpviewer_keywords:
- debugger
ms.assetid: 944f1eb0-a74b-4d28-ae2b-a370cd869add
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 43b76ad81a2c075a11ff55dcbd7fbc5e8a4b3fe7
ms.sourcegitcommit: ba5e072c9fedeff625a1332f22dcf3644d019f51
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/31/2019
ms.locfileid: "66431845"
---
# <a name="frequently-asked-questions-for-snapshot-debugging-in-visual-studio"></a>Sık sorulan Visual Studio'da anlık görüntü hatalarını ayıklama sorular

Snapshot Debugger'ı kullanarak canlı Azure uygulamalarında hata ayıklaması yaparken sorulan sorular listesi aşağıda verilmiştir.

#### <a name="what-is-the-performance-cost-of-taking-a-snapshot"></a>Bir anlık görüntü alma performans maliyeti nedir?

Snapshot Debugger, uygulamanızın bir anlık görüntüsünü yakalar, uygulamanın işlem çatallar ve çatalı oluşturulan kopya askıya alır. Anlık görüntü hata ayıklaması yaparken, işlem çatalı kopyasını karşı ayıkladığınız. Bu işlem yalnızca 10-20 milisaniye ancak tam bir yığın Uygulamanın kopyalamaz. Bunun yerine, yalnızca sayfa tablosu kopyalar ve sayfalarını yazma kopyalamak için ayarlar. Uygulamanızın nesnelerin yığın değişiklik bazıları varsa, bunların ilgili sayfalarını ardından kopyalanır. Her anlık görüntü bir küçük (bazında çoğu uygulama için kilobayt yüzlerce) maliyet belleğe sahip whey olmasıdır.

#### <a name="what-happens-if-i-have-a-scaled-out-azure-app-service-multiple-instances-of-my-app"></a>Ölçeği genişletilen Azure App Service (Uygulamam birden çok örneğini) varsa ne olur?

Anlık görüntü noktaları her tek örnekli uygulandığından, uygulamanızın birden çok örneğe sahip olduğunda. Belirtilen koşulları ile İsabet yalnızca ilk anlık görüntü noktası anlık görüntüsünü oluşturur. Birden çok anlık görüntü noktaları varsa, daha sonra anlık görüntüleri oluşturulan ilk anlık görüntüyle aynı örnekten gelir. Uygulama günlükleri için gönderilen günlüğe kaydetme noktaları her örneğinden iletileri gönderirken çıkış penceresine gönderilen günlüğe kaydetme noktaları yalnızca bir örneği, gelen iletileri gösterir.

#### <a name="how-does-the-snapshot-debugger-load-symbols"></a>Nasıl Snapshot Debugger sembolleri?

Snapshot Debugger, Azure App Service için yerel veya dağıtılmış uygulama için eşleştirme sembolleri sahip olmasını gerektirir. (Katıştırılmış pdb şu anda desteklenmemektedir.) Snapshot Debugger, Azure uygulama hizmetiniz semboller otomatik olarak indirir. Visual Studio 2017 sürüm 15.2 ile başlayarak, Azure App Service'e dağıtma ayrıca uygulamanızın sembolleri dağıtır.

#### <a name="does-the-snapshot-debugger-work-against-release-builds-of-my-application"></a>Snapshot Debugger, sürüm derlemeleri uygulamamın karşı çalışır mı?

Evet - Snapshot Debugger, sürüm derlemeleri karşı çalışmaya yöneliktir. Bir anlık görüntü noktası bir işlevde yerleştirildiğinde, işlev hata ayıklanabilir yapmak geri bir hata ayıklama sürümünü için derlenmiştir. Anlık görüntü hata ayıklamayı durdurma işlevleri yayın derleme sürümüne döndürür.

#### <a name="can-logpoints-cause-side-effects-in-my-production-application"></a>Günlüğe kaydetme noktaları üretim uygulamamda yan etkilere neden olabilir?

Hayır - uygulamanıza eklediğiniz herhangi bir günlük iletisi hemen değerlendirilir. Bunlar, uygulamanızda yan etkileri neden olamaz. Ancak, bazı yerel özellikler günlüğe kaydetme noktası hata erişilebilir olmayabilir.

#### <a name="does-the-snapshot-debugger-work-if-my-server-is-under-load"></a>Snapshot Debugger sunucumu yük altında ise çalışır mı?

Evet, anlık görüntü hata ayıklama sunucuları yük altında çalışabilir. Snapshot Debugger kısıtlar ve anlık görüntüleri durumlarda yakalamaz boş bellek miktarı sunucunuzdaki yetersiz olduğunda.

#### <a name="how-do-i-uninstall-the-snapshot-debugger"></a>Snapshot Debugger'ı nasıl kaldırabilirim?

Uygulama hizmetinizde aşağıdaki adımlarla Snapshot Debugger site uzantısını kaldırabilirsiniz:

1. Visual Studio'daki bulut Gezgini'nde ya da Azure portal aracılığıyla uygulama hizmetiniz devre dışı bırakın.
1. Uygulama hizmetinizin Kudu sitesine gidin (diğer bir deyişle, yourappservice. **SCM**. azurewebsites.net) gidin **Site uzantıları**.
1. Snapshot Debugger site uzantısını kaldırmak için X tıklayın.

#### <a name="why-are-ports-opened-during-a-snapshot-debugger-session"></a>Bağlantı noktaları, Snapshot Debugger oturumu sırasında neden açıldı?

Anlık görüntü hata ayıklayıcısı Azure'da alınan anlık görüntülere hata ayıklamak için bir dizi bağlantı noktası açmak gereken, uzaktan hata ayıklama için gereken aynı bağlantı noktaları şunlardır. [Bağlantı noktalarının listesi, burada bulduğunuz](../debugger/remote-debugger-port-assignments.md).

#### <a name="how-do-i-disable-the-remote-debugger-extension"></a>Uzaktan hata ayıklayıcı uzantıyı nasıl devre dışı bırakabilirim?

Uygulama hizmetleri için:
1. Azure Portalı aracılığıyla uzaktan hata ayıklayıcı uzantısı uygulama hizmetiniz için devre dışı bırakın.
2. Azure portalı > uygulama hizmeti kaynak dikey pencerenizi > *uygulama ayarları*
3. Gidin *hata ayıklama* tıklayın ve bölüm *kapalı* için düğme *uzaktan hata ayıklama*.

AKS için:
1. Dockerfile, karşılık gelen bölümlere kaldırmak için güncelleştirme [Docker görüntüleri üzerinde Visual Studio Snapshot Debugger](https://github.com/Microsoft/vssnapshotdebugger-docker).
2. Yeniden oluşturun ve değiştirilmiş bir Docker görüntüsü dağıtın.

İçin sanal makine/sanal makine ölçek kümeleri uzaktan hata ayıklayıcı uzantısı, sertifikalar, KeyVaults ve gelen NAT havuzları şu şekilde kaldırabilirsiniz:

1. Uzaktan hata ayıklayıcı uzantısını kaldırma  

   Sanal makineler ve sanal makine ölçek kümeleri için uzaktan hata ayıklayıcıyı devre dışı bırakmak için birkaç yolu vardır:  

      - Cloud Explorer aracılığıyla uzaktan hata ayıklayıcıyı devre dışı bırak  

         - Cloud Explorer > sanal makine kaynağınıza > hata ayıklama devre dışı bırak (hata ayıklama devre dışı bırakma yok sanal makine ölçek kümesi üzerinde Cloud Explorer için).  


      - PowerShell betikleri/cmdlet'leri'ile uzaktan hata ayıklayıcıyı devre dışı bırak  

         Sanal makine için:  

         ```
         Remove-AzVMExtension -ResourceGroupName $rgName -VMName $vmName -Name Microsoft.VisualStudio.Azure.RemoteDebug.VSRemoteDebugger  
         ```

         Sanal makine ölçek kümeleri için:  
         ```
         $vmss = Get-AzVmss -ResourceGroupName $rgName -VMScaleSetName $vmssName  
         $extension = $vmss.VirtualMachineProfile.ExtensionProfile.Extensions | Where {$_.Name.StartsWith('VsDebuggerService')} | Select -ExpandProperty Name  
         Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $extension  
         ```

      - Azure portalı üzerinden uzaktan hata ayıklayıcıyı devre dışı bırak
         - Azure portalı > kaynak dikey penceresinde, sanal makine/sanal makine ölçek ayarlar > uzantıları  
         - Microsoft.VisualStudio.Azure.RemoteDebug.VSRemoteDebugger uzantıyı kaldırın  


         > [!NOTE]
         > Sanal makine ölçek kümeleri - portal DebuggerListener bağlantı noktalarını kaldırma izin vermez. Azure PowerShell kullanmanız gerekir. Ayrıntılar için aşağıya bakın.
  
2. Sertifikalar ve Azure anahtar Kasası'nı Kaldır

   Sanal makine veya sanal makine ölçek kümeleri için uzaktan hata ayıklayıcı uzantısını yüklerken, hem istemci hem de sunucu sertifikalarını VS istemci kimlik doğrulaması ile Azure sanal makine için oluşturulan/kaynaklar sanal makine ölçek kümeleri.  

   - İstemci sertifikası  

      Bu sertifika bulunan sertifika otomatik olarak imzalanan bir sertifika olduğundan: / CurrentUser/My /  

      ```
      Thumbprint                                Subject  
      ----------                                -------  

      1234123412341234123412341234123412341234  CN=ResourceName  
      ```

      Bu sertifikayı makinenizden kaldırmak için bir PowerShell yoludur

      ```
      $ResourceName = 'ResourceName' # from above  
      Get-ChildItem -Path Cert:\CurrentUser\My | Where-Object {$_.Subject -match $ResourceName} | Remove-Item  
      ```

   - Sunucu sertifikası
      - Karşılık gelen sunucu sertifikası parmak izi Azure anahtar kasası için gizli dizi olarak dağıtılır. VS bulun veya ön eki MSVSAZ * bölgesindeki sanal makineye karşılık gelen bir anahtar kasası oluşturma dener veya kaynak sanal makine ölçek kümeleri. Tüm sanal makine veya sanal makine ölçek kümeleri bu bölgeye dağıtılan kaynakları bu nedenle aynı KeyVault paylaşmak.  
      - Sunucu sertifikası parmak izi gizli anahtarı silmek için Azure portalına gidin ve MSVSAZ * anahtar kasası kaynağınızın barındıran aynı bölgede bulun. Etiketli gizli anahtarı silme `remotedebugcert<<ResourceName>>`  
      - PowerShell aracılığıyla, kaynak sunucu gizli anahtarı silmek gerekir.  

      Sanal makineler için:  

      ```
      $vm.OSProfile.Secrets[0].VaultCertificates.Clear()  
      Update-AzVM -ResourceGroupName $rgName -VM $vm  
      ```
                        
      Sanal makine ölçek kümeleri için:  

      ```
      $vmss.VirtualMachineProfile.OsProfile.Secrets[0].VaultCertificates.Clear()  
      Update-AzVmss -ResourceGroupName $rgName -VMScaleSetName $vmssName -VirtualMachineScaleSet $vmss  
      ```
                        
3. Tüm DebuggerListener gelen NAT havuzları (sanal makine ölçek kümesi yalnızca) Kaldır  

   Uzaktan hata ayıklayıcı, Ölçek kümesi ait yük dengeleyici için uygulanan DebuggerListener gelen NAT havuzları tanıtır.  

   ```
   $inboundNatPools = $vmss.VirtualMachineProfile.NetworkProfile.NetworkInterfaceConfigurations.IpConfigurations.LoadBalancerInboundNatPools  
   $inboundNatPools.RemoveAll({ param($pool) $pool.Id.Contains('inboundNatPools/DebuggerListenerNatPool-') }) | Out-Null  
                
   if ($LoadBalancerName)  
   {
      $lb = Get-AzLoadBalancer -ResourceGroupName $ResourceGroup -name $LoadBalancerName  
      $lb.FrontendIpConfigurations[0].InboundNatPools.RemoveAll({ param($pool) $pool.Id.Contains('inboundNatPools/DebuggerListenerNatPool-') }) | Out-Null  
      Set-AzLoadBalancer -LoadBalancer $lb  
   }
   ```

#### <a name="how-do-i-disable-snapshot-debugger"></a>Snapshot Debugger nasıl devre dışı bırakabilirim?

App Service için:
1. Snapshot Debugger, Azure portalı üzerinden uygulama hizmetiniz için devre dışı bırakın.
2. Azure portalı > uygulama hizmeti kaynak dikey pencerenizi > *uygulama ayarları*
3. Azure portalında aşağıdaki uygulama ayarlarını silin ve değişikliklerinizi kaydedin. 
    - INSTRUMENTATIONENGINE_EXTENSION_VERSION
    - SNAPSHOTDEBUGGER_EXTENSION_VERSION

    > [!WARNING]
    > Herhangi bir değişiklik uygulama ayarları, uygulamanın yeniden başlatır. Uygulama ayarları hakkında daha fazla bilgi bulunabilir [burada](https://docs.microsoft.com/azure/app-service/web-sites-configure#app-settings). 

AKS için:
1. Dockerfile, karşılık gelen bölümlere kaldırmak için güncelleştirme [Docker görüntüleri üzerinde Visual Studio Snapshot Debugger](https://github.com/Microsoft/vssnapshotdebugger-docker).
2. Yeniden oluşturun ve değiştirilmiş bir Docker görüntüsü dağıtın.

Sanal makine/sanal makine ölçek kümeleri için:

Snapshot Debugger'ı devre dışı bırakmak için birkaç yolu vardır:
- Cloud Explorer > kaynak sanal makine/sanal makine ölçek kümesi > tanılama devre dışı bırak

- Azure portalı > kaynak dikey penceresinin, sanal makine/sanal makine ölçek kümesi > uzantılar > Microsoft.Insights.VMDiagnosticsSettings kaldırma uzantısı

- PowerShell cmdlet'lerinden [Az PowerShell](https://docs.microsoft.com/powershell/azure/overview)

    Sanal makine:
    ```
        Remove-AzVMExtension -ResourceGroupName $rgName -VMName $vmName -Name Microsoft.Insights.VMDiagnosticsSettings 
    ```
    
    Sanal makine ölçek kümeleri:
    ```
        $vmss = Get-AzVmss -ResourceGroupName $rgName -VMScaleSetName $vmssName
        Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name Microsoft.Insights.VMDiagnosticsSettings
    ```

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio’da hata ayıklama](../debugger/index.md)
- [Snapshot Debugger'ı kullanarak canlı ASP.NET uygulamalarının hatalarını ayıklama](../debugger/debug-live-azure-applications.md)
- [Snapshot Debugger'ı kullanarak canlı ASP.NET Azure sanal Machines\Virtual makineler ölçek kümeleri hata ayıklama](../debugger/debug-live-azure-virtual-machines.md)
- [Snapshot Debugger'ı kullanarak canlı ASP.NET Azure Kubernetes hata ayıklama](../debugger/debug-live-azure-kubernetes.md)
- [Anlık görüntü hata ayıklama için sorun giderme ve bilinen sorunlar](../debugger/debug-live-azure-apps-troubleshooting.md)