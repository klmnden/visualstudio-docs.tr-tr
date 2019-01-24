---
title: 'DA0026: Aşırı Çekirdek CPU süresi işleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.performance.rules.DA0026
- vs.performance.DA0026
- vs.performance.26
ms.assetid: 4cfc8a29-b29b-4a72-b386-03d8856fdf8a
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: fef0a3c42be1057bd1217ec676ae43b220d80345
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54768977"
---
# <a name="da0026-excessive-kernel-cpu-time-processing"></a>DA0026: Aşırı Çekirdek CPU süresi işleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kural Kimliği | TODO |  
| Kategori | Profil oluşturma araçları kullanım |  
| Profil oluşturma yöntemi | Örnekleme |  
| İleti | Çekirdek modu CPU zamanı görece yüksek miktarda ölçülmüştür. Kaynağı etkin syscall örneklemesiyle incelemeyi dikkate alın. |  
| Kural türü | Bilgi |  
  
 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.  
  
## <a name="cause"></a>Sebep  
 Çekirdek modunda yürütülen oranda CPU süresi, kullanıcı modunda harcanan süreyi aştı. Yeniden profil oluşturmayı hem de örnekleme yüksek çekirdek modu yürütme sürelerini nedenini belirlemek için sistem çağrıları (syscalls) sayısını göz önünde bulundurun.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Uygulama çekirdek modu yürütme için harcanan süre görece yüksek oranda daha fazla araştırma isteyebilirsiniz. Bir kullanıcı modu uygulaması için iş parçacığı veya işlem eşitleme temellerine bekleyin ya da sistem çağrıları yapmak için g/ç işlemleri gerçekleştirmek için çekirdek moduna geçer. Sistem çağrıları uygulama yapar ve sistem çağrıları örnek çağrı yığınlarını Topla seçeneğini belirlediğinizde, bunlardan sorumlu olan işlevleri temel tür araştırabilirsiniz.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Profili yeniden çalıştırın ve sistem çağrıları tabanlı örnekleri toplamak için seçeneğini uygulamanızı sağlayan sistem çağrıları tür araştırmak için. Bkz: [nasıl yapılır: Örnekleme olayları seçme](../profiling/how-to-choose-sampling-events.md) daha fazla bilgi için IDE içinde profil oluşturma araçları çalıştırıyorsanız. Komut satırından profil oluşturma araçları çalıştırıyorsanız bkz **örnekleme aralığı seçenekleri** bölümünü [VSPerfCmd](../profiling/vsperfcmd.md) konuda Profil Araçları komut satırı araçları başvurusu.
