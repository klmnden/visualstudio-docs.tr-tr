---
title: 'Nasıl Yapılır: SharePoint dağıtım komutlarını ayarlama | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, deploying
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 98aedc0c7fa557a45b43ab8344a49587b8febec1
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53920371"
---
# <a name="how-to-set-sharepoint-deployment-commands"></a>Nasıl Yapılır: SharePoint dağıtım komutlarını ayarlama
  Dağıtım öncesi ve dağıtım sonrası komutları ayarlayarak, dağıtım işlemi özelleştirebilirsiniz. SharePoint çözümleri Visual Studio'dan hata ayıklaması yaparken önce ve sonra diğer dağıtım eylemleri şu komutları çalıştırın.  
  
### <a name="to-add-a-pre-deployment-command"></a>Dağıtım öncesi komut ekleme  
  
1.  Menü çubuğunda, **proje** > **\<*ProjectName*> Özellikleri**.  
  
2.  Seçin **SharePoint** sekmesi.  
  
3.  İçinde **dağıtım öncesi komut satırını** metin kutusunda, bu adımı özelleştirmek için MS-DOS veya MSBuild komut girin.  
  
     Örneğin, dağıtım tamamlanmadan önce dizin içeriğini listelemek için girin **dir**.  
  
### <a name="to-add-a-post-deployment-command"></a>Dağıtım sonrası komut ekleme  
  
1.  Menü çubuğunda, **proje** > **\<*ProjectName*> Özellikleri**.  
  
2.  Seçin **SharePoint** sekmesi.  
  
3.  İçinde **dağıtım sonrası komut satırı** metin kutusunda, bu adımı özelleştirmek için MS-DOS veya MSBuild komut girin.  
  
     Örneğin, dağıtım tamamlandıktan sonra dizin içeriğini listelemek için girin **dir**. Derleme derleme dizininden kopyalamak için bir MSBuild değişken kullanmak için girin **$(TargetPath) c:\DeploymentDirectory kopyalama**.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)  
