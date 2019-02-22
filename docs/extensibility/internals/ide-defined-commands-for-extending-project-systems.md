---
title: Proje sistemlerini genişletmeye yönelik IDE tanımlı komutlar | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- commands, project systems
- project systems, environment-defined commands
ms.assetid: 0e33b8e9-16fa-4400-a941-e92d56120e7e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 26f5ee29a52546e7f2111189f54d64c160a94cea
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56646922"
---
# <a name="ide-defined-commands-for-extending-project-systems"></a>Proje Sistemlerini Genişletmeye Yönelik IDE Tanımlı Komutlar
Proje sistemleri genişletmek istediğinizde, komutları ve komut grupları tarafından sağlanan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE.

 Aşağıdaki bölümlerde proje sistemleri genişletmek için kullanışlı olan komut öğeleri listelenir.

## <a name="command-menus"></a>Komut menüleri
 Aşağıdaki tablo, bir proje genişletici çağırma üst düzey komutların koymak için yararlı konumlar komut menüleri gösterir.

|Komutu menüsü|Açıklama|
|------------------|-----------------|
|IDM_VS_MENU_PROJECT|**Proje** üst düzey menü.|
|IDM_VS_TOOL_PROJWIN|**Çözüm Gezgini** araç çubuğu.|

## <a name="shortcut-menus"></a>Kısayol menüleri
 Aşağıdaki tabloda, tek bir düğüm olarak seçildiğinde uygulayan kısayol menülerini gösterilmektedir **Çözüm Gezgini**, veya birden çok homojen seçimleri olduğunda **Çözüm Gezgini**, ne zaman olduğu Tüm seçili düğümleri aynı türüdür.

|Kısayol menüsü|Açıklama|
|-------------------|-----------------|
|<xref:Microsoft.VisualStudio.Shell.VsMenus.IDM_VS_CTXT_PROJNODE>|Proje düğümü seçildiğinde uygulanır.|
|<xref:Microsoft.VisualStudio.Shell.VsMenus.IDM_VS_CTXT_ITEMNODE>|Bir dosya seçili durumdayken geçerlidir.|
|<xref:Microsoft.VisualStudio.Shell.VsMenus.IDM_VS_CTXT_FOLDERNODE>|Bir klasörü seçildiğinde uygulanır.|
|IDM_VS_CTXT_WEBREFFOLDER|Web başvuru klasörü seçildiğinde uygulanır.|
|<xref:Microsoft.VisualStudio.Shell.VsMenus.IDM_VS_CTXT_REFERENCEROOT>|"Başvuru" adlı başvuruları kök düğümü seçildiğinde uygulanır.|
|<xref:Microsoft.VisualStudio.Shell.VsMenus.IDM_VS_CTXT_REFERENCE>|Başvuru düğümleri seçili olduğunda geçerlidir; Bunlar, derleme, COM ve yalnızca proje başvurularını içerir. Web başvuruları içermez.|

 Aşağıdaki tabloda, ne zaman uygulamak kısayol menüleri gösterilmektedir seçiminde **Çözüm Gezgini** yayılan birden çok hiyerarşi

|Kısayol menüsü|Açıklama|
|-------------------|-----------------|
|IDM_VS_CTXT_XPROJ_SLNPROJ|Çözüm düğümü ve kök proje düğümleri geçerli seçime içerdiğinde, geçerlidir.|
|IDM_VS_CTXT_XPROJ_SLNITEM|Geçerli seçimi çözüm düğümü ve proje öğeleri içeren uygulanır.|
|IDM_VS_CTXT_XPROJ_MULTIPROJ|Geçerli seçimi birden çok kök proje düğümden yalnızca oluşur uygulanır.|
|IDM_VS_CTXT_XPROJ_PROJITEM|Geçerli seçimi kök proje düğümleri ve proje öğeleri bir karışımını içeren uygulanır. Ayrıca, seçim çözüm düğümüne içerebilir.|
|IDM_VS_CTXT_XPROJ_MULTIITEM|Geçerli seçimi proje öğelerinden bir çözümde birden çok proje içeriyorsa ya da farklı türdeki öğeleri aynı proje içinde seçili olduğunda geçerlidir.|

## <a name="command-groups"></a>Komut grupları
 Projeleri genişletme ve aracılığıyla erişebileceğiniz kullanabileceğiniz komut gruplarını aşağıdaki tabloda gösterilmektedir <xref:Microsoft.VisualStudio.Shell.VsMenus.IDM_VS_CTXT_PROJNODE> kısayol menüsü.

|Komut grubu|Açıklama|
|-------------------|-----------------|
|IDG_VS_CTXT_PROJECT_BUILD|Derleme, yeniden oluşturma ve projeyi dağıtma komutları.|
|IDG_VS_CTXT_COMPILELINK|Derleme ve bağlama projesi komutlar içerir.|
|IDG_VS_CTXT_PROJECT_CONFIG|Proje yapılandırması ayarlayın ve derleme sırası komutları.|
|IDG_VS_CTXT_PROJECT_ADD|Proje öğeleri Ekle komutları.|
|IDG_VS_CTXT_PROJECT_START|F5 tuşuna ile ilişkili başlangıç projesi ayarlama komutları.|
|IDG_VS_CTXT_PROJECT_SAVE|Proje öğeleri kaydedilirken komutlar içerir.|
|IDG_VS_CTXT_PROJECT_DEBUG|Hata ayıklama komutlar içerir.|
|IDG_VS_CTXT_PROJECT_SCC|Kaynak denetimi için komutları.|
|IDG_VS_CTXT_PROJECT_TRANSFER|Komutları için kesme, kopyalama ve yapıştırma işlemleri.|
|IDG_VS_CTXT_PROJECT_PROPERTIES|Erişim sağlayan komutlar **proje özellikleri** iletişim kutusu.|

## <a name="see-also"></a>Ayrıca Bkz.
- [VSPackage’ların Kullanıcı Arabirimi Öğeleri Eklemesi](../../extensibility/internals/how-vspackages-add-user-interface-elements.md)
- [MenuCommands Vs. OleMenuCommands](../../extensibility/menucommands-vs-olemenucommands.md)
- [Yeniden Kullanılabilir Düğme Grupları Oluşturma](../../extensibility/creating-reusable-groups-of-buttons.md)