---
title: 'Nasıl yapılır: SharePoint dağıtım komutlarını ayarlama | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, deploying
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 79843389adcd7dc0a4e350e4fd010d450c837a4e
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56606699"
---
# <a name="how-to-set-sharepoint-deployment-commands"></a>Nasıl yapılır: SharePoint dağıtım komutlarını ayarlama
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
- [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)
