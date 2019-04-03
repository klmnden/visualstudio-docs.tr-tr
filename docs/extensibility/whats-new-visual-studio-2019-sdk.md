---
title: Visual Studio 2019 SDK'da yenilikler | Microsoft Docs
ms.date: 03/29/2019
ms.topic: conceptual
ms.assetid: 4a07607b-0c87-4866-acd8-6d68358d6a47
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: daa4203ccdcbce89f1eb09efdd9433210bcbc987
ms.sourcegitcommit: 509fc3a324b7748f96a072d0023572f8a645bffc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58856651"
---
# <a name="whats-new-in-the-visual-studio-2019-sdk"></a>Visual Studio 2019 SDK'da yenilikler nelerdir?

Visual Studio SDK'sı için Visual Studio 2019 aşağıdaki yeni ve güncelleştirilmiş özelliklere sahiptir.

## <a name="synchronously-autoloaded-extensions-warning"></a>Zaman uyumlu olarak uyarı autoloaded uzantıları

Herhangi bir yüklü uzantılarını autoloaded başlangıçta zaman uyumlu olarak ise kullanıcılar artık bir uyarı görürsünüz. Uyarı hakkında daha fazla bilgi [zaman uyumlu olarak autoloaded uzantıları](synchronously-autoloaded-extensions.md).

## <a name="single-unified-visual-studio-sdk"></a>Visual Studio SDK tek ve birleştirilmiş

Artık tüm Visual Studio SDK varlıkları tek bir NuGet paketi alabilirsiniz [Microsoft.VisualStudio.SDK](https://www.nuget.org/packages/microsoft.visualstudio.sdk).

## <a name="editor-registration-enhancements"></a>Düzenleyici kayıt geliştirmeleri

Burada bir düzenleyici (örneğin, .xaml ve .rc) belirli uzantılar için kendi benzeşimi bildirebilir veya herhangi bir uzantı için uygun olan özel düzenleyici kayıt desteklenen oluşturulduktan sonra Visual Studio (. *). Visual Studio 2019 sürüm 16.1 başlayarak, biz Düzenleyicisi kaydı desteğini genişletmek.

### <a name="filenames"></a>Dosya Adları

Ek olarak ya da yerine, belirli bir dosya uzantısı için destek kaydetme bir düzenleyicide yeni uygulayarak belirli dosya adlarını desteklediğini kaydedebilirsiniz `ProvideEditorFilename` Öznitelik Düzenleyicisi'nin paketi.

Örneğin, tüm .json dosyaları destekleyen bir düzenleyici bu uygulanacak `ProvideEditorExtension` özniteliği için paketi:

```cs
[ProvideEditorExtension(typeof(MyEditor), ".json", MyEditor.Priority)]
```

Yalnızca birkaç iyi bilinen .json dosyaları MyEditor destekliyorsa 16.1 ile başlayarak, bunun yerine bu uygulamadan `ProvideEditorFilename` öznitelikler için kendi paket:

```cs
[ProvideEditorFilename(typeof(MyEditor), "particular.json", MyEditor.Priority)]
[ProvideEditorFilename(typeof(MyEditor), "special.json",    MyEditor.Priority)]
```

### <a name="uicontexts"></a>Uıcontexts

Bir düzenleyici etkinleştirildiğinde temsil eden bir veya daha fazla Uıcontexts kaydedebilirsiniz. Uıcontexts kayıtlı bir veya daha fazla örneği uygulayarak `ProvideEditorUIContextAttribute` Düzenleyici kaydeder paketi.

Bir düzenleyici kayıtlı Uıcontexts varsa:

- Verilen uzantılı bir dosya açıldığında, kayıtlı Uıcontexts en az biri etkin olursa, düzenleyici Düzenleyicisi aramaya dahil edilir.
- Kayıtlı Uıcontexts hiçbiri etkin olursa, düzenleyici Düzenleyicisi aramaya dahil edilmez.

Bir düzenleyici herhangi Uıcontexts kaydolursanız değil, bu uzantı için düzenleyici arama her zaman dahildir.

Örneğin, bir düzenleyici yalnızca kullanılabilir bir C# proje açıksa, bu benzeşim uygulayarak bildirebilirsiniz bir `ProvideEditorUIContext` özniteliği:

```cs
[ProvideEditorUIContext(typeof(MyEditor), KnownUIContexts.CSharpProjectContext)]
```