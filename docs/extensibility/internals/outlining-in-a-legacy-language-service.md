---
title: Eski dil hizmetinde ana hat oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- outlining
- language services [managed package framework], outlining
- outlining, supporting in language services [managed package framework]
ms.assetid: 7b5578b4-a20a-4b94-ad4c-98687ac133b9
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 12ce11a057884f12466eb5c9c499b0822217b474
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53939180"
---
# <a name="outlining-in-a-legacy-language-service"></a>Eski Dil Hizmetinde Ana Hat Oluşturma
Anahat oluşturma, karmaşık bir program bir genel bakış veya anahat Daralt mümkün kılar. Örneğin, C# ' de tüm yöntemler yöntem imzası gösteren tek bir satır için daraltılabilirler. Ayrıca, yapılar ve sınıflar yalnızca yapılar ve sınıflar adlarını göstermek üzere daraltılabilir. Tek bir yöntem içinde deyim yalnızca ilk satır göstererek genel akışını göstermek için karmaşık mantık daratılmadan `foreach`, `if`, ve `while`.  
  
 Eski dil Hizmetleri bir VSPackage'ı bir parçası olarak uygulanır, ancak dil hizmeti özellikleri uygulamak için daha yeni MEF uzantıları kullanmaktır. Daha fazla bilgi için bkz: [izlenecek yol: Anahat oluşturma](../../extensibility/walkthrough-outlining.md).  
  
> [!NOTE]
>  Yeni bir düzenleyici API hemen kullanmaya başlamak öneririz. Bu dil hizmetinizin performansını ve yeni düzenleyici özellikleri yararlanmanıza olanak tanır.  
  
## <a name="enabling-support-for-outlining"></a>Anahat oluşturma için desteğini etkinleştirme  
 `AutoOutlining` Kayıt defteri girişini otomatik anahatlandırma etkinleştirmek için 1 olarak ayarlanır. Bir dosya yüklendiğinde veya gizli bölgeleri belirleyin ve ana hat oluşturma karakterleri göstermek için değiştirilen otomatik anahat oluşturma tüm kaynak bir ayrıştırma ayarlar. Ana hat oluşturmayı da el ile kullanıcı tarafından denetlenebilir.  
  
 Değerini `AutoOutlining` kayıt defteri girdisi aracılığıyla elde edilebilir <xref:Microsoft.VisualStudio.Package.LanguagePreferences.AutoOutlining%2A> özelliği <xref:Microsoft.VisualStudio.Package.LanguagePreferences> sınıfı. `AutoOutlining` Kayıt defteri girişi, adlandırılmış bir parametre ile başlatılabilir <xref:Microsoft.VisualStudio.Shell.ProvideLanguageServiceAttribute> öznitelik (bkz [eski dil hizmetinde kaydetme](../../extensibility/internals/registering-a-legacy-language-service1.md) Ayrıntılar için).  
  
## <a name="the-hidden-region"></a>Gizli bölge  
 Anahat oluşturma sağlamak için dil hizmeti gizli bölgeler desteklemesi gerekir. Bu genişletilmiş veya daraltılmış metin yayılma vardır. Gizli bölgeler, küme ayraçlarını gibi standart dil simgeleri veya özel semboller sınırlandırılabilir. Örneğin, C# sahip bir `#region` / `#endregion` gizli bölge sınırlandıran çifti.  
  
 Gizli bölgeler olarak kullanıma sunulan bir gizli bölge yöneticisi tarafından yönetilir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> arabirimi.  
  
 Anahat oluşturma kullanan gizli bölgeler <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenRegion> arabirim ve aralık gizli bölge, geçerli görünür durumu ve ne zaman aralığı daraltılmış gösterilecek başlığı içermelidir.  
  
 Dil hizmeti ayrıştırıcısı kullanan <xref:Microsoft.VisualStudio.Package.AuthoringSink.AddHiddenRegion%2A> gizli bölgeler için varsayılan davranışa sahip yeni bir gizli bölge ekleme yöntemi sırasında <xref:Microsoft.VisualStudio.Package.AuthoringSink.AddHiddenRegion%2A> yöntemi anahat davranışını ve görünümünü özelleştirmenize olanak sağlar. Gizli bölgeler gizli bölge oturumuna verildi sonra [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] gizli bölgeler için dil hizmeti yönetir.  
  
 Gizli bölge oturumu kaldırıldığında belirlemeniz gerekiyorsa, gizli Bölge değiştirildiğinde veya belirli bir gizli bölge görülebilir emin olmanız gerekir; bir sınıftan türetilmelidir <xref:Microsoft.VisualStudio.Package.Source> sınıfı ve uygun yöntemleri geçersiz kılmak <xref:Microsoft.VisualStudio.Package.Source.OnBeforeSessionEnd%2A>, <xref:Microsoft.VisualStudio.Package.Source.OnHiddenRegionChange%2A>, ve <xref:Microsoft.VisualStudio.Package.Source.MakeBaseSpanVisible%2A>sırasıyla.  
  
