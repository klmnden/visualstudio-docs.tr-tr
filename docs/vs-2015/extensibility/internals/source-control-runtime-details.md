---
title: Kaynak Denetimi çalışma zamanı ayrıntıları | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- source control [Visual Studio SDK], runtime details
ms.assetid: 1acd30e0-f98c-4bde-b9cd-4076845887df
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 38b086f578d71c291ef12cb7b90e3ba1ce1ee89f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49212441"
---
# <a name="source-control-runtime-details"></a>Kaynak Denetimi Çalışma Zamanı Ayrıntıları
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Kullanıcı bir dosya projede kaynak denetimi için veya bir sihirbaz gibi Otomasyon denetleyicisi aracılığıyla eklediğinde projesi kaynak denetimine eklenir. Bir proje kendisi için kaynak denetimi altında olduğunu belirtmez; Kaynak denetimi destekler, ancak kendisine el ile eklenmesi gerekir.  
  
## <a name="registering-with-a-source-control-package"></a>Bir kaynak denetimi paketiyle kaydediliyor  
 Projenizdeki bir dosya kaynak denetimine eklendiğinde, ortam çağırır <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProject2.SetSccLocation%2A> tanımlama bilgileri kaynak denetim sistemi tarafından kullanılan dört donuk dizelerin sağlamak için. Bu dizeler, proje dosyanızda Store. Bu dizeler kaynak denetimi saplama (kaynak denetimi paketleri yöneten Visual Studio bileşeni) proje türünü başlangıçta çağırarak geçirilmelidir <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2.RegisterSccProject%2A>. Bu sırayla uygun kaynak denetimi paketini yükler ve uygulaması çağrısına iletilen `IVsSccManager2::RegisterSccProject`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2.RegisterSccProject%2A>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProject2.SetSccLocation%2A>   
 [Kaynak Denetimini Destekleme](../../extensibility/internals/supporting-source-control.md)

