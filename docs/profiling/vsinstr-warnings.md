---
title: Vsınstr uyarıları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- instrumentation, VSInstr tool
- warnings
- VSInstr tool
- warnings, VSInstr tool
- performance tools, VSInstr tool
ms.assetid: 47512bc9-a8e9-4628-883a-d9888edab786
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 3d0b201d22b93b7c023627887f0fc033da360fe9
ms.sourcegitcommit: d0b02affd24e66efed924c197824f35f823e3240
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/21/2019
ms.locfileid: "54417869"
---
# <a name="vsinstr-warnings"></a>Vsınstr uyarıları
Aşağıdaki tabloda tarafından verilen uyarılar *VSInstr.exe* aracı. Uyarıyı görüntülenmesini engellemek için uyarı numaralarını NOWARN seçeneğiyle kullanabilirsiniz.  
  
|Uyarı numarası|Açıklama|  
|--------------------|-----------------|  
|**VSP1026**|Kapsamı MSCorLib başvurma kitaplıklar üzerinde desteklenmiyor. Bu genellikle taşınabilir kitaplıklar için geçerlidir.|  
|**VSP2000**|İç Hata. Bu yürütülebilir dosya için modülün dosya adı alınamıyor.|  
|**VSP2001**|\<derleme adı > kesin adlandırılmış bir derlemedir. Yürütülmek üzere önce onu yeniden imzalanması gerekir.<br /><br /> İmzalı bir derleme işaretlenmiş durumda olduğunda bu uyarı oluşur. Kullanabileceğiniz *sn.exe* aracı ikili çekilmeye veya geçici olarak devre dışı tanımlayıcı ad gereksinim kapatmak için. Daha fazla bilgi için [Sn.exe (tanımlayıcı ad aracı)](/dotnet/framework/tools/sn-exe-strong-name-tool).|  
|**VSP2002**|İşlevi bulunamadı \<funcname > dosyasındaki \<dosya adı ><br /><br /> Bir işlev içinde belirtilen dosya bulunamıyorsa, bu uyarı oluşur.|  
|**VSP2003**|Çapraz atlama işlevi bulunamadı \<funcname > dosyasındaki \<dosya adı >.<br /><br /> Vsınstr silinmez olamaz, bu uyarı, çapraz atlar meydana gelir. Çapraz atlama kodu iyileştirme için kullanılır.|  
|**VSP2004**|İşlev \<funcname > EXCLUDE komut satırı anahtarı kullanılarak dışlandı ancak çapraz atlama içerdiği için gerekli.<br /><br /> İşlevi, hariç TUTMA seçeneğini kullanarak dışlandı ancak izleme işlemi sırasında gerekli bu uyarı oluşur. Profil Oluşturucu otomatik olarak gerekli işlevi içerir.|  
|**VSP2005**|İç izleme hatası \<hata metni ><br /><br /> İzleme gerçekleştirdiyseniz, bu uyarı görüntülenir. Bunu düzeltilebilir olup olmadığını belirlemek için hata metni gözden geçirin.|  
|**VSP2006**|İçin PDB bulunamadı \<adı ><br /><br /> PDB dosyası arama yolunda yok veya ikili ile eşlemiyor değilse bu uyarı oluşur.|  
|**VSP2007**|\<Dosya adı > hiçbir izlenebilir kod içermiyor.<br /><br /> Bu uyarı, İşlevler ikili dosyadaki tüm dışlanan veya belirtilen dosya yalnızca kaynaklar içeriyorsa görüntülenir.|  
|**VSP2008**|Güvenlik öznitelikleri alınamıyor \<adı >. Hata kodu \<kod ><br /><br /> Kullanıcı READ_DAC iznine sahip değilse bu uyarı oluşur. İzleme işlemi sırasında profil oluşturucu için ikili dosya özgün DACL korumak çalışır. Özgün ikiliyi yeni bir ikili dosya ile değiştirilir olduğundan, özgün ikilinin DACL kopyalanır ve yeni ikili için uygulanır. Kullanıcı özgün iki READ_DAC erişim olmaması durumunda başarısız olabilir.|  
|**VSP2009**|Güvenlik öznitelikleri ayarlanamadı \<adı >. Hata kodu \<hata numarası ><br /><br /> Kullanıcı WRITE_DAC iznine sahip değilse bu uyarı oluşur. İzleme işlemi sırasında profil oluşturucu için ikili dosya özgün DACL korumak çalışır. Özgün ikiliyi yeni bir ikili dosya ile değiştirilir olduğundan, özgün ikilinin DACL kopyalanır ve yeni ikili için uygulanır. Kullanıcı yeni ikili dosya WRITE_DAC erişim olmaması durumunda başarısız olabilir.|  
|**VSP2010**|Hiçbir işlevlerdir özellikle /-EXCLUDE seçenekleri nedeniyle, - izleme için seçili içerir|  
|**VSP2011**|İçerme/dışlama funcspec \<adı > tüm işlevleri eşleşmiyor|  
|**VSP2012**|Görüntü için kod kapsamı izleme eklenmiş herhangi bir kod içermiyor.<br /><br /> Profiler, aşağıdaki kodun türünü izleme değil:<br /><br /> -Statik CRT işlevleri<br />-Yönetilen yöntemleri ile NonUserCodeAttribute öznitelikli<br />-DebuggerHiddenAttribute ile öznitelikli yönetilen yöntemleri<br />-MASM blokları<br /><br /> Bu filtreleme sonrasında, varsa, kod sol bu uyarı oluşturulur.|  
|**VSP2013**|Bu görüntüyü izlemek 32-bit işlem olarak çalıştırmayı gerektirir. CLR üst bilgi bayrakları bunu yansıtmak için güncelleştirildi.<br /><br /> Profil Oluşturucu, 64-bit işletim sistemlerinde WOW64 öykünücüsünde 32-bit işlem açabilmek ikili değiştirir. Var olan bir 64 bit işlemde yüklü olmaları durumunda kitaplıkları (DLL'ler) için bu başarısız olabilir. Bu uyarı, bağımlılık kullanıcıya bildirir.|  
|**VSP2014**|Elde edilen izleme eklenmiş görüntü geçersiz görünüyor ve çalışmayabilir.<br /><br /> Geçersiz PE üst bilgisi son kullanılan derleme sahip olduğunda bu ileti oluşur.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSInstr](../profiling/vsinstr.md)