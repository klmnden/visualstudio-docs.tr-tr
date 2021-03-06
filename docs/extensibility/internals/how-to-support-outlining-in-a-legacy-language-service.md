---
title: 'Nasıl yapılır: Eski dil hizmetinde ana hat oluşturma desteği | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], collapse to definitions command
- language services, supporting Collapse to Definitions command
- hidden text, Collapse to Definitions command
ms.assetid: bb6e74c3-93e4-4ef7-afc7-1c9b342f083b
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6f79f98ede5c28f8e3acb682ebe8f23e4dc4f72e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66312045"
---
# <a name="how-to-support-outlining-in-a-legacy-language-service"></a>Nasıl yapılır: Eski dil hizmetinde ana hat oluşturma desteği
Anahat oluşturma, genişletme veya daraltma farklı bölgelerdeki metin için kullanılır. Anahat oluşturma şekilde kullanılan tarafından farklı dillerde farklı şekilde tanımlanabilir. Daha fazla bilgi için [anahat](../../ide/outlining.md).

 Eski dil Hizmetleri bir VSPackage'ı bir parçası olarak uygulanır, ancak dil hizmeti özellikleri uygulamak için daha yeni MEF uzantıları kullanmaktır. Anahat oluşturma uygulamak için en yeni yolu hakkında daha fazla bilgi için bkz: [izlenecek yol: Anahat oluşturma](../../extensibility/walkthrough-outlining.md).

> [!NOTE]
> Yeni bir düzenleyici API hemen kullanmaya başlamak öneririz. Bu dil hizmetinizin performansını ve yeni düzenleyici özellikleri yararlanmanıza olanak tanır.

 Bu komut, language service Pro desteklemek nasıl gösterir.

## <a name="to-support-outlining"></a>Ana hat oluşturmayı desteklemek için

1. Uygulama <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningCapableLanguage> dil hizmeti nesneniz üzerinde.

2. Çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession.AddOutlineRegions%2A> yeni anahat bölge ekleme için anahat oluşturma geçerli oturum nesnesi üzerinde.

## <a name="robust-programming"></a>Güçlü programlama
 Bir kullanıcı seçtiğinde **Daralt tanımları** üzerinde **anahat** menüsü, IDE çağrıları <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningCapableLanguage.CollapseToDefinitions%2A> dil hizmetinizde.

 Bu yöntem çağrıldığında, IDE içinde geçen bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines> işaretçi (işaretçiye bir metin arabelleği için) ve bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession> (geçerli anahat oluşturma oturumu için bir işaretçi).

 Çağırabilirsiniz <xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession.AddOutlineRegions%2A> yöntemi bu bölgelerde belirterek, birden çok ana hat bölgeler için `rgOutlnReg` parametresi. `rgOutlnReg` Parametresi bir <xref:Microsoft.VisualStudio.TextManager.Interop.NewOutlineRegion> yapısı. Bu işlem belirli bir bölge genişletilmiş veya daraltılmış gibi gizli bölge farklı özelliklerini belirtmenize olanak sağlar.

> [!NOTE]
> Yeni satır karakterleri gizleme hakkında dikkatli olun. Gizli metin ilk satırını başından son karakter bir bölümdeki son satırın son yeni satır karakteri görünür bırakmak genişletmelidir.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Eski dil hizmetinde gizli metin desteği](../../extensibility/internals/how-to-provide-hidden-text-support-in-a-legacy-language-service.md)
- [Nasıl yapılır: Eski dil hizmetinde genişletilmiş ana hat oluşturma desteği sağlar](../../extensibility/internals/how-to-provide-expanded-outlining-support-in-a-legacy-language-service.md)