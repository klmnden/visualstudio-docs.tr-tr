---
title: .NET framework kullanımı performans kuralları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: ab573755-6370-48aa-853d-a7321c424c79
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a9c976560b39fd8a9146733d78cd3a094ed3b118
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54755118"
---
# <a name="net-framework-usage-performance-rules"></a>.NET Framework Kullanımı Performans Kuralları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kategorideki.NET Framework kullanımı performans kuralları iyileştirilebilir ve aynı zamanda çöp toplama ve performans sorunlarını araştırılan kilit çakışması gibi daha genel kullanım düzenlerini tanımlamak belirli yöntemleri belirleyin.  
  
|||  
|-|-|  
|[DA0001: Birleştirmeler için StringBuilder kullanma](../profiling/da0001-use-stringbuilder-for-concatenations.md)|Çağrılar <xref:System.String.Concat%28System.String%2CSystem.String%29?displayProperty=fullName> profil oluşturma verilerinin önemli bir kısmı olan. Kullanmayı <xref:System.Text.StringBuilder> birden çok kesimi dizeleri oluşturmak için sınıf.|  
|[DA0005: Sık kullanılan GC2 koleksiyonları](../profiling/da0005-frequent-gc2-collections.md)|Görece yüksek sayıda .NET bellek nesneleri nesil 2 çöp toplamada kazanılır. Çok kısa süreli nesneleri nesil 1 toplamadan, bellek yönetimi maliyetini kolayca aşırı hale gelebilir.|  
|[DA0006: Değer türleri için Equals() üzerine yazın](../profiling/da0006-override-equals-parens-for-value-types.md)|Çağrılar `Equals` yöntemi veya bir genel değer türü eşitlik işleçleri olan profil oluşturma verilerinin önemli bir kısmı. Daha verimli bir yöntem uygulamayı düşünün.|  
|[DA0007: Denetim akışı için özel durumlar kullanmaktan kaçının](../profiling/da0007-avoid-using-exceptions-for-control-flow.md)|Yüksek oranda .NET Framework özel durum işleyicileri profil oluşturma verileri adı veriliyordu. Oluşan özel durumların sayısını azaltmak için başka bir denetim akışı mantığı kullanmayı düşünün.|  
|[DA0010: Pahalı GetHashCode](../profiling/da0010-expensive-gethashcode.md)|Çağrılar `GetHashCode` türü yöntemi olan profil oluşturma verilerinin önemli bir kısmı veya `GetHashCode` yöntemi bellek ayırır. Yöntem karmaşıklığını azaltın.|  
|[DA0011: Pahalı CompareTo](../profiling/da0011-expensive-compareto.md)|`CompareTo` Pahalı türü yöntemi veya yöntem bellek ayırır. Karmaşıklığını azaltın `CompareTo` yöntemi.|  
|[DA0012: Önemli miktarda Yansıma](../profiling/da0012-significant-amount-of-reflection.md)|Çağrılar <xref:System.Reflection?displayProperty=fullName> gibi yöntemler <xref:System.Reflection.IReflect.InvokeMember%2A> ve <xref:System.Reflection.IReflect.GetMember%2A> veya türü yöntemleri gibi <xref:System.Type.InvokeMember%2A> profil oluşturma verilerinin önemli bir kısmı olan. Mümkün olduğunda, erken bağlama yöntemlerine bağımlı derlemelerin bu yöntemler yerine göz önünde bulundurun.|  
|[DA0013: Yüksek oranda String.Split veya String.Substring kullanımı](../profiling/da0013-high-usage-of-string-split-or-string-substring.md)|Çağrılar <xref:System.String.Split%2A?displayProperty=fullName> veya <xref:System.String.Substring%2A> profil oluşturma verilerinin büyük bir kısmı yöntemlerdir. Kullanmayı <xref:System.String.IndexOf%2A> veya <xref:System.String.IndexOfAny%2A> bir dizedeki bir alt dizenin bulunup bulunmadığını sınıyorsanız.|  
|[DA0018: Yönetilen bellek limitlerinde çalışan 32 bit Uygulama](../profiling/da0018-32-bit-application-running-at-process-managed-memory-limits.md)|Profil oluşturma çalışması sırasında toplanan sistem verilerini, .NET Framework bellek 32-bit işlem içinde yönetilen yığınlar ulaşan en büyük boyutu yığınlardaki yaklaşıldığında gösterir. Uygulama tarafından yönetilen kaynaklarının kullanımını en iyi duruma getirme ve .NET bellek profil oluşturma yöntemini kullanarak yeniden profil oluşturmayı göz önünde bulundurun.|  
|[DA0021: Yüksek oranda 1. nesil atık toplama](../profiling/da0021-high-rate-of-gen-1-garbage-collections.md)|.NET bellek nesneleri görece yüksek sayıda kuşak 1 çöp toplamada kazanılır. Çok kısa süreli nesneleri nesil 0 toplamadan, bellek yönetimi maliyetini kolayca aşırı hale gelebilir.|  
|[DA0022: Yüksek oranda 2. nesil atık toplama](../profiling/da0022-high-rate-of-gen-2-garbage-collections.md)|Çok sayıda .NET bellek nesneleri nesil 2 çöp toplamada kazanılır. Çok kısa süreli nesneleri nesil 1 toplamadan, bellek yönetimi maliyetini kolayca aşırı hale gelebilir. Bu kural, oranda kilit çakışması kural DA0005 üst eşik değerini aştığında tetikler.|  
|[DA0023: Yüksek GC CPU süresi](../profiling/da0023-high-gc-cpu-time.md)|Profil oluşturma sırasında toplanan sistem performansı verilerini toplam uygulama işleme süresi ile karşılaştırıldığında, çöp toplamaya harcanan süreyi önemli olduğunu gösterir.|  
|[DA0024: Aşırı GC CPU Süresi](../profiling/da0024-excessive-gc-cpu-time.md)|Profil oluşturma sırasında toplanan sistem performansı verilerini toplam uygulama işleme süresi ile karşılaştırıldığında, çöp toplamaya harcanan süreyi aşırı yüksek olduğunu gösterir. Bu kural, çöp toplamaya harcanan süreyi kural DA0023 üst eşik değerini aştığında tetikler.|  
|[DA0038: Yüksek Oranda Kilit çakışması](../profiling/da0038-high-rate-of-lock-contentions.md)|Toplanan sistem performansı verilerini profil oluşturma verileriyle birlikte önemli ölçüde yüksek oranda kilit çakışması uygulama yürütme sırasında oluştuğunu gösterir. Çekişme nedenini bulmak için eşzamanlılık profili oluşturma yöntemi kullanarak yeniden profil oluşturmayı göz önünde bulundurun.|  
|[DA0039: Çok Yüksek Oranda Kilit çakışması](../profiling/da0039-very-high-rate-of-lock-contentions.md)|Toplanan sistem performansı verilerini profil oluşturma verileriyle birlikte bir aşırı yüksek oranda kilit çakışması uygulama yürütme sırasında oluştuğunu gösterir. Çekişme nedenini bulmak için eşzamanlılık profili oluşturma yöntemi kullanarak yeniden profil oluşturmayı göz önünde bulundurun. Bu kural, oranda kilit çakışması kural DA0038 üst eşik değerini aştığında tetikler.|
