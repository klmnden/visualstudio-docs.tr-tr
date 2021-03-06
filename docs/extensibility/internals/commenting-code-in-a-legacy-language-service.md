---
title: Eski dil hizmetinde koda açıklama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- comments, supporting in language services [managed package framework]
- language services [managed package framework], commenting code
ms.assetid: 9600d6f0-e2b6-4fe0-b935-fb32affb97a4
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ec42d81a2d472cec5f96cbeec416801c22465834
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66342039"
---
# <a name="comment-code-in-a-legacy-language-service"></a>Eski dil hizmetinde kod açıklaması
Programlama dilleri, normalde açıklama eklemek veya kod açıklaması için bir yol sağlar. Bir yorum, metin, kod hakkında ek bilgi sağlar ancak derleme veya yorumu sırasında yok sayılır bölümüdür.

 Yönetilen paket framework (MPF) sınıfları, yorum ve uncommenting seçili metin için destek sağlar.

## <a name="comment-styles"></a>Açıklama stilleri
Açıklama iki genel stiller şunlardır:

1. Yorumu tek bir satırda olduğu satırlı yorumlar.

2. Bloğu açıklamaları, burada açıklama birden fazla satır içerebilir.

Satırlı yorumlar, genellikle başlangıç karakteri (ya da karakterler) bloğu açıklamaları sırasında hem başlangıç ve bitiş karakterlerini sahip sahiptir. Örneğin, C# ' ta bir satırı yorum ile başlayan `//`, ve bir blok açıklama ile başlayan `/*` ve ile sona eren `*/`.

Kullanıcı komutu seçtiğinde **yorum seçimi** gelen **Düzenle** > **Gelişmiş** menüsünden komut yönlendirileceğini <xref:Microsoft.VisualStudio.Package.Source.CommentSpan%2A> yöntemi <xref:Microsoft.VisualStudio.Package.Source> sınıfı. Kullanıcı komutu seçtiğinde **seçimi işletilir satıra çevir**, komut yönlendirilir <xref:Microsoft.VisualStudio.Package.Source.UncommentSpan%2A> yöntemi.

## <a name="support-code-comments"></a>Destek kod açıklamaları
 Dil hizmeti desteği kodu yorumlarınızı yoluyla olabilir `EnableCommenting` parametresinin adlı <xref:Microsoft.VisualStudio.Shell.ProvideLanguageServiceAttribute> . Bu ayarlar <xref:Microsoft.VisualStudio.Package.LanguagePreferences.EnableCommenting%2A> özelliği <xref:Microsoft.VisualStudio.Package.LanguagePreferences> sınıfı. Dil hizmeti özellikleri ayarlama hakkında daha fazla bilgi için bkz. [eski dil hizmeti kayıt](../../extensibility/internals/registering-a-legacy-language-service1.md).

 Geçersiz kılmalısınız <xref:Microsoft.VisualStudio.Package.Source.GetCommentFormat%2A> döndürülecek yöntemi bir <xref:Microsoft.VisualStudio.Package.CommentInfo> açıklama karakterler dil yapısı. C#-stili satır yorum karakterlerdir, varsayılan.

### <a name="example"></a>Örnek
 Örnek uygulama için işte <xref:Microsoft.VisualStudio.Package.Source.GetCommentFormat%2A> yöntemi.

```csharp
using Microsoft.VisualStudio.Package;

namespace MyLanguagePackage
{
    class MySource : Source
    {
        public override CommentInfo GetCommentFormat() {
            CommentInfo info = new CommentInfo();
            info.LineStart       = "//";
            info.BlockStart      = "/*";
            info.BlockEnd        = "*/";
            info.UseLineComments = true;
            return info;
        }
    }
}
```

## <a name="see-also"></a>Ayrıca bkz.
- [Eski dil hizmeti özellikleri](../../extensibility/internals/legacy-language-service-features1.md)
- [Eski dil hizmeti kaydedin](../../extensibility/internals/registering-a-legacy-language-service1.md)