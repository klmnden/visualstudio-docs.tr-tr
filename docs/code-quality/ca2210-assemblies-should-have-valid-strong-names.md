---
title: 'CA2210: Derlemelerin geçerli tanımlayıcı adları olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- AssembliesShouldHaveValidStrongNames
- CA2210
helpviewer_keywords:
- AssembliesShouldHaveValidStrongNames
- CA2210
ms.assetid: 8ed33d1c-8ec6-4b47-a692-e22dc8693088
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 54f7d3a0efc2f6199c030c8dd488de3b5b158240
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231718"
---
# <a name="ca2210-assemblies-should-have-valid-strong-names"></a>CA2210: Derlemelerin geçerli tanımlayıcı adları olmalıdır

|||
|-|-|
|TypeName|AssembliesShouldHaveValidStrongNames|
|CheckId|CA2210|
|Kategori|Microsoft.Design|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bütünleştirilmiş kod bir tanımlayıcı ad ile imzalanmamıştır, tanımlayıcı ad doğrulanamadı veya tanımlayıcı ad bilgisayarın geçerli kayıt defteri ayarları olmadan geçerli değildir.

## <a name="rule-description"></a>Kural açıklaması

Bu kural, bir derlemenin tanımlayıcı adını alır ve doğrular. Aşağıdakilerden biri doğruysa bir ihlal oluşur:

- Derlemenin tanımlayıcı adı yok.

- İmza, imzalandıktan sonra değiştirildi.

- Derleme gecikmeli imzalanmış.

- Derleme yanlış imzalanmış veya imzalama başarısız oldu.

- Derleme için kayıt defteri ayarlarının doğrulanması gerekir. Örneğin, tanımlayıcı ad Aracı (sn. exe), derleme için doğrulamayı atlamak için kullanılır.

Güçlü ad oynanmış derlemeyi bilmeden yükleyerek istemcileri korur. Güçlü adı olmayan derlemeler oldukça sınırlı sayıda senaryo dışında kullanılmamalıdır. Düzgün imzalanmamış derlemeleri paylaşırsanız veya dağıtırsanız, derleme aslı bozuabilir, ortak dil çalışma zamanı derlemeyi yükleyemeyebilir veya kullanıcı kendi bilgisayarındaki doğrulamayı devre dışı bırakabilir. Güçlü adı olmayan bir derleme aşağıdaki dezavantajlardan daha fazlasını içerir:

- Kaynakları doğrulanamıyor.

- Ortak dil çalışma zamanı, derlemenin içeriği değiştirilmişse kullanıcıları uyaramaz.

- Genel bütünleştirilmiş kod önbelleğine yüklenemez.

Gecikmeli imzalanmış bir derlemeyi yüklemek ve analiz etmek için, derlemenin doğrulanmasını devre dışı bırakmanız gerektiğini unutmayın.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

### <a name="create-a-key-file"></a>Anahtar dosyası oluşturma

Aşağıdaki yordamlardan birini kullanın:

- [Derleme bağlayıcı aracı 'nı (al. exe)](/dotnet/framework/tools/al-exe-assembly-linker)kullanın.

- 2,0 `/keyfile` .NET Framework için, veya `/keycontainer` derleyici seçeneği olan [/keyfile (bir derlemeyi imzalamak için anahtar veya anahtar çiftini belirt](/cpp/build/reference/keyfile-specify-key-or-key-pair-to-sign-an-assembly) ) veya [/keycontainer (bir derlemeyi imzalamak için anahtar kapsayıcısı belirtin)](/cpp/build/reference/keycontainer-specify-a-key-container-to-sign-an-assembly) ' C++ı kullanın.

- .NET Framework v 1.0 veya v 1.1 için ya da <xref:System.Reflection.AssemblyKeyFileAttribute?displayProperty=fullName> <xref:System.Reflection.AssemblyKeyNameAttribute?displayProperty=fullName> özniteliğini kullanın.

### <a name="sign-your-assembly-with-a-strong-name-in-visual-studio"></a>Visual Studio 'da derlemenizi tanımlayıcı bir adla imzalama

1. Visual Studio 'da çözümünüzü açın.

2. **Çözüm Gezgini**, projenize sağ tıklayın ve ardından Özellikler ' e tıklayın **.**

3. **İmzalama** sekmesine tıklayın ve **derlemeyi imzala** onay kutusunu seçin.

4. **Bir tanımlayıcı ad anahtar dosyası seçin**listesinden **Yeni**' yi seçin.

   **Tanımlayıcı ad oluştur anahtar** penceresi görüntülenecektir.

5. **Anahtar dosya adı**' nda, tanımlayıcı ad anahtarınız için bir ad yazın.

6. Anahtarın bir parolayla korunmasını seçin ve ardından **Tamam**' a tıklayın.

7. **Çözüm Gezgini**, projenize sağ tıklayın ve ardından **Oluştur**' a tıklayın.

### <a name="sign-your-assembly-with-a-strong-name-outside-visual-studio"></a>Derlemenizi Visual Studio dışında bir güçlü adla imzalama

[Tanımlayıcı ad aracı 'nı (sn. exe)](/dotnet/framework/tools/sn-exe-strong-name-tool)kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan yalnızca derleme, içerik üzerinde değişiklik yapılmasını gerektiren bir ortamda kullanılıyorsa bir uyarı göstermez.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Reflection.AssemblyKeyFileAttribute?displayProperty=fullName>
- <xref:System.Reflection.AssemblyKeyNameAttribute?displayProperty=fullName>
- [Nasıl yapılır: Bir derlemeyi güçlü bir adla imzala](/dotnet/framework/app-domains/how-to-sign-an-assembly-with-a-strong-name)
- [Sn.exe (Tanımlayıcı Ad Aracı)](/dotnet/framework/tools/sn-exe-strong-name-tool)