### <a name="example"></a>Örnek  
 Gizli bölgeler için tüm küme ayracı çiftlerini oluşturmanın basitleştirilmiş bir örnek aşağıda verilmiştir. Dil Ayraç eşleştirme sağlar ve eşleştirilecek ayraçlar ve küme ayraçlarının en az dahil varsayılır ({ve}). Bu yaklaşım yalnızca tanım amaçlıdır. Tam bir uygulamayı durumlarda, tam bir işleme sahip olabileceği <xref:Microsoft.VisualStudio.Package.LanguageService.ParseSource%2A>. Bu örnek ayrıca nasıl ayarlanacağını gösterir <xref:Microsoft.VisualStudio.Package.LanguagePreferences.AutoOutlining%2A> tercihi `true` geçici olarak. Belirtmek için bir alternatifidir `AutoOutlining` parametresinde belirtilen `ProvideLanguageServiceAttribute` dil paketinizi özniteliği.  
  
 Bu örnek, yorumlar, dizeler ve sabit değerleri için C# kurallarını varsayar.  
  
```csharp  
using Microsoft.VisualStudio.Package;  
using Microsoft.VisualStudio.TextManager.Interop;  
  
namespace MyLanguagePackage  
{  
  
    public class MyLanguageService : LanguageService  
    {  
        private LanguagePreferences m_preferences;  
  
        public override LanguagePreferences  GetLanguagePreferences()  
        {  
            if (m_preferences == null)  
            {  
                m_preferences = new LanguagePreferences(this.Site,  
                                                        typeof(MyLanguageService).GUID,  
                                                        Name);  
                m_preferences.Init();  
                // Temporarily enabled auto-outlining  
                m_preferences.AutoOutlining = true;  
            }  
            return m_preferences;  
        }  
  
        public override AuthoringScope  ParseSource(ParseRequest req)  
        {  
            Source source = (Source) this.GetSource(req.FileName);  
            switch (req.Reason)  
            {  
               case ParseReason.HighlightBraces:  
               case ParseReason.MatchBraces:  
               case ParseReason.MemberSelectAndHighlightBraces:  
                  if (source.Braces != null)  
                  {  
                      foreach (TextSpan[] brace in source.Braces)  
                      {  
                         if (brace.Length == 2)  
                         {  
                             if (req.Sink.HiddenRegions == true   
                                   && source.GetText(brace[0]).Equals("{")   
                                   && source.GetText(brace[1]).Equals("}"))  
                             {  
                                //construct a TextSpan of everything between the braces  
                                TextSpan hideSpan = new TextSpan();  
                                hideSpan.iStartIndex = brace[0].iStartIndex;  
                                hideSpan.iStartLine = brace[0].iStartLine;  
                                hideSpan.iEndIndex = brace[1].iEndIndex;  
                                hideSpan.iEndLine = brace[1].iEndLine;  
                                req.Sink.ProcessHiddenRegions = true;  
                                req.Sink.AddHiddenRegion(hideSpan);  
                             }  
                             req.Sink.MatchPair(brace[0], brace[1], 1);  
                         }  
                         else if (brace.Length >= 3)  
                             req.Sink.MatchTriple(brace[0], brace[1], brace[2], 1);  
                  }  
        }  
                   break;  
               default:  
                   break;  
      }  
            // Must always return a valid AuthoringScope object.  
            return new MyAuthoringScope();  
        }  
    }  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Eski dil hizmeti özellikleri](../../extensibility/internals/legacy-language-service-features1.md)   
 [Eski Dil Hizmeti Kaydetme](../../extensibility/internals/registering-a-legacy-language-service1.md)