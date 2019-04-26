---
title: Araç penceresi içeren bir uzantı oluşturma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
ms.assetid: 585b0a3a-f85b-4f92-81bb-9ca499bb8a89
caps.latest.revision: 6
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 94c8335b8d723ef20c04cfffe6b3788d71ecaa4f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62431855"
---
# <a name="creating-an-extension-with-a-tool-window"></a>Araç Penceresi İçeren Bir Uzantı Oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu yordamda, VSIX proje şablonu kullanmayı öğrenin ve **özel araç penceresi** öğe şablonu, araç penceresi içeren bir uzantı oluşturma.  
  
## <a name="prerequisites"></a>Önkoşullar  
 Visual Studio 2015'ten başlayarak, size Visual Studio SDK İndirme Merkezi'nden yüklemeyin. Visual Studio kurulumunda isteğe bağlı bir özellik olarak eklenmiştir. VS SDK'yi daha sonra yükleyebilirsiniz. Daha fazla bilgi için [Visual Studio SDK'sını yükleme](../extensibility/installing-the-visual-studio-sdk.md).  
  
### <a name="creating-a-tool-window"></a>Araç penceresi oluşturma  
  
1. Adlı bir VSIX projesi oluşturun **FirstWindow**. VSIX proje şablonunda bulabilirsiniz **yeni proje** iletişim altında **Visual C# / genişletilebilirlik**.  
  
2. Projeyi açtığında, adlı bir araç penceresi öğesi şablonu ekleme **FirstWindow**. İçinde **Çözüm Gezgini**, proje düğümüne sağ tıklayıp **Ekle / yeni öğe**. İçinde **Yeni Öğe Ekle** iletişim kutusunda, Git **Visual C# / genişletilebilirlik** seçip **özel araç penceresi**. İçinde **adı** alan penceresinin en altında bir araç penceresi dosya adını değiştirerek **FirstWindow.cs**.  
  
3. Projeyi oluşturmak ve hata ayıklamaya başlayın.  
  
     Visual Studio'nun deneysel örneğinde görünür. Deneysel örnek hakkında daha fazla bilgi için bkz. [deneysel örneğinde](../extensibility/the-experimental-instance.md).  
  
4. Deneysel örneğinde Git **görünüm / diğer Windows**.  
  
     Bir menü öğesi için görmelisiniz **FirstWindow**. Tıklayın.  
  
     Başlığa sahip araç penceresi görmeniz gerekir **FirstWindow** ve bir düğmeyi bildiren **Me tıklayın!**
