---
title: Kaynak Denetimi çalışma zamanı ayrıntıları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control [Visual Studio SDK], runtime details
ms.assetid: 1acd30e0-f98c-4bde-b9cd-4076845887df
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3f7501a25596fc0a818277d164337bb0d4e4e077
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56618802"
---
# <a name="source-control-runtime-details"></a>Kaynak Denetimi Çalışma Zamanı Ayrıntıları
Kullanıcı bir dosya projede kaynak denetimi için veya bir sihirbaz gibi Otomasyon denetleyicisi aracılığıyla eklediğinde projesi kaynak denetimine eklenir. Bir proje kendisi için kaynak denetimi altında olduğunu belirtmez; Kaynak denetimi destekler, ancak kendisine el ile eklenmesi gerekir.

## <a name="registering-with-a-source-control-package"></a>Bir kaynak denetimi paketiyle kaydediliyor
 Projenizdeki bir dosya kaynak denetimine eklendiğinde, ortam çağırır <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProject2.SetSccLocation%2A> tanımlama bilgileri kaynak denetim sistemi tarafından kullanılan dört donuk dizelerin sağlamak için. Bu dizeler, proje dosyanızda Store. Bu dizeler kaynak denetimi saplama (kaynak denetimi paketleri yöneten Visual Studio bileşeni) proje türünü başlangıçta çağırarak geçirilmelidir <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2.RegisterSccProject%2A>. Bu sırayla uygun kaynak denetimi paketini yükler ve uygulaması çağrısına iletilen `IVsSccManager2::RegisterSccProject`.

## <a name="see-also"></a>Ayrıca Bkz.
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2.RegisterSccProject%2A>
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProject2.SetSccLocation%2A>
- [Kaynak Denetimini Destekleme](../../extensibility/internals/supporting-source-control.md)