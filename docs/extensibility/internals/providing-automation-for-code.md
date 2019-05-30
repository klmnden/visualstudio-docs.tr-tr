---
title: Kod için Otomasyon sağlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- CodeModel object
ms.assetid: 21cb3e63-f25c-404b-bc1d-a32ad0fdd4d5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7c7fa6836f3c396471e3b330d94b67d0978252e3
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66341554"
---
# <a name="providing-automation-for-code"></a>Kod için Otomasyon Sağlama
Kodunuz için bir otomasyon modeli oluşturulması gerekli değildir. Ortamı SDK'sı, bunu yapmak için bir örnek sağlamaz. Kod modelleri hakkında bilgi için bkz: <xref:EnvDTE.CodeModel> nesne.

 Kod modeli uygulamak için iç veri yapısı tarafından belirlenen hiçbir arabirimi uygulamalıdır. Nesneleri nesnesinden türetilmesi `IDispatch` sınıfı.

 Genişlettiğinizde, nesneleri <xref:EnvDTE.CodeModel> ve <xref:EnvDTE.FileCodeModel>, kullanılabilir <xref:EnvDTE.Project> nesne ve aşağıdakine benzer:

- <xref:EnvDTE.Project.CodeModel%2A>

- <xref:EnvDTE.ProjectItem.FileCodeModel%2A>

 Uygulamak seçebilirsiniz yalnızca `CodeModel` veya `FileCodeModel` arabirimi, iade nesnesinde, `Project` ve <xref:EnvDTE.ProjectItem> nesneleri. Bu arabirimden, proje sistemi için uygun olan herhangi bir işlevsellik sağlar.

 Yöntemleri veya özellikleri gibi özellikler eklemek istiyorsanız, kullanılabilir değil standart `CodeModel` ve `FileCodeModel` arabirimleri, standart devralan kendi arabirimi oluşturun. Son kullanıcılar için aranacak bilmesi, proje sisteminizi belgelediğinizden emin olun. Standart arabirimi döndürür, ancak kullanıcı çağırabilirsiniz `QueryInterface` yöntemi veya mevcut biliniyorsa, arabirime cast.

## <a name="see-also"></a>Ayrıca Bkz.
- [Otomasyon Modeline Genel Bakış](../../extensibility/internals/automation-model-overview.md)