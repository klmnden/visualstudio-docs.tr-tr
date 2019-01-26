---
title: Sözleşmeler birlikte çalışma bütünleştirilmiş kodlarında komut | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- command handling with interop assemblies, command contracts
- interop assemblies, command contracts
ms.assetid: 57245708-f539-42dc-8963-2754a48f0189
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9daadac56fd74fe78cc5606f94927d1057496dd1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54949941"
---
# <a name="command-contracts-in-interop-assemblies"></a>Birlikte çalışma bütünleştirilmiş kodlarında komut sözleşmeleri
Komutları işlemeye yönelik temel sözleşmesi <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> arabirimidir ortam çağırır <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus%2A> komutu desteklenip desteklenmediğini ve bu desteklenip desteklenmediğini belirlemek için metin ve durumu belirlemek için yöntemi. Sonra ortamı çağrıları <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.Exec%2A> komutu yürütmek için yöntemi.  
  
 <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus%2A> Yöntemi tüm komutlar için aynı şekilde işlenir. Daha fazla iletişim (örneğin, açılan listeler ile), gerekirse yönetilir çağırarak <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.Exec%2A> uygun parametrelerle yöntemi. Bu parametre yorumu belirtilen komut bağlıdır.  
  
 Komut hedefi çıkış parametresi değerleri döndürürse, çağıran her zaman ayrılmış tüm kaynakları serbest bırakma için sorumludur. Bu parametre bir değişken olduğundan, değişken temizleme kaynakları serbest bırakır.  
  
 Burada komutları gerekir çalışan bir hiyerarşi penceresinde durumlarda <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> arabirimi kullanılmalıdır. <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> Benzer yöntemler ile benzer bir sözleşme arabirimi vardır: <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.QueryStatusCommand%2A> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.ExecCommand%2A>.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSPackage kullanıcı arabirimi öğelerini nasıl eklenir](../../extensibility/internals/how-vspackages-add-user-interface-elements.md)   
 [Vspackage'larda komut yönlendirme](../../extensibility/internals/command-routing-in-vspackages.md)   
 [Komut uygulama](../../extensibility/internals/command-implementation.md)