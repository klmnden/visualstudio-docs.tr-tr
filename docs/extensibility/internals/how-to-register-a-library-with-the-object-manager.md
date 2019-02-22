---
title: 'Nasıl yapılır: Nesne yöneticisine kitaplık kaydetme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- libraries, registering with object manager
- IVsLibrary2 interface, registering library with object manager
- IVsSimpleLibrary2 interface, registering library with object manager
- IVsObjectManager2 interface, registering library with object manager
- libraries, symbol-browsing tools
ms.assetid: f124dd05-cb0f-44ad-bb2a-7c0b34ef4038
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fb764b453caa0a6230929fdc5fd002eb56550d67
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56609107"
---
# <a name="how-to-register-a-library-with-the-object-manager"></a>Nasıl yapılır: Nesne yöneticisine kitaplık kaydetme
Sembol tarama araçlarını, gibi **sınıf görünümü**, **Nesne Tarayıcısı**, **çağrı tarayıcısı** ve **sembol sonuçları Bul**, etkinleştirdiğiniz görüntülemek Projenizdeki veya dış bileşenler semboller. Simgeler, ad alanları, sınıflar, arabirimler, yöntemleri ve diğer dil öğelerini içerir. Kitaplıkları bu sembolleri izlemek ve bunlara üzerinden kullanıma sunacaksınız [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] araçları verilerle dolduran Nesne Yöneticisi.

 Nesne Yöneticisi, kullanılabilir tüm kitaplıkları izler. Her kitaplık nesne yöneticisine semboller için Sembol tarama araçlarını sağlamadan önce kaydetmeniz gerekir.

 Genellikle, bir VSPackage'ı yüklerken bir kitaplık kaydedin. Ancak, bunu başka bir zaman gerektiği şekilde gerçekleştirebilirsiniz. VSPackage'ı kapatıldığında kitaplığı kaydını silin.

 Kitaplığa kaydetmek için kullanın <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2.RegisterLibrary%2A> yöntemi. Bir yönetilen kod kitaplık için kullanmak <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2.RegisterSimpleLibrary%2A> yöntemi.

 Bir tür kitaplığının kaydını silmek için kullanın <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2.UnregisterLibrary%2A> yöntemi.

 Nesne Yöneticisi ' ni bir başvuru almak <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2>, geçmesi <xref:Microsoft.VisualStudio.Shell.Interop.SVsObjectManager> kimliği için hizmet `GetService` yöntemi.

## <a name="register-and-unregister-a-library-with-the-object-manager"></a>Kaydolun ve nesne yöneticisine kitaplık kaydını sil

### <a name="to-register-a-library-with-the-object-manager"></a>Nesne yöneticisine kitaplık kaydetmek için

1.  Bir kitaplığı oluşturun.

    ```vb
    Private m_CallBrowserLibrary As CallBrowser.Library = Nothing
    Private m_nLibraryCookie As UInteger = 0
    ' Create Library.
    m_CallBrowserLibrary = New CallBrowser.Library()
    ```

    ```csharp
    private CallBrowser.Library m_CallBrowserLibrary = null;
    private uint m_nLibraryCookie = 0;
    // Create Library.
    m_CallBrowserLibrary = new CallBrowser.Library();

    ```

2.  Bir nesnenin bir başvuru elde <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2> yazın ve arama <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2.RegisterSimpleLibrary%2A> yöntemi.

    ```vb
    Private Sub RegisterLibrary()
        If m_nLibraryCookie <> 0 Then
            Throw New Exception("Library already registered with Object Manager")
        End If

        ' Obtain a reference to IVsObjectManager2 type object.
        Dim objManager As IVsObjectManager2 = TryCast(GetService(GetType(SVsObjectManager)), IVsObjectManager2)
        If objManager Is Nothing Then
            Throw New NullReferenceException("GetService failed for SVsObjectManager")
        End If

        Try
            Dim hr As Integer = objManager.RegisterSimpleLibrary(m_CallBrowserLibrary, m_nLibraryCookie)
            Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure(hr)
        Catch e As Exception
            ' Code to handle any CLS-compliant exception.
            Trace.WriteLine(e.Message)
            Throw
        End Try
    End Sub
    ```

    ```csharp
    private void RegisterLibrary()
    {
        if (m_nLibraryCookie != 0)
            throw new Exception("Library already registered with Object Manager");

        // Obtain a reference to IVsObjectManager2 type object.
        IVsObjectManager2 objManager =
                          GetService(typeof(SVsObjectManager)) as IVsObjectManager2;
        if (objManager == null)
            throw new NullReferenceException("GetService failed for SVsObjectManager");

        try
        {
            int hr =
                objManager.RegisterSimpleLibrary(m_CallBrowserLibrary,
                                                 out m_nLibraryCookie);
                Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure(hr);
        }
        catch (Exception e)
        {
            // Code to handle any CLS-compliant exception.
            Trace.WriteLine(e.Message);
            throw;
        }
    }

    ```

### <a name="to-unregister-a-library-with-the-object-manager"></a>Nesne yöneticisine kitaplık kaydını kaldırmak için

1.  Bir nesnenin bir başvuru elde <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2> yazın ve arama <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2.UnregisterLibrary%2A> yöntemi.

    ```vb
    Private Sub UnregisterLibrary()
        If m_nLibraryCookie <> 0 Then
            ' Obtain a reference to IVsObjectManager2 type object.
            Dim objManager As IVsObjectManager2 = TryCast(GetService(GetType(SVsObjectManager)), IVsObjectManager2)
            If objManager Is Nothing Then
                Throw New NullReferenceException("GetService failed for SVsObjectManager")
            End If

            Try
                objManager.UnregisterLibrary(m_nLibraryCookie)
            Catch e As Exception
                ' Code to handle any CLS-compliant exception.
                Trace.WriteLine(e.Message)
                Throw
            Finally
                m_nLibraryCookie = 0
            End Try
        End If
    End Sub
    ```

    ```csharp
    private void UnregisterLibrary()
    {
        if (m_nLibraryCookie != 0)
        {
            // Obtain a reference to IVsObjectManager2 type object.
            IVsObjectManager2 objManager = GetService(typeof(SVsObjectManager)) as IVsObjectManager2;
            if (objManager == null)
                throw new NullReferenceException("GetService failed for SVsObjectManager");

            try
            {
                objManager.UnregisterLibrary(m_nLibraryCookie);
            }
            catch (Exception e)
            {
                // Code to handle any CLS-compliant exception.
                Trace.WriteLine(e.Message);
                throw;
            }
            finally
            {
                m_nLibraryCookie = 0;
            }
        }
    }

    ```

## <a name="see-also"></a>Ayrıca bkz.
- [Eski dil hizmeti genişletilebilirliği](../../extensibility/internals/legacy-language-service-extensibility.md)
- [Sembol tarama araçlarını destekler](../../extensibility/internals/supporting-symbol-browsing-tools.md)
- [Nasıl yapılır: Nesne yöneticisine kitaplık tarafından sağlanan sembollerin listelerini kullanıma sunma](../../extensibility/internals/how-to-expose-lists-of-symbols-provided-by-the-library-to-the-object-manager.md)