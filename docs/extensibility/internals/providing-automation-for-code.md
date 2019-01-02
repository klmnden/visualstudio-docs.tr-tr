---
title: Kod için Otomasyon sağlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- CodeModel object
ms.assetid: 21cb3e63-f25c-404b-bc1d-a32ad0fdd4d5
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 3922de57a275dd24ce3161209b7775db104afada
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53896441"
---
# <a name="providing-automation-for-code"></a>Kod için Otomasyon Sağlama
Kodunuz için bir otomasyon modeli oluşturulması gerekli değildir. Ortamı SDK'sı, bunu yapmak için bir örnek sağlamaz. Kod modelleri hakkında bilgi için bkz: <xref:EnvDTE.CodeModel> nesne.  
  
 Kod modeli uygulamak için iç veri yapısı tarafından belirlenen hiçbir arabirimi uygulamalıdır. Nesneleri nesnesinden türetilmesi `IDispatch` sınıfı.  
  
 Genişlettiğinizde, nesneleri <xref:EnvDTE.CodeModel> ve <xref:EnvDTE.FileCodeModel>, kullanılabilir <xref:EnvDTE.Project> nesne ve aşağıdakine benzer:  
  
 <xref:EnvDTE.Project.CodeModel%2A>  
  
 <xref:EnvDTE.ProjectItem.FileCodeModel%2A>  
  
 Uygulamak seçebilirsiniz yalnızca `CodeModel` veya `FileCodeModel` arabirimi, iade nesnesinde, `Project` ve <xref:EnvDTE.ProjectItem> nesneleri. Bu arabirimden, proje sistemi için uygun olan herhangi bir işlevsellik sağlar.  
  
 Yöntemleri veya özellikleri gibi özellikler eklemek istiyorsanız, kullanılabilir değil standart `CodeModel` ve `FileCodeModel` arabirimleri, standart devralan kendi arabirimi oluşturun. Son kullanıcılar için aranacak bilmesi, proje sisteminizi belgelediğinizden emin olun. Standart arabirimi döndürür, ancak kullanıcı çağırabilirsiniz `QueryInterface` yöntemi veya mevcut biliniyorsa, arabirime cast.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Otomasyon Modeline Genel Bakış](../../extensibility/internals/automation-model-overview.md)