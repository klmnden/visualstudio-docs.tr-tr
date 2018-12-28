---
title: Özel belge özelliklerine genel bakış
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], custom properties
- custom document properties
- document-level customizations [Office development in Visual Studio], custom properties
- Office documents [Office development in Visual Studio], custom properties
- _AssemblyLocation property
- _AssemblyName property
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 9fcd250f75e21d24409bb7b17764d9d18e7d6c7b
ms.sourcegitcommit: a715de2ba8c703f37aa2102567b1aa2c0f05a117
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/15/2018
ms.locfileid: "53441450"
---
# <a name="custom-document-properties-overview"></a>Özel belge özelliklerine genel bakış

Belge düzeyi projesi oluşturduğunuzda, Visual Studio projedeki belge iki özel özellikler ekler: \_AssemblyLocation ve \_AssemblyName. Bir kullanıcı bir belgeyi açtığında, Microsoft Office uygulamasının bu özel belge özelliklerini denetler. Belgede varsa, uygulamayı yükleyen [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)], özelleştirme başlatır. Daha fazla bilgi için [mimarisi Office çözümlerini Visual Studio'da](../vsto/architecture-of-office-solutions-in-visual-studio.md).

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

## <a name="assemblyname"></a>\_AssemblyName

Bu özellik bir arabirim, Office çözüm yükleyicisi bileşeninin CLSID içeren [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]. CLSID 4E3C66D5 58-D 4-491E-A7D4-64AF99AF6E8B değerdir. Hiçbir zaman bu değeri değiştirmeniz gerekir.

## <a name="assemblylocation"></a>\_AssemblyLocation

Bu özellik, özelleştirme için dağıtım bildirimi hakkında daha fazla ayrıntı sağlayan bir dize içerir. Bildirimleri hakkında daha fazla bilgi için bkz. [uygulama ve dağıtım bildirimlerini Office çözümlerinde](../vsto/application-and-deployment-manifests-in-office-solutions.md).

 The_AssemblyLocation özellik değeri, çözümün nasıl dağıtıldığına bağlı olarak farklı biçimlerde olabilir:

- Çözüm, bir Web sitesi, UNC yolu ya da bir CD veya USB sürücüsüne yüklenecek yayımladıysanız _AssemblyLocation özelliğini biçimdedir *DeploymentManifestPath*|*SolutionID*. Aşağıdaki dize örneği şöyledir:

     File://deployserver/MyShare/ExcelWorkbook1.vsto | 74744e4b-e4d6-41eb-84f7-ad20346fe2d9 & lt

- Çalışan veya Visual Studio çözümünden hata ayıklama, _AssemblyLocation özelliğini biçimdedir *DeploymentManifestName*|*SolutionID*| vstolocal. Aşağıdaki dize örneği şöyledir:

     ExcelWorkbook1.vsto|74744e4b-e4d6-41eb-84f7-ad20346fe2d9 & lt | vstolocal

  *SolutionID* bir GUID, [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] çözümü belirlemek için kullanır. *SolutionID* projeyi oluşturduğunuzda otomatik olarak oluşturulur. **Vstolocal** terimi gösterir [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] derlemenin belgeyle aynı klasörde bulunan yüklenmesi.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da Office çözümleri mimarisi](../vsto/architecture-of-office-solutions-in-visual-studio.md)
- [Belge düzeyi özelleştirmeler mimarisi](../vsto/architecture-of-document-level-customizations.md)
- [Office çözümlerinde uygulama ve dağıtım bildirimleri](../vsto/application-and-deployment-manifests-in-office-solutions.md)
- [Nasıl yapılır: ClickOnce kullanarak Office çözümü yayımlama](https://msdn.microsoft.com/2b6c247e-bc04-4ce4-bb64-c4e79bb3d5b8)
- [Nasıl yapılır: Özel belge özelliklerini oluşturma ve değiştirme](../vsto/how-to-create-and-modify-custom-document-properties.md)
