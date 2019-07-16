---
title: 'İzlenecek yol: Düzenleyici uzantısından DTE nesnesine erişme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], new - getting the DTE object
ms.assetid: c1f40bab-c6ec-45b0-8333-ea5ceb02a39d
caps.latest.revision: 23
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 4b14b59465b94ddd0a09748f0e309166bf3d4114
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68148885"
---
# <a name="walkthrough-accessing-the-dte-object-from-an-editor-extension"></a>İzlenecek yol: Düzenleyici Uzantısından DTE Nesnesine Erişme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Vspackage'larda, çağırarak DTE nesnesi alabilirsiniz <xref:Microsoft.VisualStudio.Shell.Package.GetService%2A> DTE nesnesi türü ile yöntemi. Yönetilen Genişletilebilirlik Çerçevesi (MEF) uzantılar, aldığınız <xref:Microsoft.VisualStudio.Shell.SVsServiceProvider> ve sonra çağrı <xref:Microsoft.VisualStudio.Shell.ServiceProvider.GetService%2A> yöntemi türünde <xref:EnvDTE.DTE>.  
  
## <a name="prerequisites"></a>Önkoşullar  
 Bu izlenecek yolda takip etmek için Visual Studio SDK'yı yüklemeniz gerekir. Daha fazla bilgi için [Visual Studio SDK](../extensibility/visual-studio-sdk.md).  
  
## <a name="getting-the-dte-object"></a>DTE nesnesini alma  
  
#### <a name="to-get-the-dte-object-from-the-serviceprovider"></a>ServiceProvider DTE nesnesini almak için  
  
1. Adlı bir C# VSIX projesi oluşturun `DTETest`. Bir düzenleyici sınıflandırıcı öğe şablonu ekleyin ve adlandırın `DTETest`. Daha fazla bilgi için [bir düzenleyici öğesi şablonuyla uzantı oluşturma](../extensibility/creating-an-extension-with-an-editor-item-template.md).  
  
2. Projenin aşağıdaki derleme başvuruları ekleyin:  
  
    - EnvDTE  
  
    - EnvDTE80  
  
    - Microsoft.VisualStudio.Shell.Immutable.10.0  
  
3. DTETest.cs dosyasına gidin ve aşağıdakileri ekleyin `using` yönergeleri:  
  
    ```csharp  
    using EnvDTE;  
    using EnvDTE80;  
    using Microsoft.VisualStudio.Shell;  
  
    ```  
  
4. İçinde `GetDTEProvider` sınıfı, içeri aktarma bir <xref:Microsoft.VisualStudio.Shell.SVsServiceProvider>.  
  
    ```csharp  
    [Import]  
    internal SVsServiceProvider ServiceProvider = null;  
  
    ```  
  
5. İçinde `GetClassifier()` yöntemine aşağıdaki kodu ekleyin.  
  
    ```csharp  
    DTE dte = (DTE)ServiceProvider.GetService(typeof(DTE));  
  
    ```  
  
6. Kullanmanız gerekiyorsa <xref:EnvDTE80.DTE2> arabirimi DTE nesnesi çevirebilirsiniz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Dil Hizmeti ve Düzenleyici Uzantı Noktaları](../extensibility/language-service-and-editor-extension-points.md)
