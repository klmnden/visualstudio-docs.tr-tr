---
title: Komut işleme | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - command handling
ms.assetid: 78f67d92-77f7-45cb-ad75-6e3346379cc3
caps.latest.revision: 21
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: de4bf6ace6860cbd6155fe67a0de824e5626cfe3
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49257224"
---
# <a name="command-handling"></a>Komut işleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Düzenleyici yeni komutları tanımlayabilirsiniz. Komutları genellikle bir araç çubuğunda veya bağlam menüsündeki bir menü görüntülenir.  
  
 Komutlar ve menüler tanımlama hakkında daha fazla bilgi için bkz. [komutlar, menüler ve araç çubukları](../extensibility/internals/commands-menus-and-toolbars.md).  
  
 Dil hizmeti uğratarak Düzenleyici'de gösterilen hangi bağlam menüleri denetleyebilirsiniz <xref:Microsoft.VisualStudio.VSConstants.VSStd2KCmdID> sabit listesi. Alternatif olarak, bağlam menüsünü işaret başına temelinde denetleyebilirsiniz. Daha fazla bilgi için [dil hizmeti filtreleri için önemli komutlar](../extensibility/internals/important-commands-for-language-service-filters.md).  
  
## <a name="adding-commands-to-the-editor-context-menu"></a>Düzenleyici bağlam menüsüne komut ekleme  
 Bağlam menüsüne komut ekleme, menü komutları belirli bir gruba ait olan bir dizi tanımlamanız gerekir. Aşağıdaki örnek, adım adım kılavuzun bir parçası olarak oluşturulan .vsct dosyası alındığı [izlenecek yol: bir özel düzenleyiciye özellik ekleme](../extensibility/walkthrough-adding-features-to-a-custom-editor.md):  
  
 \<Menü GUID "guidCustomEditorCmdSet" id = "IDMX_RTF" priority = "0x0000" type = "Context" >  
  
 \<Üst GUID "guidCustomEditorCmdSet" id = "0" / >  
  
 \<Dizeleri >  
  
 \<ButtonText > CustomEditor bağlam menüsü\</ButtonText >  
  
 \<CommandName > CustomEditorContextMenu\</CommandName >  
  
 \</ Dizeleri >  
  
 \</ Menüsü >  
  
 \</ Menülerine >  
  
 Bir bağlam menüsü komutu metinle yukarıdaki metin ekler **CustomEditor bağlam menüsü**. Menü komut kümesi bu düzenleyici ile oluşturulur ve "İçerik" türüdür GUID'dir.  
  
 .Vsct dosyası içinde tanımlanması gerekmez önceden tanımlanmış komutları da kullanabilirsiniz. Visual Studio Paket şablon tarafından oluşturulan EditorPane.cs dosyası incelerseniz, örneğin, bir dizi önceden tanımlanmış komut gibi bulduğunuz <xref:Microsoft.VisualStudio.VSConstants.VSStd97CmdID> tarafından tanımlanan <xref:Microsoft.VisualStudio.VSConstants.GUID_VSStandardCommandSet97>, komut işleyicileri onSelectAll yöntemi gibi işlenir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Komutlar, Menüler ve Araç Çubukları](../extensibility/internals/commands-menus-and-toolbars.md)

