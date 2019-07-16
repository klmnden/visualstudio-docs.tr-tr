---
title: Eski dil hizmetinde koda açıklama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- comments, supporting in language services [managed package framework]
- language services [managed package framework], commenting code
ms.assetid: 9600d6f0-e2b6-4fe0-b935-fb32affb97a4
caps.latest.revision: 15
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: cd1405456ca9a6ba00926c82bcc7959ea36d26c2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68160911"
---
# <a name="commenting-code-in-a-legacy-language-service"></a>Eski Dil Hizmetinde Koda Açıklama Ekleme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Programlama dilleri, normalde açıklama eklemek veya kod açıklaması için bir yol sağlar. Bir yorum, metin, kod hakkında ek bilgi sağlar ancak derleme veya yorumu sırasında yok sayılır bölümüdür.  
  
 Yönetilen paket framework (MPF) sınıfları, yorum ve uncommenting seçili metin için destek sağlar.  
  
## <a name="comment-styles"></a>Açıklama stilleri  
 Açıklama iki genel stiller şunlardır:  
  
1. Yorumu tek bir satırda olduğu satırlı yorumlar.  
  
2. Bloğu açıklamaları, burada açıklama birden fazla satır içerebilir.  
  
   Satırlı yorumlar, genellikle başlangıç karakteri (ya da karakterler) bloğu açıklamaları sırasında hem başlangıç ve bitiş karakterlerini sahip sahiptir. Örneğin, C# ' ta bir satırı yorum ile başlayan / /, ve bir blok açıklama ile başlayan / * ve ile sona eren \*/.  
  
   Kullanıcı komutu seçtiğinde **yorum seçimi** gelen **Düzenle** -> **Gelişmiş** menüsünden komut yönlendirileceğini <xref:Microsoft.VisualStudio.Package.Source.CommentSpan%2A> yöntemi <xref:Microsoft.VisualStudio.Package.Source> sınıfı. Kullanıcı komutu seçtiğinde **seçimi işletilir satıra çevir**, komut yönlendirilir <xref:Microsoft.VisualStudio.Package.Source.UncommentSpan%2A> yöntemi.  
  
## <a name="supporting-code-comments"></a>Kod açıklamaları destekleme  
 Dil hizmeti desteği kodu yorumlarınızı yoluyla olabilir `EnableCommenting` parametresinin adlı <xref:Microsoft.VisualStudio.Shell.ProvideLanguageServiceAttribute> . Bu ayarlar <xref:Microsoft.VisualStudio.Package.LanguagePreferences.EnableCommenting%2A> özelliği <xref:Microsoft.VisualStudio.Package.LanguagePreferences> sınıfı. Dil servicce özellikleri ayarlama hakkında daha fazla bilgi için bkz. [eski dil hizmetinde kaydetme](../../extensibility/internals/registering-a-legacy-language-service1.md)).  
  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Eski dil hizmeti özellikleri](../../extensibility/internals/legacy-language-service-features1.md)   
 [Eski Dil Hizmeti Kaydetme](../../extensibility/internals/registering-a-legacy-language-service1.md)
