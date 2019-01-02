---
title: Eski dil hizmetinde otomatik değişkenler penceresi için destek | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- language services [managed package framework], Autos window
- Autos window, supporting in language services [managed package framework]
ms.assetid: 47d40aae-7a3c-41e1-a949-34989924aefb
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d3f65b6d4daeb928cab1c59aaa5f1f2ded3225e6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53898222"
---
# <a name="support-for-the-autos-window-in-a-legacy-language-service"></a>Eski Dil Hizmetinde Otomatik Değişkenler Penceresi için Destek
**Otolar** penceresi değişkenleri ve hata ayıklanan programa (ya da bir kesme noktası veya bir özel durum nedeniyle) duraklatıldığında, kapsamdaki parametreleri gibi ifadeler görüntüler. İfadeler, değişkenler, yerel veya genel ve yerel kapsama değişmiş olan parametreler içerebilir. **Otolar** penceresi de bir sınıf, yapı veya başka bir tür örneklemeleri içerir. İfade değerlendiricisi değerlendirebilirsiniz herhangi bir şey olabilecek gösterilebileceği **Otolar** penceresi.  
  
 Yönetilen paket çerçevesini (MPF) için doğrudan destek sağlamaz **Otolar** penceresi. Ancak, kılarsanız <xref:Microsoft.VisualStudio.Package.LanguageService.GetProximityExpressions%2A> yöntemi, bir ifade içinde listesini döndürebilir **Otolar** penceresi.  
  
## <a name="implementing-support-for-the-autos-window"></a>Otomatik değişkenler penceresi için uygulama desteği  
 Tüm destek sağlamak için yapmanız gereken **Otolar** penceredir uygulamak için <xref:Microsoft.VisualStudio.Package.LanguageService.GetProximityExpressions%2A> yönteminde <xref:Microsoft.VisualStudio.Package.LanguageService> sınıfı. Uygulamanız ifadeleri gözükeceğini kaynak dosyasının bir konumda verilen karar vermelisiniz **Otolar** penceresi. Yöntem her bir dizenin tek bir ifade temsil eden bir dize listesi döndürür. Dönüş değeri <xref:Microsoft.VisualStudio.VSConstants.S_OK> listenin ifadeleri içerdiğini gösterir ancak <xref:Microsoft.VisualStudio.VSConstants.S_FALSE> gösterecek şekilde hiçbir ifade olduğunu gösterir.  
  
 Döndürülen gerçek ifadeler, değişkenlerin ya da kod bu konumda görünen parametreleri adlarıdır. İfade değerlendirici değerlerini ve ardından görüntülenen türlerini almak için bu adlar geçirilecek **Otolar** penceresi.  
  
### <a name="example"></a>Örnek  
 Aşağıdaki örnek bir uygulamasını gösterir <xref:Microsoft.VisualStudio.Package.LanguageService.GetProximityExpressions%2A> gelen ifadeleri bir listesini alır yöntemi <xref:Microsoft.VisualStudio.Package.LanguageService.ParseSource%2A> ayrıştırma nedeni kullanarak yöntemini <xref:Microsoft.VisualStudio.Package.ParseReason>. Her bir ifadenin olarak kaydırılan bir `TestVsEnumBSTR` uygulayan <xref:Microsoft.VisualStudio.TextManager.Interop.IVsEnumBSTR> arabirimi.  
  
 Unutmayın `GetAutoExpressionsCount` ve `GetAutoExpression` yöntemleri olan özel yöntemler `TestAuthoringSink` nesne ve bu örnek destek eklenmiştir. Eklenen hangi ifadeleri bir şekilde temsil ettikleri `TestAuthoringSink` ayrıştırıcının nesnesiyle (çağırarak <xref:Microsoft.VisualStudio.Package.AuthoringSink.AutoExpression%2A> yöntemi) ayrıştırıcının dışında erişilebilir.  
  
```csharp  
using Microsoft.VisualStudio;  
using Microsoft.VisualStudio.Package;  
using Microsoft.VisualStudio.TextManager.Interop;  
  
namespace TestLanguagePackage  
{  
    public class TestLanguageService : LanguageService  
    {  
        public override int GetProximityExpressions(IVsTextBuffer buffer,  
                                                    int line,  
                                                    int col,  
                                                    int cLines,  
                                                    out IVsEnumBSTR ppEnum)  
        {  
            int retval = VSConstants.E_NOTIMPL;  
            ppEnum = null;  
            if (buffer != null)  
            {  
                IVsTextLines textLines = buffer as IVsTextLines;  
                if (textLines != null)  
                {  
                    Source src = this.GetSource(textLines);  
                    if (src != null)  
                    {  
                        TokenInfo tokenInfo = new TokenInfo();  
                        string text = src.GetText();  
                        ParseRequest req = CreateParseRequest(src,  
                                                              line,  
                                                              col,  
                                                              tokenInfo,  
                                                              text,  
                                                              src.GetFilePath(),  
                                                              ParseReason.Autos,  
                                                              null);  
                        req.Scope = this.ParseSource(req);  
                        TestAuthoringSink sink = req.Sink as TestAuthoringSink;  
  
                        retval = VSConstants.S_FALSE;  
                        int spanCount = sink.GetAutoExpressionsCount();  
                        if (spanCount > 0) {  
                            TestVsEnumBSTR bstrList = new TestVsEnumBSTR();  
                            for (int i = 0; i < spanCount; i++)  
                            {  
                                TextSpan span;  
                                sink.GetAutoExpression(i, out span);  
                                string expression = src.GetText(span.iStartLine,  
                                                                span.iStartIndex,  
                                                                span.iEndLine,  
                                                                span.iEndIndex);  
                                bstrList.AddString(expression);  
                            }  
                            ppEnum = bstrList;  
                            retval = VSConstants.S_OK;  
                        }  
                    }  
                }  
            }  
            return retval;  
        }  
    }  
}  
```