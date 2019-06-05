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
ms.openlocfilehash: 89edba30a95d61268aebb26de8d973f6201c0fcf
ms.sourcegitcommit: 5483e399f14fb01f528b3b194474778fd6f59fa6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/05/2019
ms.locfileid: "66714758"
---
# <a name="ca2210-assemblies-should-have-valid-strong-names"></a>CA2210: Derlemelerin geçerli tanımlayıcı adları olmalıdır

|||
|-|-|
|TypeName|AssembliesShouldHaveValidStrongNames|
|CheckId|CA2210|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Bir derlemeyi tanımlayıcı bir ad ile imzalı değil, tanımlayıcı adı doğrulanamadı veya tanımlayıcı adı geçerli kayıt defteri ayarları bilgisayarın geçerli olmaz.

## <a name="rule-description"></a>Kural açıklaması

Bu kural, alır ve bir derlemenin tanımlayıcı adı doğrular. Aşağıdakilerden biri doğruysa bir ihlali oluşur:

- Derlemeyi tanımlayıcı bir ada sahip değil.

- Derleme imzalama sonra değiştirildi.

- Derleme gecikmeli imzalanmış.

- Derleme yanlış imzalı veya imzalama başarısız oldu.

- Derleme doğrulama geçirmek kayıt defteri ayarları gerektirir. Örneğin, tanımlayıcı ad Aracı (Sn.exe), derleme için doğrulama atlama için kullanıldı.

Güçlü ad oynanmış derlemeyi bilmeden yükleyerek istemcileri korur. Güçlü adı olmayan derlemeler oldukça sınırlı sayıda senaryo dışında kullanılmamalıdır. Düzgün imzalanmamış derlemeleri paylaşırsanız veya dağıtırsanız, derleme aslı bozuabilir, ortak dil çalışma zamanı derlemeyi yükleyemeyebilir veya kullanıcı kendi bilgisayarındaki doğrulamayı devre dışı bırakabilir. Bir derlemeyi tanımlayıcı ad aşağıdaki dezavantajları vardır:

- Kendi kaynakları doğrulanamıyor.

- Ortak dil çalışma zamanı derlemenin içeriğini değiştirilmiş, kullanıcıları uyarın olamaz.

- Genel bütünleştirilmiş kod önbelleğine yüklenemiyor.

Yüklenecek unutmayın ve gecikmeli imzalanmış bir bütünleştirilmiş kod çözümleme, derleme için doğrulama devre dışı bırakmanız gerekir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

### <a name="create-a-key-file"></a>Bir anahtar dosyası oluştur

Aşağıdaki yordamlardan birini kullanın:

- Kullanım [derleme bağlayıcı Aracı (Al.exe)](/dotnet/framework/tools/al-exe-assembly-linker).

- .NET Framework 2.0, kullanın `/keyfile` veya `/keycontainer` derleyici seçeneği [/keyfile (derlemeyi imzalamak için anahtar belirtin veya anahtar çiftini)](/cpp/build/reference/keyfile-specify-key-or-key-pair-to-sign-an-assembly) veya  [ /keycontainer (derlemeyi imzalamak için bir anahtar kapsayıcısı belirtin)](/cpp/build/reference/keycontainer-specify-a-key-container-to-sign-an-assembly) bağlayıcı seçeneğini C++).

- .NET Framework v1.0 veya v1.1 için kullanın <xref:System.Reflection.AssemblyKeyFileAttribute?displayProperty=fullName> veya <xref:System.Reflection.AssemblyKeyNameAttribute?displayProperty=fullName> özniteliği.

### <a name="sign-your-assembly-with-a-strong-name-in-visual-studio"></a>Derlemenizin tanımlayıcı bir adla Visual Studio'da oturum açın

1. Visual Studio'da çözümünüzü açın.

2. İçinde **Çözüm Gezgini**, projenize sağ tıklayın ve ardından **özellikleri.**

3. Tıklayın **imzalama** sekmesine tıklayın ve **derlemeyi imzalamayı** onay kutusu.

4. Gelen **bir tanımlayıcı ad anahtar dosyası seç**seçin **yeni**.

   **Katı ad anahtarı oluştur** penceresinde gösterilir.

5. İçinde **anahtar dosya adını**, tanımlayıcı ad anahtarınız için bir ad yazın.

6. Anahtarı bir parolayla koruyun ve ardından isteyip istemediğinizi seçin **Tamam**.

7. İçinde **Çözüm Gezgini**, projenize sağ tıklayın ve ardından **yapı**.

### <a name="sign-your-assembly-with-a-strong-name-outside-visual-studio"></a>Derlemenizi Visual Studio dışında bir tanımlayıcı adla imzalama

Kullanım [tanımlayıcı ad Aracı (Sn.exe)](/dotnet/framework/tools/sn-exe-strong-name-tool).

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Derleme ortamında kullandıysanız yalnızca bu kuraldan bir uyarıyı bastırmak burada içeriğiyle oynama bir sorun değildir.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Reflection.AssemblyKeyFileAttribute?displayProperty=fullName>
- <xref:System.Reflection.AssemblyKeyNameAttribute?displayProperty=fullName>
- [Nasıl yapılır: Derlemeyi tanımlayıcı bir adla imzalama](/dotnet/framework/app-domains/how-to-sign-an-assembly-with-a-strong-name)
- [Sn.exe (Tanımlayıcı Ad Aracı)](/dotnet/framework/tools/sn-exe-strong-name-tool)