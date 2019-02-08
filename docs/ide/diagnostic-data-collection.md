---
title: Tanılama verilerini ve sistem tarafından oluşturulan günlükler
ms.date: 05/24/2018
ms.topic: conceptual
author: gewarren
ms.author: michma
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0f92e899ff8e56c68fcf1a4ab639d027c139afcf
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55925504"
---
# <a name="system-generated-logs-collected-by-visual-studio"></a>Visual Studio tarafından toplanan sistem tarafından oluşturulan günlükler

Visual Studio aracılığıyla ürünün kalitesini ve sorunları gidermek için sistem tarafından oluşturulan günlükleri toplar [Visual Studio Müşteri Deneyimi Geliştirme Programı](visual-studio-experience-improvement-program.md). Bu makalede topladığımız verilerinin ve nasıl kullandığımızı türleri hakkında bazı bilgiler sağlar. Ayrıca, kişisel veya gizli bilgilerin yanlışlıkla açığa çıkmasına uzantı yazarları nasıl kaçınabilirsiniz ipuçları sağlar.

## <a name="types-of-collected-data"></a>Toplanan veri türleri

Visual Studio, kilitlenmeleri, askıda, kullanıcı Arabirimi yanıt vermeyi durdurma sorununa ve yüksek CPU veya bellek kullanımı için sistem tarafından oluşturulan günlükleri toplar. Ürün yüklemesi ya da kullanım sırasında karşılaşılan hatalar hakkında bilgileri de toplarız. Toplanan verileri hatada göre değişir ve Yığın izlemeleri ve bellek dökümlerini özel durum bilgilerini içerebilir:

- Yüksek CPU kullanımı ve yanıt vermeyi durdurma sorununa ilgili Visual Studio iş parçacığı Yığın izlemeleri toplanır.

- Kilitlenmeler, askıda veya yüksek bellek kullanımı, sorunun nerede bazı iş parçacığı yığın izlemelerini olmayan kök belirlemek için yeterli çalışmaları neden bir bellek topladığımız *döküm*. Hata oluştuğunda döküm işlemin durumunu temsil eder.

- Beklenmeyen hata koşulları, diskte, bir dosyaya yazmaya çalışırken hata oluştu, özel durum için özel durum hakkında bilgi topluyoruz. Özel durum yığın izleme özel durumun oluştuğu iş parçacığının, özel durum ve belirli özel durumu ile ilgili diğer bilgileri ile ilişkili ileti adı bilgileri içerir.

   Aşağıdaki örnek, toplanan verilerin bir özel durum adı, yığın izlemesi ve özel durum iletisi gösterilir:

   ```text
   "Reserved.DataModel.Fault.Exception.TypeString": "System.IO.IOException",
   "Reserved.DataModel.Fault.Exception.StackTrace": "System.IO.__Error.WinIOError(Int32,String)\r\n
   System.IO.FileStream.Init(String,FileMode,FileAccess,Int32,Boolean,FileShare,Int32,FileOptions,SECURITY_ATTRIBUTES,String,Boolean,Boolean,Boolean)\r\n
   System.IO.FileStream..ctor(String,FileMode,FileAccess,FileShare,Int32,FileOptions,String,Boolean,Boolean,Boolean)\r\nSystem.IO.StreamWriter.CreateFile(String,Boolean,Boolean)\r\n
   System.IO.StreamWriter..ctor(String,Boolean,Encoding,Int32,Boolean)\r\n
   System.IO.StreamWriter..ctor(String,Boolean)\r\n
   System.IO.File.CreateText(String)\r\n
   Microsoft.VisualStudio.Setup.Services.FileSystem.CreateText(String,Boolean)\r\n
   Microsoft.VisualStudio.Setup.Cache.ChannelManifestRepository.WriteChannelManifest(IChannelManifest,String,String)\r\n
   Microsoft.VisualStudio.Setup.Cache.ChannelManifestRepository.AddChannel(ChannelManifestPair,Boolean)\r\n
   Microsoft.VisualStudio.Setup.Cache.CacheManager.AddChannel(ChannelManifestPair,Boolean)\r\n
   Microsoft.VisualStudio.Setup.ChannelManager.\<UpdateAsync>d__37.MoveNext()\r\n”,
   "Reserved.DataModel.Fault.Exception.Message": " The process cannot access the file 'C:\\Users\\[UserName]\\AppData\\Local\\Microsoft\\VisualStudio\\Packages\\_Channels\\4CB340F5\\channelManifest.json' because it is being used by another process."
   ```

