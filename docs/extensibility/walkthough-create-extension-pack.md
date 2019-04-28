---
title: Uzantı paketi öğesi şablonuyla uzantı paketi oluştur | Microsoft Docs
ms.date: 07/27/2018
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], new - extensions
ms.assetid: 5388EEBA-211D-4114-8CD9-70C899919F7E
author: gregvanl
ms.author: gregvanl
manager: Meng
ms.workload:
- vssdk
ms.openlocfilehash: 7899a096bb2a56e93ea55a4ba0a17cde272bd615
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62950968"
---
# <a name="walkthrough-create-an-extension-pack"></a>İzlenecek yol: Uzantı Paketi Oluşturma

Birlikte yüklenebilir uzantıları kümesi bir uzantı paketidir. Uzantı paketleri kolayca sık kullandığınız uzantıların diğer kullanıcılarla paylaşmak ya da belirli bir senaryo için bir arada uzantıları kümesini paket olanak sağlar.

## <a name="prerequisites"></a>Önkoşullar

Visual Studio 2015'ten başlayarak, Visual Studio SDK'sı Visual Studio kurulumunda isteğe bağlı bir özellik olarak dahil edilir. VS SDK'yi daha sonra yükleyebilirsiniz. Daha fazla bilgi için [Visual Studio SDK'sını yükleme](../extensibility/installing-the-visual-studio-sdk.md).

Uzantı paketi bu özellik, Visual Studio 15,8 önizleme 2'den itibaren kullanılabilir.

## <a name="create-an-extension-with-an-extension-pack-item-template"></a>Uzantı paketi öğesi şablonuyla uzantı oluşturma

Uzantı paketi öğe şablonu, bir uzantı paketi ile birlikte yüklenen uzantı kümesi oluşturur.

1. İçinde **yeni proje** iletişim kutusunda, "VSIX" ve seçin için arama **VSIX projesi**. İçin **proje adı**, "Test uzantı paketi" yazın. **Oluştur**’u seçin.

2. İçinde **Çözüm Gezgini**, proje düğümüne sağ tıklayıp **Ekle** > **yeni öğe**. Git için Visual C# **genişletilebilirlik** düğümünü seçip alt **uzantı paketi**. Varsayılan dosya adı (ExtensionPack1.cs) bırakın.

3. Aşağıdaki kodu içeren ExtensionPack1.vsext dosya eklendiğinde

   ```json
   {
    "id": "ExtensionPack1",
    "name": "ExtensionPack1",
    "description": "Read about creating extension packs at https://aka.ms/vsextpack",
    "version": "1.0.0.0",
    "extensions": [  // List of extensions that are included in the Extension Pack.
      {
        "vsixId": "41858b2d-ff0b-4a43-80b0-f1b2d6084935", // The vsix id of the extension you want to   include.
        "name": "AlignAssignments"
      },
      {
          "vsixId": "42374550-426a-400e-96f9-237682e8dea6",
        "name": "CopyAsHtml"
      }
    ]
   }
   ```

4. Uzantının uzantısı paketinde içerecek şekilde vsixıd bulunabilir [Visual Studio Market](https://marketplace.visualstudio.com/). Uzantısına tıklayın ve eklemek istediğiniz bulma **kopya Kimliğini**. Var olan güncelleştirme **Vsixıd** yukarıdaki içinde dosya veya başka bir uzantı listeye ekleyin.

    ![Market'ten Vsixıd kopyalayın](media/vsixid-marketplace.png)

5. Projeyi oluşturmak ve Market'te uzantınızı yükleyin. Bkz: [Visual Studio uzantısı yayımlama](../extensibility/walkthrough-publishing-a-visual-studio-extension.md).

> [!NOTE]
> Uzantı paketi, kullanılabilir uzantıları yalnızca yükleyebilirsiniz [Visual Studio Market](https://marketplace.visualstudio.com/) veya [özel galeri](../extensibility/how-to-create-an-atom-feed-for-a-private-gallery.md).

## <a name="install-the-extension-pack-from-the-visual-studio-marketplace"></a>Visual Studio Market'ten uzantı paketini yükle

Uzantı yayımlandıktan sonra Visual Studio'da yükleyin ve test etmek.

::: moniker range="vs-2017"

1. Visual Studio'da üzerinde **Araçları** menüsünü tıklatın **Uzantılar ve güncelleştirmeler**.

::: moniker-end

::: moniker range=">=vs-2019"

1. Visual Studio'da üzerinde **uzantıları** menüsünde tıklatın **Yönetilen Uzantılar**.

::: moniker-end

2. Tıklayın **çevrimiçi** ve ardından "Test uzantı paketi" arayın.

3. **İndir**'e tıklayın. Uzantı ve kendi uzantısı paketinde uzantılarının listesi için yükleme zamanlanacak.

4. Bir örnek uzantısı paketi yükleme görünümünü aşağıdadır **uzantıları yönetme** iletişim. Dahil edilen uzantılar yalnızca bazıları uzantısı paketinde yüklemeyi tercih ediyorsanız, uzantı listesinde değiştirebilirsiniz **için zamanlanmış yükleme**.

    ![Market'ten uzantı paketi indirin](media/vside-extensionpack.png)

5. Yüklemeyi tamamlamak için Visual Studio'nun tüm örneklerini kapatın.

## <a name="remove-the-extension"></a>Uzantıyı kaldırın

Uzantıyı bilgisayarınızdan kaldırmak için:

::: moniker range="vs-2017"

1. Visual Studio'da üzerinde **Araçları** menüsünü tıklatın **Uzantılar ve güncelleştirmeler**.

::: moniker-end

::: moniker range=">=vs-2019"

1. Visual Studio'da üzerinde **uzantıları** menüsünde tıklatın **Yönetilen Uzantılar**.

::: moniker-end

2. Seçin **Test uzantı paketi** ve ardından **kaldırma**. Uzantı ve uzantısı paketinde uzantıları listesini kaldırma işlemi için zamanlanacak.

3. Kaldırma işlemini tamamlamak için Visual Studio'nun tüm örneklerini kapatın.
