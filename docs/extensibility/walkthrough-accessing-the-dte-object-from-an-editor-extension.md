---
title: 'İzlenecek yol: Düzenleyici uzantısından DTE nesnesine erişme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], new - getting the DTE object
ms.assetid: c1f40bab-c6ec-45b0-8333-ea5ceb02a39d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1319e539c185a231637b4e78d7ac0de9154ed8a3
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60105181"
---
# <a name="walkthrough-accessing-the-dte-object-from-an-editor-extension"></a>İzlenecek yol: Düzenleyici uzantısından DTE nesnesine erişme
Vspackage'larda, çağırarak DTE nesnesi alabilirsiniz <xref:Microsoft.VisualStudio.Shell.Package.GetService%2A> DTE nesnesi türü ile yöntemi. Yönetilen Genişletilebilirlik Çerçevesi (MEF) uzantılar, aldığınız <xref:Microsoft.VisualStudio.Shell.SVsServiceProvider> ve sonra çağrı <xref:Microsoft.VisualStudio.Shell.ServiceProvider.GetService%2A> yöntemi türünde <xref:EnvDTE.DTE>.

## <a name="prerequisites"></a>Önkoşullar
 Bu izlenecek yolda takip etmek için Visual Studio SDK'yı yüklemeniz gerekir. Daha fazla bilgi için [Visual Studio SDK](../extensibility/visual-studio-sdk.md).

## <a name="getting-the-dte-object"></a>DTE nesnesini alma

### <a name="to-get-the-dte-object-from-the-serviceprovider"></a>ServiceProvider DTE nesnesini almak için

1. Adlı bir C# VSIX projesi oluşturun `DTETest`. Bir düzenleyici sınıflandırıcı öğe şablonu ekleyin ve adlandırın `DTETest`. Daha fazla bilgi için [bir düzenleyici öğesi şablonuyla uzantı oluşturma](../extensibility/creating-an-extension-with-an-editor-item-template.md).

2. Projenin aşağıdaki derleme başvuruları ekleyin:

    - EnvDTE

    - EnvDTE80

    - Microsoft.VisualStudio.Shell.Immutable.10.0

3. Git *DTETest.cs* dosyasını bulun ve aşağıdakileri ekleyin `using` yönergeleri:

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

## <a name="see-also"></a>Ayrıca bkz.
- [Dil hizmeti ve düzenleyici uzantı noktaları](../extensibility/language-service-and-editor-extension-points.md)