## <a name="how-we-use-system-generated-logs"></a>Sistem tarafından oluşturulan günlüklere nasıl kullandığımızı

Bir hata nedenini belirlemek için iş akışı türünü hata ve önemine bağlı olarak değişir.

### <a name="error-classification"></a>Hata sınıflandırma

Hataları günlüklerine göre sınıflandırılmış ve bunların araştırma önceliğini belirlemek için hesaba katılır. Örneğin, biz keşfedebilir, "System.IO. \__Error.WinIOError ""System.IO.FileStream.Init "sürümünde 500 kereden oluştu \<x > ürünün ve bu sürümde en yüksek oran, oluşumunu sahiptir.

### <a name="work-items-for-tracking"></a>İş öğelerini izlemek için

Tek tek, öncelikli hatalar için çalışma öğeleri oluşturulur ve mühendislerine araştırma için atanmış. Bu iş öğeleri genellikle Sınıflandırma, öncelik ve hata türüne ilgili tanılama bilgileri içerir. Bu bilgiler hata için toplanan sistem tarafından oluşturulan günlüklere türetilir. Örneğin, bir iş öğesi için bir kilitlenme kilitlenme nerede oluştuğunu yığın izlemesi içerebilir.

### <a name="error-investigation"></a>Hata araştırma

Mühendisler, bir hata nedenini belirlemek için bir iş öğesinde kullanılabilir bilgileri kullanın. Bazı durumlarda, istedikleri nedir iş öğesinde değerinden daha fazla bilgi bu durumda bunlar toplanan özgün sistem tarafından oluşturulan günlüğüne başvurun. Örneğin, bir mühendis, bir ürün kilitlenme anlamak için bellek dökümü inceleyin.

## <a name="tips-for-extension-authors"></a>Uzantı yazarları için ipuçları

Uzantı yazarları kullanarak kişisel değil kişisel bilgiler veya kendi modüller, türler ve yöntemlerin adlarını diğer hassas bilgiler açığa sınırlamanız gerekir. Bu bilgileri, yığında kodu ile bir kilitlenme veya benzer bir hata koşulu ortaya çıkarsa, sistem tarafından oluşturulan günlükleri bir parçası olarak toplanan.

## <a name="opt-out-of-data-collection"></a>Veri toplama işlemini iptal

Amacını topladığımız veriler ve saklama ve erişim kısıtlamaları göz önünde bulundurulduğunda, Visual Studio ve Windows için varsayılan gizlilik ayarlarını kullanmanızı öneririz. Ancak, [çıkma](../ide/visual-studio-experience-improvement-program.md#opt-in-or-out) Visual Studio deneyimini geliştirme programı. Tüm programları için sistem tarafından oluşturulan günlük toplama dışında iptal etmek için bkz. [Tanılama, geri bildirim ve Windows 10'daki gizlilik](https://privacy.microsoft.com/windows-10-feedback-diagnostics-and-privacy). Seçenekler, kullandığınız Windows sürümüne bağlı olarak değişiklik gösterebilir.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio Müşteri Deneyimi Geliştirme Programı](visual-studio-experience-improvement-program.md)
- [Tanılama, geri bildirim ve Windows 10'daki gizlilik](https://privacy.microsoft.com/windows-10-feedback-diagnostics-and-privacy)