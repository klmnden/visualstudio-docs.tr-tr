---
title: 'Nasıl yapılır: Bir kitaplıktaki sembolleri tanımlama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- Call Browser tool, identifying symbols in the library
- Call Browser tool
ms.assetid: 8fb0de61-71e7-42d1-8b41-2ad915474384
caps.latest.revision: 22
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 5dcdbd6d9f9f24b094d62289b0b058edde8c156b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54801960"
---
# <a name="how-to-identify-symbols-in-a-library"></a>Nasıl yapılır: Bir Kitaplıktaki Sembolleri Tanımlama
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Sembol tarama araçlarını hiyerarşik görünümleri simgeleri görüntüler. Simgeler, ad alanları, nesneler, sınıflar, sınıf üyeleri ve diğer dil öğelerini temsil eder.  
  
 Hiyerarşideki her bir simge için simge kitaplığı tarafından geçirilen Gezinti bilgileri belirlenebilir [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] aşağıdaki arabirimleri aracılığıyla Nesne Yöneticisi:  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsNavInfo>  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsNavInfoNode>  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsEnumNavInfoNodes>.  
  
 Hiyerarşideki simgenin konumunu sembol ayırır. Belirli bir simgeye gitmek sembol tarama araçlarını sağlar. Simgeyi benzersiz, tam yolunu konumunu belirler. Her öğe yolunda bir düğümdür. Yolu, üst düzey düğüm ile başlar ve belirli bir sembolün ile sona erer. Örneğin, M1 yöntemi C1 sınıfın bir üyesidir ve C1 N1 ad alanında ise, tam M1 yöntemin N1 yoludur. C1. M1. Bu yol üç düğümü içerir: N1, C1 ve M1.  
  
 Gezinti bilgileri sağlayan [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] Nesne Yöneticisi'ni bulun, seçin ve tutmak için hiyerarşi içinde simgeleri seçili. Bir tarama aracını başka gezinme sağlar. Kullanırken **Nesne Tarayıcısı** sembolleri göz atmak için bir [!INCLUDE[vcprvc](../../includes/vcprvc-md.md)] proje, bir yöntem sağ tıklatın ve Başlat **çağrı tarayıcısı** yöntemi çağrısı grafikte görüntülenecek aracı.  
  
 İki tür simge konumu açıklar. Kurallı biçimi tam yolun simgenin temel alır. Bu hiyerarşi simgesinin benzersiz bir konumu temsil eder. Sembol tarama aracının bağımsızdır. Kurallı biçimi bilgi almak için [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] nesnesi Yöneticisi çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsNavInfo.EnumCanonicalNodes%2A> yöntemi. Sunu formun içinde belirli bir sembol Tarama Aracı simgenin konumunu açıklar. Simgenin konumunu hierarchicy diğer simgeler konumunu göredir. Belirli bir sembol, kurallı tek yolu ancak birkaç sunu yolu olabilir. Örneğin, C1 sınıfı, C2 sınıfından devralınır ve N1 ad alanındaki sınıflar **Nesne Tarayıcısı** aşağıdaki hiyerarşik ağaç görüntüler:  
  
```  
N1  
    C1  
        Bases and Interfaces  
            C2  
    C2  
        Bases and Interfaces  
. . . . . . . . . . .  
  
```  
  
 Bu örnekte, C2 sınıfı kurallı yolunu, N1 + C2 şeklindedir. C2 sunu yolunu C1 ve "Tabanları ve arabirimleri" düğümleri içerir: N1 + C1 + "tabanları ve arabirimleri" + C2.  
  
 Nesne manager çağrılarını sunu form bilgi almak için <xref:Microsoft.VisualStudio.Shell.Interop.IVsNavInfo.EnumPresentationNodes%2A> yöntemi.  
  
## <a name="identifying-a-symbol-in-the-hierarchy"></a>Hiyerarşideki bir simge tanımlama  
  
#### <a name="to-obtain-canonical-and-presentation-forms-information"></a>Kurallı edinme ve sunu forms bilgileri  
  
1.  Uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsNavInfo.EnumCanonicalNodes%2A> yöntemi.  
  
     Nesne yöneticisine kurallı simge yolunda bulunan düğüm listesi elde etmek için bu yöntemi çağırır.  
  
    ```vb  
    Public Function EnumCanonicalNodes(ByRef ppEnum As Microsoft.VisualStudio.Shell.Interop.IVsEnumNavInfoNodes) As Integer  
        Dim EnumNavInfoNodes As CallBrowserEnumNavInfoNodes = _New CallBrowserEnumNavInfoNodes(m_strMethod)  
        ppEnum = CType(EnumNavInfoNodes, IVsEnumNavInfoNodes)  
        Return 0  
    End Function  
    ```  
  
    ```csharp  
    public int EnumCanonicalNodes(out Microsoft.VisualStudio.Shell.Interop.IVsEnumNavInfoNodes ppEnum)  
    {  
        CallBrowserEnumNavInfoNodes EnumNavInfoNodes =  
            new CallBrowserEnumNavInfoNodes(m_strMethod);  
        ppEnum = (IVsEnumNavInfoNodes)(EnumNavInfoNodes);  
        return 0;  
    }  
  
    ```  
  
2.  Uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsNavInfo.EnumPresentationNodes%2A> yöntemi.  
  
     Nesne yöneticisine sembol sunu yolunda bulunan düğüm listesi elde etmek için bu yöntemi çağırır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sembol tarama araçlarını destekleme](../../extensibility/internals/supporting-symbol-browsing-tools.md)   
 [Nasıl yapılır: Nesne yöneticisine kitaplık kaydetme](../../extensibility/internals/how-to-register-a-library-with-the-object-manager.md)   
 [Nasıl yapılır: Nesne yöneticisine kitaplık tarafından sağlanan sembollerin listelerini kullanıma sunma](../../extensibility/internals/how-to-expose-lists-of-symbols-provided-by-the-library-to-the-object-manager.md)
