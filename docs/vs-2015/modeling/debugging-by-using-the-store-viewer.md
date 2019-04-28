---
title: Store görüntüleyiciyi kullanarak hata ayıklama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, store viewer
- Domain-Specific Language, store
ms.assetid: 0178db2e-ae99-4ed3-9b87-8620fa9fa8e4
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 1a76cd9b726e534271937cb67a8d3f946d4eb477
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63433191"
---
# <a name="debugging-by-using-the-store-viewer"></a>Depo Görüntüleyiciyi Kullanarak Hata Ayıklama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Store Görüntüleyici ile durumunu inceleyebilirsiniz bir *depolamak* tarafından kullanılan [!INCLUDE[dsl](../includes/dsl-md.md)]. Store Görüntüleyici öğesi özellikleri ve öğeleri arasında bağlantılar ile birlikte, belirli bir depolama alanında bulunan tüm etki alanı model öğeleri görüntüler.  
  
## <a name="opening-store-viewer"></a>Açılış Store Görüntüleyicisi  
 Uygulamasındayken [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Deneysel burada depolama örneği model bilgileri içeren kodunuz bir kesme noktasında durdurmak, oluşturun. Ardından, aşağıdaki komutu yazarak Store Görüntüleyicisi'ni açın **hemen** penceresi:  
  
```  
Microsoft.VisualStudio.Modeling.Diagnostics.StoreViewer.Show(mystore);  
```  
  
> [!NOTE]
> Değiştirmeniz gereken `mystore` deposu örneğinizin adı. Ayrıca, ad alanı kodunuza ekleyin, tam nitelikli ad Store Görüntüleyicisi'ni görüntülemek için komutu yazabilirsiniz:  
>   
> `using Microsoft.VisualStudio.Modeling.Diagnostics;`  
>   
> `…`  
>   
> `StoreViewer.Show(mystore);`  
  
 `Show` Yöntemi olan çeşitli aşırı yükler. Bir mağaza veya bir bölümleme örneği parametre olarak belirtebilirsiniz.  
  
 Alternatif olarak, Store Görüntüleyicisi kodunuzdaki herhangi bir yere görüntüler kod satırının koyabilirsiniz burada geçirdiğiniz parametre `Show` kapsamda bir yöntemdir. Bu eylem, kod satırının bir anlık görüntüsünü deposunun içeriğini yürütüldüğünde Store Görüntüleyicisi'ni görüntüler.  
  
### <a name="using-store-viewer"></a>Store Görüntüleyicisi'ni kullanma  
 Store Görüntüleyicisi oturum açtığında, engelleyici olmayan bir Windows Forms pencere, aşağıdaki çizimde gösterildiği gibi görünür.  
  
 ![](../modeling/media/storeviewer2.png "storeviewer2")  
Store Görüntüleyicisi  
  
 Store Görüntüleyicisi üç bölme vardır: sol bölmesinde, sağ üst bölmesi ve sağ alt bölmesi. Sol bölmede türlerini ağaç görünümünde olduğunu `DomainDataDirectory` mağaza üyesi. Ve bölüm düğümünü genişletin ve bir öğeyi tıklatın, öğenin özellikler sağ üst bölmede görünür. Öğenin diğer öğelere bağlı ise, ek öğeler sağ alt bölmede görünür. Öğesi, öğenin sağ alt bölmede çift tıklarsanız, sol bölmede vurgulanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Program Kodunda Modeli Gezinme ve Güncelleştirme](../modeling/navigating-and-updating-a-model-in-program-code.md)
