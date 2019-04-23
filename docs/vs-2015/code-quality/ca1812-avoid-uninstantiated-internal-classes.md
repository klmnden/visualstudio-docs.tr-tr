---
title: 'CA1812: Örneklenmemiş iç sınıflardan kaçının | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1812
- AvoidUninstantiatedInternalClasses
helpviewer_keywords:
- AvoidUninstantiatedInternalClasses
- CA1812
ms.assetid: 1bb92a42-322a-44cc-98a8-8858212c1e1f
caps.latest.revision: 28
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: f44dcb010dd9c62d130913efd590a4c1b651de50
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60082009"
---
# <a name="ca1812-avoid-uninstantiated-internal-classes"></a>CA1812: Örneklenmemiş iç sınıflardan kaçının
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|AvoidUninstantiatedInternalClasses|
|CheckId|CA1812|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir derleme düzeyi türünün örneği, derleme içindeki kod tarafından oluşturulmaz.

## <a name="rule-description"></a>Kural Tanımı
 Bu kural, bir türü oluşturucular bir çağrı bulmaya çalışır ve hiçbir çağrı bulunursa bir ihlali bildirir.

 Aşağıdaki türleri bu kural tarafından incelenir değil:

- Değer türleri

- Soyut türler

- Numaralandırmalar

- Temsilciler

- Derleyici yayılan dizi türleri

- Olamaz başlatılamaz ve tanımlayan türler `static` (`Shared` Visual Basic'te) yalnızca yöntemleri.

  Uygularsanız, <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute?displayProperty=fullName> analiz ediliyor. derlemeye olarak işaretlenmiş tüm oluşturucular üzerinde bu kural gerçekleşmez `internal` alana bir başkası tarafından kullanılıp kullanılmadığını bildiremez çünkü `friend` derleme.

  İçinde bu sınırlamaya geçici bir çözüm çalışamaz olsa bile [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] kod analizi, dış tek başına FxCop oluşacak iç oluşturucularda her varsa `friend` analiz derleme varsa.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için türünü kaldırın veya onu kullanan kodu ekleyin. Tür yalnızca statik yöntemler içeriyorsa, derleyici varsayılan bir ortak örnek oluşturucusu yayma gelen önlemek için türü için aşağıdakilerden birini ekleyin:

- İçin özel bir oluşturucu türleri hedefleyen [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] 1.0 ve 1.1 sürümleri.

- `static` (`Shared` Visual Basic) değiştirici için türleri hedefleyen [!INCLUDE[dnprdnlong](../includes/dnprdnlong-md.md)].

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan bir uyarıyı bastırmak güvenlidir. Aşağıdaki durumlarda bu uyarının gösterilmemesi gerektiğini öneririz:

- Sınıfı gibi geç bağlanan yansıma yöntemleri ile oluşturulan <xref:System.Activator.CreateInstance%2A?displayProperty=fullName>.

- Sınıfı çalışma zamanı tarafından otomatik olarak oluşturulan veya [!INCLUDE[vstecasp](../includes/vstecasp-md.md)]. Örneğin, uygulayan sınıflar <xref:System.Configuration.IConfigurationSectionHandler?displayProperty=fullName> veya <xref:System.Web.IHttpHandler?displayProperty=fullName>.

- Sınıfının yeni bir kısıtlamaya sahip bir genel tür parametresi geçirilir. Örneğin, aşağıdaki örnekte, bu kural oluşturacak.

  ```csharp
  internal class MyClass
  {
      public DoSomething()
      {
      }
  }
  public class MyGeneric<T> where T : new()
  {
      public T Create()
      {
          return new T();
      }
  }
  // [...]
  MyGeneric<MyClass> mc = new MyGeneric<MyClass>();
  mc.Create();
  ```

  Bu durumda, bu uyarının gösterilmemesi önerilir.

## <a name="related-rules"></a>İlgili kuralları
 [CA1811: Çağrılmayan özel kodlardan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md)

 [CA1801: Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md)

 [CA1804: Kullanılmayan yerel öğeleri kaldırın](../code-quality/ca1804-remove-unused-locals.md)
