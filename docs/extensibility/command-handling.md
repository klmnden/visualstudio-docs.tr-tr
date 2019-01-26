---
title: Komut işleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - command handling
ms.assetid: 78f67d92-77f7-45cb-ad75-6e3346379cc3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f3f9086bba7d5c5adfa42f1297de07a2f50ff7e6
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54988135"
---
# <a name="command-handling"></a>Komut işleme
Düzenleyici yeni komutları tanımlayabilirsiniz. Komutları genellikle bir araç çubuğunda veya bağlam menüsündeki bir menü görüntülenir.  
  
 Komutlar ve menüler tanımlama hakkında daha fazla bilgi için bkz. [komutlar, menüler ve araç çubukları](../extensibility/internals/commands-menus-and-toolbars.md).  
  
 Dil hizmeti uğratarak Düzenleyici'de gösterilen hangi bağlam menüleri denetleyebilirsiniz <xref:Microsoft.VisualStudio.VSConstants.VSStd2KCmdID> sabit listesi. Alternatif olarak, bağlam menüsünü işaret başına temelinde denetleyebilirsiniz. Daha fazla bilgi için [dil hizmeti filtreleri için önemli komutlar](../extensibility/internals/important-commands-for-language-service-filters.md).  
  
## <a name="add-commands-to-the-editor-context-menu"></a>Düzenleyici bağlam menüsüne komut ekleme  
 Bağlam menüsüne komut ekleme, menü komutları belirli bir gruba ait olan bir dizi tanımlamanız gerekir. Aşağıdaki örnek runbook'undan *.vsct* adım adım kılavuzun bir parçası olarak oluşturulan dosya [izlenecek yol: Özellikler eklemek için özel bir düzenleyici](../extensibility/walkthrough-adding-features-to-a-custom-editor.md):  
  
 \<Menü GUID "guidCustomEditorCmdSet" id = "IDMX_RTF" priority = "0x0000" type = "Context" >  
  
 \<Üst GUID "guidCustomEditorCmdSet" id = "0" / >  
  
 \<Dizeleri >  
  
 \<ButtonText > CustomEditor bağlam menüsü\</ButtonText >  
  
 \<CommandName>CustomEditorContextMenu\</CommandName>  
  
 \</ Dizeleri >  
  
 \</ Menüsü >  
  
 \</ Menülerine >  
  
 Bir bağlam menüsü komutu metinle yukarıdaki metin ekler **CustomEditor bağlam menüsü**. Menü GUID, bu Düzenleyicisi ile oluşturulmuş komut kümesi bir parçasıdır. "Bağlam" türüdür.  
  
 Ayrıca tanımlanması gerekmez önceden tanımlanmış komutları kullanabilirsiniz *.vsct* dosya. Örneğin, inceleyin *EditorPane.cs* Visual Studio Paket şablon tarafından oluşturulan dosya. Bir dizi önceden tanımlanmış komutları gibi bulabilirsiniz <xref:Microsoft.VisualStudio.VSConstants.VSStd97CmdID> tarafından tanımlanan <xref:Microsoft.VisualStudio.VSConstants.GUID_VSStandardCommandSet97>, komut işleyicileri gibi işlenir `onSelectAll` yöntemi.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Komutlar, menüler ve araç çubukları](../extensibility/internals/commands-menus-and-toolbars.md)