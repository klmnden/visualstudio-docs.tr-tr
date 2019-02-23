---
title: Desteklenen kod değişiklikleri (C# ve Visual Basic) | Microsoft Docs
ms.date: 10/11/2017
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Edit and Continue [C#], supported code changes
- Edit and Continue [Visual Basic], supported code changes
ms.assetid: c7a48ea9-5a7f-4328-a9d7-f0e76fac399d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 753a3816b6432a58c5f79077c4e438db753297b9
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56692236"
---
# <a name="supported-code-changes-c-and-visual-basic"></a>Desteklenen kod değişiklikleri (C# ve Visual Basic)
Düzenle ve devam et, metot gövdeleri içinde kod değişiklikleri çoğu türde işler. Metot gövdeleri dışında çoğu değişiklikleri ve metot gövdeleri içindeki bazı değişiklikler, ancak hata ayıklama sırasında uygulanamaz. Desteklenmeyen bu değişiklikleri uygulamak için hata ayıklamayı durdurmak ve kod yeni bir sürümle yeniden başlatmanız gerekir.

## <a name="supported-changes-to-code"></a>Desteklenen kod değişiklikleri

Aşağıdaki tabloda yapılan değişiklikleri gösterir C# ve Visual Basic kodunu oturum başlatmadan hata ayıklama oturumu sırasında.

|Dil öğesi/özelliği|Desteklenen düzenleme işlemi|Sınırlamalar|
|-|-|-|
|Türler|Yöntemler, alanlar, Oluşturucular, tarayıcılarınızda ekleyin|[Evet](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|
|Yineleyiciler|Ekleme veya değiştirme|Hayır|
|Async ve await ifadeleri|Ekleme veya değiştirme|[Evet](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|
|Dinamik nesneler|Ekleme veya değiştirme|Hayır|
|lambda ifadeleri|Ekleme veya değiştirme|[Evet](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|
|LINQ ifadeleri|Ekleme veya değiştirme|[Lambda ifadeleri ile aynı](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|

> [!NOTE]
> Dize ilişkilendirme ve null koşullu işleçleri gibi yeni dil özellikleri genellikle Düzenle ve devam et tarafından desteklenir. En güncel bilgiler için bkz: [Enc desteklenen düzenler](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits) sayfası.

## <a name="unsupported-changes-to-code"></a>Desteklenmeyen kod değişiklikleri
 Aşağıdaki değişiklikler uygulanamaz C# ve Visual Basic kodu hata ayıklama oturumu sırasında:

-   Geçerli deyimi veya herhangi bir etkin deyim yapılan değişiklikler.

     Etkin deyimleri için geçerli durumunu almak için çağrılan işlevler çağrı yığını üzerinde herhangi bir deyim ekleyin.

     Geçerli deyimi kaynak penceresinde sarı arka plan olarak işaretlenir. Diğer etkin deyimleri gölgeli bir arka plan işaretlenir ve salt okunurdur. Bu varsayılan renkleri değiştirilebilir **seçenekleri** iletişim kutusu.

- Aşağıdaki tabloda, dil öğesi tarafından desteklenmeyen kod değişiklikleri gösterir.

|Dil öğesi/özelliği|Desteklenmeyen düzenleme işlemi|
|-|-|
|Tüm kod öğeleri|Yeniden adlandırma|
|Ad Alanları|Ekle|
|Ad alanlarını, türleri, üyeleri|Sil|
|Genel Türler|Ekleme veya değiştirme|
|Arabirimler|Değiştirme|
|Türler|Soyut ya da sanal bir üye eklemek için geçersiz kılma (bkz [ayrıntıları](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits))|
|Türler|Yıkıcı Ekle|
|Üyeler|Gömülü birlikte çalışma türü başvuru üyesi değiştirme|
|Üyeler (Visual Basic)|On Error veya Resume deyimi bir üyesiyle değiştirin|
|Üyeler (Visual Basic)|Bir Aggregate, Group By, basit katılın veya grup katılın LINQ sorgu yan tümcesi içeren bir üye değiştirme|
|Yöntemler|İmzaları değiştirme|
|Yöntemler|Bir duruma soyut yöntemi soyut olmayan bir yöntem gövdesi ekleyerek olun|
|Yöntemler|Yöntem gövdesi silme|
|Öznitelikler|Ekleme veya değiştirme|
|Olaylar veya özellikler|Bir tür parametresi, temel türü değiştirme temsilci türü veya dönüş türü |
|Operatörler ya da dizin oluşturucular|Bir tür parametresi, temel türü değiştirme temsilci türü veya dönüş türü |
|catch blokları|Etkin bir deyim içerdiği durumlarda değiştirme|
|try-catch-finally blokları|Etkin bir deyim içerdiği durumlarda değiştirme|
|using deyimleri|Ekle|
|zaman uyumsuz yöntemler/lambdalar|.NET Framework 4 hedefleyen bir proje içinde zaman uyumsuz yöntem/lambda değiştirebilir ve daha düşük (bkz [ayrıntıları](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits))|
|Yineleyiciler|.NET Framework 4 hedefleyen bir proje içinde bir yineleyici değiştirebilir ve daha düşük (bkz [ayrıntıları](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits))|

## <a name="unsafe-code"></a>Güvenli olmayan kod
 Güvenli olmayan kod değişiklikleri başka bir kısıtlama ile güvenli kod değişiklikleri onunla aynı sınırlamalara sahiptir: Düzenle ve devam et değişiklikleri içeren bir yöntemi içinde güvenli olmayan kod desteklemiyor `stackalloc` işleci.

## <a name="unsupported-app-scenarios"></a>Desteklenmeyen uygulama senaryoları

Desteklenmeyen uygulamalar ve platformlar, ASP.NET 5, Silverlight 5 ve Windows 8.1 içerir.

> [!NOTE]
> Desteklenen uygulamaların UWP dahil Windows 10 ve .NET Framework 4.6 hedefleyen x86 ve x64 uygulamaları (yalnızca masaüstü bir sürümünde olan .NET Framework) masaüstü veya sonraki sürümleri.

## <a name="unsupported-scenarios"></a>Desteklenmeyen senaryolar
 Düzenle ve devam et hata ayıklama aşağıdaki senaryolarda kullanılabilir değil:

-   Karma mod (yerel/yönetilen) hata ayıklama.

-   SQL hata ayıklama.

-   Bir Dr hata ayıklama. Watson dökümü.

-   Katıştırılmış çalışma zamanı uygulama hata ayıklama.

-   Bir uygulama kullanarak hata ayıklama iliştirme (**hata ayıklama > iliştirme**) seçerek uygulamayı çalıştırmak yerine **Başlat** gelen **hata ayıklama** menüsü.

-   En iyi duruma getirilmiş kodda hata ayıklama.

-   Derleme hataları nedeniyle oluşturmak yeni bir sürüm başarısız olduktan sonra kodunuzu eski bir sürümü hata ayıklama.

## <a name="see-also"></a>Ayrıca Bkz.
- [Düzenle ve Devam Et (Visual C#)](../debugger/edit-and-continue-visual-csharp.md)
- [Nasıl yapılır: Düzenle ve Devam Et’i Kullanma (C#)](../debugger/how-to-use-edit-and-continue-csharp.md)