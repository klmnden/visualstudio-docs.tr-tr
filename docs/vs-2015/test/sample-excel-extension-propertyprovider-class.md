---
title: 'Örnek Excel uzantısı: PropertyProvider Sınıfı | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-test
ms.topic: conceptual
ms.assetid: 075d9b8d-8658-4fca-8711-08304dbac1c5
caps.latest.revision: 11
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: d38b430dd88eb1a732c4e4ca335a0a5bb057b1f4
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54801256"
---
# <a name="sample-excel-extension-propertyprovider-class"></a>Örnek Excel uzantısı: PropertyProvider Sınıfı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu iç sınıfını genişleten <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider> sınıf ve özellik hizmetleri sağlar [!INCLUDE[ofprexcel](../includes/ofprexcel-md.md)] ve kullanıcı arabirimi (UI) testleri kayıttan için öğeleri.  
  
## <a name="getcontrolsupportlevel-method"></a>GetControlSupportLevel yöntemi  
 <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider.GetControlSupportLevel%2A> Yöntem, özellik sağlayıcısı sağlanan denetim için sunduğu destek düzeyini gösteren bir sayı döndürür. Döndürülen değer, daha fazla özellik sağlayıcısı denetimini destekler. Bu durumda, yöntem değerini denetler <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.IUITechnologyElement.TechnologyName%2A> sağlanan denetimin özellik. Değer "Excel" ise ve <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.IUITechnologyElement.ControlTypeName%2A> olduğu gösteren bir `CellElement`, yöntem en yüksek değer döndürür; Aksi takdirde, hiçbir destek sağlandığını belirtir, sıfır döndürür.  
  
## <a name="getpropertynames-method"></a>GetPropertyNames yöntemi  
 Özellik adları ve desteklenen bir Excel hücre denetimi özelliklerinin özellik tanımlayıcılarının bir sözlüğü döndürür.  
  
## <a name="getpropertydescriptor-method"></a>GetPropertyDescriptor yöntemi  
 Bu yöntem, önceden tanımlanmış bir özellik tanımlayıcısı için belirtilen özellik adı almak için test çerçevesi tarafından çağrılır.  
  
## <a name="getpropertyvalue-and-setpropertyvalue-methods"></a>GetPropertyValue ve SetPropertyValue Yöntemleri  
 `GetPropertyValue` Yöntemi kullanan `Communicator` Excel'den özellik değeri döndürmek için bu uzantının sınıfı. `SetPropertyValue` Yöntemi kullanan <xref:Microsoft.VisualStudio.TestTools.UITesting.Keyboard> sınıfı ve `Communicator` özellik değerini ayarlamak için bileşen. Bu yöntemleri test çerçevesi tarafından çağrılır.  
  
## <a name="code-generation-customization-methods"></a>Kod üretimi özelleştirme yöntemleri  
 Bu uzantı için bu yöntem uygulanmadı. Bu nedenle, bunlar ya da dönüş `null` veya throw <xref:System.NotImplementedException>.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider>   
 <xref:Microsoft.VisualStudio.TestTools.UITesting.Keyboard>   
 [Kodlanmış Kullanıcı Arabirimi Testlerini ve Eylem Kayıtlarını Microsoft Excel'i Desteklemek için Genişletme](../test/extending-coded-ui-tests-and-action-recordings-to-support-microsoft-excel.md)
