---
title: 'DA0007: Denetim akışı için özel durumlar kullanmaktan kaçının | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DAExceptionsThrown
- vs.performance.7
- vs.performance.rules.DA0007
- vs.performance.DA0007
ms.assetid: ee8ba8b5-2313-46c9-b129-3f3a2a232898
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 7ae7b890e12d56e61571ecbf72dc1b0cd39567a4
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53898209"
---
# <a name="da0007-avoid-using-exceptions-for-control-flow"></a>DA0007: Denetim akışı için özel durumlar kullanmaktan kaçının

|||  
|-|-|  
|Kural Kimliği|DA0007|  
|Kategori|.NET framework kullanımı|  
|Profil oluşturma yöntemleri|Tümü|  
|İleti|Çok sayıda özel durumları tutarlı bir şekilde oluşturuldu. Program mantığında özel durumların kullanımını azaltmayı deneyin.|  
|İleti türü|Uyarı|  

 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 25 örnekleri toplamanız gerekir.  

## <a name="cause"></a>Sebep  
 Yüksek oranda .NET Framework özel durum işleyicileri profil oluşturma verileri adı veriliyordu. Oluşan özel durumların sayısını azaltmak için başka bir denetim akışı mantığı kullanmayı düşünün.  

## <a name="rule-description"></a>Kural açıklaması  
 Hataları ve program yürütme kesintiye diğer olayları yakalamak için özel durum işleyicileri kullanımını iyi olsa da, normal program yürütme mantığının parçası olarak özel durum işleyicisi kullanımını pahalı olabilir ve kaçınılmalıdır. Çoğu durumda, özel durum nadiren oluşur ve değil beklendiği durumlarda kullanılmalıdır. Özel durumlar programın normal akışının bir parçası değer döndürmek için kullanılmamalıdır. Çoğu durumda, değerler doğrulanıyor ve soruna neden deyimleri yürütülmesini durdurmak için koşullu mantığı kullanarak özel durumlarını oluşturma önleyebilirsiniz.  

 Daha fazla bilgi için bkz [özel durum yönetimi](http://go.microsoft.com/fwlink/?LinkID=177825) bölümünü **bölüm 5: yönetilen kod performansını iyileştirme** içinde **geliştirme .NET uygulama performansı ve ölçeklenebilirlik** hacmi **Microsoft Patterns and Practices** MSDN Kitaplığı.  

## <a name="how-to-investigate-a-warning"></a>Bir uyarı araştırma  
 İleti Hata Listesi penceresindeki işaretleri görünümüne gitmek için çift tıklayın. İçeren bir sütun Bul **.NET CLR özel durumları (@ProcessInstance)\\Excels durum sayısı / sn** ölçümleri. Varsa belirli aşamaları program yürütmenin özel durum işleme diğerlerinden daha sık olduğu belirleyin. Throw deyimleri tanımlamak ve try/catch blokları sık karşılaşılan özel durumların üreten bir örnekleme profili kullanarak deneyin. Gerekirse, catch blokları hangi özel durumları en sık işlenen anlamanıza yardımcı olması için mantık ekleyin. Mümkünse, sık yürütülen Değiştir throw deyimleri ya da basit bir akış ile catch blokları mantığı veya doğrulama kodunu denetleyin.  

 Örneğin, Bul çıkacaksa uygulamanızı sıfır değerleri olan kesirler denetlemek için program mantığını uygulama performansını artırır ekleme sık DivideByZeroException özel durumları, işleme oluştu.