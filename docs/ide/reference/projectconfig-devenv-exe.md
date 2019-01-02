---
title: DevEnv ProjectConfig anahtarı
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- /projectconfig Devenv switch
- configurations, rebuilding
- deployment projects, creating
- configurations, cleaning
- deployment projects, specifying
- deployment projects, adding
- build configurations, specifying
- Devenv, /projectconfig switch
- projectconfig Devenv switch (/projectconfig)
- projects [Visual Studio], build configuration
- projects [Visual Studio], cleaning
ms.assetid: 6b54ef59-ffed-4f62-a645-1279ede97ebf
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 7ca481d23757cc9022042db42a6d4be477880367
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53967923"
---
# <a name="projectconfig-devenvexe"></a>/ProjectConfig (devenv.exe)

Derleme, temizleme, yeniden oluşturun veya adlı projeyi dağıtmak uygulanacak bir proje yapı yapılandırmasını belirtir **/project** bağımsız değişken.

## <a name="syntax"></a>Sözdizimi

```cmd
devenv SolutionName {/build|/clean|/rebuild|/deploy} SolnConfigName [/project ProjName] [/projectconfig ProjConfigName]
```

## <a name="arguments"></a>Arguments

|||
|-|-|
|/ Build|Tarafından belirtilen projeyi derler **/project** bağımsız değişken.|
|/ clean|Tüm ara dosyaları ve derleme sırasında oluşturulan çıktı dizini temizler.|
|/ Rebuild|Temizler ve ile belirtilen projeyi oluşturur **/project** bağımsız değişken.|
|/ deploy|Proje derleme veya yeniden sonra dağıtılması belirtir.|
|*SolnConfigName*|Gerekli. Adlı çözüm için uygulanacak çözüm yapılandırması adı *SolutionName*. Birden çok çözüm platformları kullanamıyorsanız, ayrıca platform örneğin belirtmelisiniz **"hata ayıklama\|Win32"**.|
|*SolutionName*|Gerekli. Çözüm dosyasının adını ve tam yolu.|
|/ project *ProjName*|İsteğe bağlı. Çözüm içindeki bir proje dosyasının adı ve yolu. Göreli bir yol girebilirsiniz *SolutionName* klasör proje dosyası veya projenin görünen adı veya tam yolu ve proje dosyasının adı.|
|/ projectconfig *ProjConfigName*|İsteğe bağlı. Bir proje adı ile belirtilen projeyi uygulanacak yapılandırma derleme **/project** bağımsız değişken. Birden çok çözüm platformları kullanamıyorsanız, ayrıca platform örneğin belirtmelisiniz **"hata ayıklama\|Win32"**.|

## <a name="remarks"></a>Açıklamalar

**/Projectconfig** anahtar kullanılmalıdır **/project** geçiş kapsamında bir **/build**, **/ clean**,  **/rebuild**, veya **/ deploy** komutu.

Çift tırnak içine boşluk dizeleri alın.

Komut penceresinde veya belirtilen herhangi bir günlük dosyasını hataları dahil olmak üzere, derlemeler için Özet bilgiler görüntülenebilir **/out** geçin.

## <a name="example"></a>Örnek

Aşağıdaki komut, "CSharpConsoleApp", "MySolution", "Debug" çözüm yapılandırması içindeki "Debug" Proje yapı yapılandırmasını kullanarak projeyi oluşturur:

```cmd
devenv "C:\Visual Studio Projects\MySolution\MySolution.sln" /build Debug /project "CSharpWinApp\CSharpWinApp.csproj" /projectconfig Debug
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [/ Project (devenv.exe)](../../ide/reference/project-devenv-exe.md)
- [/ Derleme (devenv.exe)](../../ide/reference/build-devenv-exe.md)
- [/ Clean (devenv.exe)](../../ide/reference/clean-devenv-exe.md)
- [/ Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)
- [/ (Devenv.exe) dağıtma](../../ide/reference/deploy-devenv-exe.md)
- [/ (Devenv.exe out)](../../ide/reference/out-devenv-exe.md)