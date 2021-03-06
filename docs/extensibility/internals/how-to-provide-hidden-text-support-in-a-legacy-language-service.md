---
title: Eski dil hizmetinde gizli metin desteği sağlama
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- hidden text, supporting
- editors [Visual Studio SDK], hidden text
- language services, implementing hidden text regions
ms.assetid: 1c1dce9f-bbe2-4fc3-a736-5f78a237f4cc
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c3d1088399256a4d5b16fa269ce022800ed645b1
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351023"
---
# <a name="how-to-provide-hidden-text-support-in-a-legacy-language-service"></a>Nasıl yapılır: Eski dil hizmetinde gizli metin desteği
Anahat bölgelerin yanı sıra gizli metin bölgeler oluşturabilirsiniz. İstemci tarafından denetlenen veya Düzenleyicisi tarafından denetlenen gizli metin bölgeleri olabilir ve metnin bir bölge tamamen gizlemek için kullanılır. Düzenleyici gizli bölge yatay çizgiler olarak görüntüler. Bunun bir örneği **yalnızca betik** HTML düzenleyicisinde görüntüle.

## <a name="to-implement-a-hidden-text-region"></a>Bir gizli metin bölgeye uygulamak için

1. Çağrı `QueryService` için <xref:Microsoft.VisualStudio.TextManager.Interop.SVsTextManager>.

     Bu bir işaretçi döndürür <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager>.

2. Çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.GetHiddenTextSession%2A>, verilen metin arabelleği için bir işaretçi olarak geçen. Bu, gizli metin oturumu zaten için arabellek var olup olmadığını belirler.

3. Zaten bir tane sonra biri ve var olan bir işaretçi oluşturun gerekmez <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> nesne döndürülür. Bu işaretçinin, listeleme ve gizli metin bölgeler oluşturmak için kullanın. Aksi takdirde, çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.CreateHiddenTextSession%2A> arabellek için gizli metin oturum oluşturmak için.

     Bir işaretçi <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> nesne döndürülür.

    > [!NOTE]
    > Çağırdığınızda `CreateHiddenTextSession`, gizli metin istemci belirtebilirsiniz (diğer bir deyişle, <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextClient>). Gizli metin istemci gizli metni veya anahat oluşturma genişletilmiş veya daraltılmış kullanıcı tarafından size bildirir.

4. Çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession.AddHiddenRegions%2A> ekleyin ya da daha yeni aşağıdakileri belirten bölgeleri teker teker anahat `reHidReg` (<xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion>) parametre:

    1. Bir değer belirleyebilirsiniz `hrtConcealed` içinde `iType` üyesi <xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion> yapısı bir anahat bölgesi yerine gizli bir bölge oluşturduğunuzu belirtmek için.

        > [!NOTE]
        > Bölgeleri altına gizlenmiş gizlendiğinde Düzenleyicisi satırları kendi varlığını göstermek için gizli bölgeler etrafında otomatik olarak görüntüler.

    2. Bölge istemci tarafından denetlenen veya Düzenleyicisi tarafından denetlenen içinde olup olmadığını belirtin `dwBehavior` üyeleri <xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion> yapısı. Akıllı ana hat oluşturma uygulamanız Düzenleyicisi ve istemci denetlenen anahat ve gizli metin bölgeleri bir karışımını içerebilir.