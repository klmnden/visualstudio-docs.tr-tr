---
title: Düzenleyici uzantısından DTE nesnesine erişme
ms.date: 04/24/2019
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], new - getting the DTE object
ms.assetid: c1f40bab-c6ec-45b0-8333-ea5ceb02a39d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1fb22793c3bfa805fae11c8bbea7f07c06fd5a85
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66322788"
---
# <a name="walkthrough-access-the-dte-object-from-an-editor-extension"></a>İzlenecek yol: Düzenleyici uzantısından DTE nesnesine erişme

Vspackage'larda, çağırarak DTE nesnesi alabilirsiniz <xref:Microsoft.VisualStudio.Shell.Package.GetService%2A> DTE nesnesi türü ile yöntemi. Yönetilen Genişletilebilirlik Çerçevesi (MEF) uzantılar, aldığınız <xref:Microsoft.VisualStudio.Shell.SVsServiceProvider> ve sonra çağrı <xref:Microsoft.VisualStudio.Shell.ServiceProvider.GetService%2A> yöntemi türünde <xref:EnvDTE.DTE>.

## <a name="prerequisites"></a>Önkoşullar

Bu izlenecek yolda takip etmek için Visual Studio SDK'yı yüklemeniz gerekir. Daha fazla bilgi için [Visual Studio SDK](../extensibility/visual-studio-sdk.md).

## <a name="get-the-dte-object"></a>DTE nesnesini Al

1. Oluşturma bir C# VSIX projesi ve adlandırın **DTETest**. Ekleme bir **Düzenleyicisi sınıflandırıcı** öğe şablonu ve adlandırın **DTETest**.

   Daha fazla bilgi için [bir düzenleyici öğesi şablonuyla uzantı oluşturma](../extensibility/creating-an-extension-with-an-editor-item-template.md).

::: moniker range=">=vs-2019"

2. Projeye aşağıdaki bütünleştirilmiş kod Başvurusu Ekle:

    - Microsoft.VisualStudio.Shell.Immutable.10.0

3. İçinde *DTETestProvider.cs* dosyasında, aşağıdaki ekleyin `using` yönergeleri:

    ```csharp
    using EnvDTE;
    using Microsoft.VisualStudio.Shell;
    ```

4. İçinde `DTETestProvider` sınıfı, içeri aktarma bir <xref:Microsoft.VisualStudio.Shell.SVsServiceProvider>.

    ```csharp
    [Import]
    internal SVsServiceProvider ServiceProvider = null;
    ```

5. İçinde `GetClassifier()` yöntemi, önce aşağıdaki kodu ekleyin `return` deyimi:

    ```csharp
   ThreadHelper.ThrowIfNotOnUIThread();
   DTE dte = (DTE)ServiceProvider.GetService(typeof(DTE));
   ```

::: moniker-end

::: moniker range="vs-2017"

2. Projenin aşağıdaki derleme başvuruları ekleyin:

   - EnvDTE
   - Microsoft.VisualStudio.Shell.Framework

3. İçinde *DTETestProvider.cs* dosyasında, aşağıdaki ekleyin `using` yönergeleri:

    ```csharp
    using EnvDTE;
    using Microsoft.VisualStudio.Shell;
    ```

4. İçinde `DTETestProvider` sınıfı, içeri aktarma bir <xref:Microsoft.VisualStudio.Shell.SVsServiceProvider>.

    ```csharp
    [Import]
    internal SVsServiceProvider ServiceProvider = null;
    ```

5. İçinde `GetClassifier()` yöntemi, önce aşağıdaki kodu ekleyin `return` deyimi:

    ```csharp
   DTE dte = (DTE)ServiceProvider.GetService(typeof(DTE));
   ```

::: moniker-end

## <a name="see-also"></a>Ayrıca bkz.

- [Dil hizmeti ve düzenleyici uzantı noktaları](../extensibility/language-service-and-editor-extension-points.md)
- [DTE kullanarak Visual Studio'yu başlatın](launch-visual-studio-dte.md)