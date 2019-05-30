---
title: Araç penceresi içeren bir uzantı oluşturma | Microsoft Docs
ms.date: 3/16/2019
ms.topic: conceptual
ms.assetid: 585b0a3a-f85b-4f92-81bb-9ca499bb8a89
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b5a38c9912be87c94c79076675b5db25663fb5f0
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345441"
---
# <a name="create-an-extension-with-a-tool-window"></a>Araç penceresi içeren bir uzantı oluşturma

Bu yordamda, VSIX proje şablonu kullanmayı öğrenin ve **özel araç penceresi** öğe şablonu, araç penceresi içeren bir uzantı oluşturma.

## <a name="prerequisites"></a>Önkoşullar

 Visual Studio 2015'ten başlayarak, size Visual Studio SDK İndirme Merkezi'nden yüklemeyin. Visual Studio kurulumunda isteğe bağlı bir özellik olarak eklenmiştir. VS SDK'yi daha sonra yükleyebilirsiniz. Daha fazla bilgi için [Visual Studio SDK'yı yükleme](../extensibility/installing-the-visual-studio-sdk.md).

### <a name="create-a-tool-window"></a>Araç penceresi oluşturma

1. Adlı bir VSIX projesi oluşturun **FirstWindow**. VSIX proje şablonunda bulabilirsiniz **yeni proje** iletişim "VSIX" için arama yapın.

2. Projeyi açtığında, adlı bir araç penceresi öğesi şablonu ekleme **MyWindow**. İçinde **Çözüm Gezgini**, proje düğümüne sağ tıklayıp **Ekle** > **yeni öğe**. İçinde **Yeni Öğe Ekle** iletişim kutusunda, Git **Visual C#**  > **genişletilebilirlik** seçip **özel araç penceresi**. İçinde **adı** alan penceresinin en altında bir araç penceresi dosya adını değiştirerek *MyWindow.cs*.

3. Projeyi oluşturmak ve hata ayıklamaya başlayın.

   Visual Studio'nun deneysel örneğinde görünür. Deneysel örnek hakkında daha fazla bilgi için bkz. [deneysel örneğinde](../extensibility/the-experimental-instance.md).

4. Deneysel örneğinde Git **görünümü** > **diğer Windows**.

   Bir menü öğesi için görmelisiniz **MyWindow**. Tıklayın.

   Başlığa sahip araç penceresi görmeniz gerekir **MyWindow** ve bir düğmeyi bildiren **Me tıklayın!**