---
title: Hangi&#39;s MSBuild 15'deki yenilikler | Microsoft Docs
ms.date: 03/01/2017
ms.topic: conceptual
ms.assetid: 9976b6fd-d052-4017-b848-35b5bf4b2f66
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
monikerRange: vs-2017
ms.openlocfilehash: 718ef14fda76df87dc4627dc518e993058896471
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62777990"
---
# <a name="whats-new-in-msbuild-15"></a>MSBuild 15'te Yenilikler

MSBuild olarak kullanıma sunuldu parçası [.NET Core SDK'sı](https://www.microsoft.com/net/download/core) ve Windows, macOS ve Linux üzerinde .NET Core projeleri oluşturabilirsiniz.

## <a name="changed-path"></a>Değiştirilen yolu

 MSBuild, şimdi Visual Studio'nun her sürümü altında bir klasöre yüklenir. Örneğin, *C:\Program Files (x86) \Microsoft Visual Studio\2017\Enterprise\MSBuild*. MSBuild bulmak için aşağıdaki PowerShell modülünü de kullanabilirsiniz: [vssetup.powershell](https://github.com/Microsoft/vssetup.powershell).

 MSBuild artık genel derleme önbelleğinde yüklü değil. MSBuild'ı programlı olarak başvurmak için NuGet paketlerini kullanın. Daha fazla bilgi için [MSBuild 15.0 için var olan uygulamayı güncelleştirme](../msbuild/updating-an-existing-application.md).

## <a name="changed-properties"></a>Özellikleri değiştirilmiş

 Aşağıdaki MSBuild özellikleri nedeniyle yeni sürüm numarası güncelleştirildi.

- `MSBuildToolsVersion` Bu araçlar için 15.0 sürümüdür. Derleme 15.1.0.0 sürümüdür.

- `MSBuildToolsPath` artık sabit bir konum vardır. Varsayılan olarak bulunur *MSBuild\15.0\Bin* klasörüyle ilgili Visual Studio yükleme konumunu, ancak Visual Studio yükleme konumu yükleme sırasında değiştirilebilir.

- `ToolsVersion` değerleri, kayıt defterinde artık ayarlanır.

- `SDK35ToolsPath` Ve `SDK40ToolsPath` noktası özelliklerini (örneğin, 10.0A 4.X araçları için) Visual Studio'nun bu sürümü ile paketlenmiştir .NET Framework SDK'sına.

## <a name="updates"></a>Güncelleştirmeler
- [Proje öğesi](../msbuild/project-element-msbuild.md) yeni bir `SDK` özniteliği. Ayrıca `Xmlns` özniteliği, artık isteğe bağlıdır. Daha fazla bilgi için `SDK` özniteliği için bkz: [nasıl yapılır: MSBuild proje SDK'ları kullanın](../msbuild/how-to-use-project-sdk.md), [paketler, meta paketler ve çerçeveler](/dotnet/core/packages) ve [csproj eklemeler biçimlendirmek için .NET Core](/dotnet/core/tools/csproj).
- [Öğe unsuru](../msbuild/item-element-msbuild.md) dış hedefleri olan yeni bir `Update` özniteliği. Ayrıca, kısıtlama `Remove` özniteliği ortadan kaldırılmıştır.
- *Directory.Build.props* özelleştirmeleri bir dizin altında projelerine sağlayan kullanıcı tanımlı bir dosya. Bu dosya gelen otomatik olarak içeri aktarılır *Microsoft.Common.props* sürece özelliği `ImportDirectoryBuildTargets` ayarlanır **false**. *Directory.Build.targets* tarafından alınan *Microsoft.Common.targets*.
- Herhangi bir meta veri öznitelikleri geçerli listesi ile çakışmadığından bir ad ile isteğe bağlı olarak bir özniteliği olarak ifade edilebilir. Daha fazla bilgi için [öğe](../msbuild/item-element-msbuild.md).

## <a name="new-property-functions"></a>Yeni özellik işlevleri

- `EnsureTrailingSlash` zaten yoksa eğik bir yolu ekler.
- `NormalizePath` yol öğesi bir araya getirir ve çıkış dizesi geçerli işletim sistemi için doğru dizin ayırıcı karakterleri sahip olmasını sağlar.
- `NormalizeDirectory` yol öğesi bir araya getirir, sonunda bir eğik çizgi sağlar ve çıkış dizesi geçerli işletim sistemi için doğru dizin ayırıcı karakterleri sahip olmasını sağlar.
- `GetPathOfFileAbove` Bu tek hemen önceki dosya yolunu döndürür. Arama için işlevsel olarak eşdeğerdir `<Import Project="$([MSBuild]::GetDirectoryNameOfFileAbove($(MSBuildThisFileDirectory), dir.props))\dir.props" />`

## <a name="see-also"></a>Ayrıca bkz.
- [MSBuild](../msbuild/msbuild.md)
