---
title: Kod için Otomasyon sağlama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- CodeModel object
ms.assetid: 21cb3e63-f25c-404b-bc1d-a32ad0fdd4d5
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: b3a7f1bc0f3394f0b7c0d882657d926ce11259a0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62859307"
---
# <a name="providing-automation-for-code"></a>Kod için Otomasyon Sağlama
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Kodunuz için bir otomasyon modeli oluşturulması gerekli değildir. Ortamı SDK'sı, bunu yapmak için bir örnek sağlamaz. Kod modelleri hakkında bilgi için bkz: <xref:EnvDTE.CodeModel> nesne.  
  
 Kod modeli uygulamak için iç veri yapısı tarafından belirlenen hiçbir arabirimi uygulamalıdır. Nesneleri nesnesinden türetilmesi `IDispatch` sınıfı.  
  
 Genişlettiğinizde, nesneleri <xref:EnvDTE.CodeModel> ve <xref:EnvDTE.FileCodeModel>, kullanılabilir <xref:EnvDTE.Project> nesne ve aşağıdakine benzer:  
  
 <xref:EnvDTE.Project.CodeModel%2A>  
  
 <xref:EnvDTE.ProjectItem.FileCodeModel%2A>  
  
 Uygulamak seçebilirsiniz yalnızca `CodeModel` veya `FileCodeModel` arabirimi, iade nesnesinde, `Project` ve <xref:EnvDTE.ProjectItem> nesneleri. Bu arabirimden, proje sistemi için uygun olan herhangi bir işlevsellik sağlar.  
  
 Yöntemleri veya özellikleri gibi özellikler eklemek istiyorsanız, kullanılabilir değil standart `CodeModel` ve `FileCodeModel` arabirimleri, standart devralan kendi arabirimi oluşturun. Son kullanıcılar için aranacak bilmesi, proje sisteminizi belgelediğinizden emin olun. Standart arabirimi döndürür, ancak kullanıcı çağırabilirsiniz `QueryInterface` yöntemi veya mevcut biliniyorsa, arabirime cast.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Otomasyon Modeline Genel Bakış](../../extensibility/internals/automation-model-overview.md)
