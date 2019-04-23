---
title: 'Nasıl yapılır: Mevcut şablonları güncelleştirme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- item templates, updating existing templates
- Visual Studio templates, updating existing templates
- project templates, updating existing templates
ms.assetid: d585e45b-7fe2-45fa-9cf3-7f2bc060f3c4
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 26482e844a4850efb1c50b15e51e4153baf1f9ab
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60076002"
---
# <a name="how-to-update-existing-templates"></a>Nasıl yapılır: Mevcut şablonları güncelleştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir şablonu oluşturun ve dosyalarını bir .zip dosyası olarak sıkıştırıp sonra şablonu değiştirmek isteyebilirsiniz. Şablon dosyaları el ile değiştirerek veya bir projeden şablonu temel alan yeni bir şablon vererek bunu yapabilirsiniz.  
  
## <a name="using-the-export-template-wizard-to-update-an-existing-template"></a>Mevcut bir şablonu güncellemek için şablonu Dışarı Aktarma Sihirbazı'nı kullanma  
 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] sağlar bir **şablonu dışarı aktar** Sihirbazı, mevcut bir şablonu güncellemek için kullanılabilir.  
  
#### <a name="to-use-export-template-to-update-an-existing-template"></a>Mevcut bir şablonu güncellemek için şablonu Dışarı Aktar'ı kullanmak için  
  
1. Üzerinde **dosya** menüsünü tıklatın **yeni** ve ardından **yeni proje**.  
  
2. Güncelleştirme, adını ve geçici projenizin konumunu girin ve tıklayın kullanmak istediğiniz şablonu seçin **Tamam**.  
  
3. Projede değiştirme [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
4. Üzerinde **dosya** menüsünde tıklatın **şablonu dışarı aktar**ve **şablonu dışarı aktar** yeni bir şablon oluşturmak için Sihirbazı.  
  
5. Güncelleştirilmiş şablonu bir .zip dosyasına sıkıştırıldıktan sonra eski şablonu .zip dosyasını silin.  
  
## <a name="manually-updating-an-existing-template"></a>Mevcut bir şablonu el ile güncelleştirme  
 Varolan bir şablonu dışında güncelleştirebilirsiniz [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] sıkıştırılmış .zip dosyasındaki dosyaları değiştirerek.  
  
#### <a name="to-manually-update-an-existing-template"></a>Mevcut bir şablonu el ile güncelleştirmek için  
  
1. Şablonu içeren .zip dosyasını bulun. Varsayılan olarak, bu dosya \My Documents\Visual Studio içinde bulunur *sürüm*\My dışarı aktarılan şablonları\\.  
  
2. .Zip dosyasını çıkartın.  
  
3. Değiştirmek ya da geçerli şablon dosyaları silin veya şablona yeni dosyalar ekleyin.  
  
4. Açma, değiştirme ve güncelleştirilmiş davranışı işlemek için .vstemplate XML dosyasına veya yeni dosyaları kaydedin. .Vstemplate şeması hakkında daha fazla bilgi için bkz. [Visual Studio şablon şeması başvurusu](../extensibility/visual-studio-template-schema-reference.md). Kaynak dosyalarında parametreleştirebilirsiniz hakkında daha fazla bilgi için bkz. [şablon parametreleri](../ide/template-parameters.md)  
  
5. Dosyaları, şablonunuzda sağ tıklayın, Select **göndermek için**ve ardından **sıkıştırılmış (daraltılmış) klasör**. Seçtiğiniz dosyaların bir .zip dosyasına sıkıştırılır.  
  
6. Eski bir .zip dosyası olarak aynı dizinde yeni bir .zip dosyası yerleştirin.  
  
7. Ayıklanan şablon dosyalarını ve eski şablonu .zip dosyasını silin.  
  
8. (Yönetici olarak) bir örneği, geliştirici komut istemi başlatın (Başlat menüsündeki altında **Visual Studio 2010 / Visual Studio Araçları/Geliştirici komut istemi**).  
  
9. Aşağıdaki komutu çalıştırın: `devenv /installvstemplates`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Şablonları özelleştirme](../ide/customizing-project-and-item-templates.md)   
 [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)   
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)   
 [Şablon parametreleri](../ide/template-parameters.md)   
 [Nasıl yapılır: Başlangıç Paketleri Oluşturma](../ide/how-to-create-starter-kits.md)
