---
title: Proje önceliği | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], opening items
ms.assetid: 9f707592-2fb6-4f75-9269-f6d4700a998e
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: b012136c30f72cfdddadfc1a370ed76f567afffd
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62429918"
---
# <a name="project-priority"></a>Proje Önceliği
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir proje öğesi genellikle yalnızca bir proje çözümde üyesidir. Bu nedenle, IDE kolayca hangi proje öğesini açmak için kullanılan belirleyebilirsiniz. Ancak, bir öğe birden çok proje üyesi ise, IDE öğesini açmak için en iyi proje belirlemek için bir öncelik düzenini kullanır.  
  
 Aşağıdaki liste, proje Öncelik düzenini gösterir:  
  
- IDE çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject2.IsDocumentInProject%2A> belge proje üyesi olup olmadığını belirlemek için çözümde her proje için yöntemi.  
  
- Belge proje üyesi ise, proje önceliğine sahip, projeyi bu belgeyi kendi işlenmesini göre atar yanıt verir. Örneğin, bir dil proje kendi dil kaynak dosyaları için yüksek bir öncelik verir ancak kendi yapı işleminin bir parçası kullanılmayan bir tanınmayan dosya türü için daha düşük bir öncelik verir.  
  
- Bir belge için özel, projeye özgü düzenleyicileri veya tasarımcıları sağlayan projeleri de yüksek öncelik alır.  
  
- <xref:Microsoft.VisualStudio.Shell.Interop.VSDOCUMENTPRIORITY> Numaralandırma belge öncelik değerleri sağlar.  
  
- En yüksek öncelikli belirten proje bağlamı belgeyi açmak için verilir. İki proje eşit öncelik değerleri dönerseniz, etkin proje tercih edilir. Bu belgeyi açamazsınız çözümdeki hiçbir proje yanıt verirse, IDE diğer dosyalar projesinde belge koyar. Daha fazla bilgi için [diğer dosyalar projesi](../../extensibility/internals/miscellaneous-files-project.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çeşitli dosyalar projesi](../../extensibility/internals/miscellaneous-files-project.md)   
 [Nasıl yapılır: Açık açık belgeler için düzenleyicileri](../../extensibility/how-to-open-editors-for-open-documents.md)   
 [Proje ve Proje Öğesi Şablonları Ekleme](../../extensibility/internals/adding-project-and-project-item-templates.md)
