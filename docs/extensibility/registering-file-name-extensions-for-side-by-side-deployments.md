---
title: Yan yana dağıtımlar için dosya adı uzantılarını kaydetme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- file extensions, registering for side-by-side
ms.assetid: 9ab046a2-147d-4167-aa14-7d661b1eaaa5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9bdfb562ddfcce2584b8868c3c931c21f9dbc127
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66334227"
---
# <a name="register-file-name-extensions-for-side-by-side-deployments"></a>Yan yana dağıtımlar için dosya adı uzantılarını kaydetme
Yan yana bir ortamda dağıtılan Vspackage'lar için dosyaları doğru sürümü ile ilişkilendirilecek dosya adı uzantıları kaydetmelisiniz [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Sürüme özgü dosya adı uzantısı kullanmıyorsanız, kayıt, kullanıcıların projenizi açın ve proje öğesi dosyaları uygun sürümünü de olanak tanır. [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].

## <a name="in-this-section"></a>Bu bölümde
- [Dosya adı uzantıları hakkında](../extensibility/about-file-name-extensions.md) nasıl dosya adı uzantılarının kayıtlı olduğundan açıklanır.

- [Dosya adı uzantıları için dosya işleyicileri belirtme](../extensibility/specifying-file-handlers-for-file-name-extensions.md) açabileceği uygulamalar, düzenleme ve benzeri, belirli bir dosya adı uzantısı kaydetme hakkında bilgi sağlar.

- [Dosya adı uzantıları için fiil kaydetme](../extensibility/registering-verbs-for-file-name-extensions.md) anlatılmaktadır fiiller kaydedin.

- [Yan yana dosya ilişkilendirmelerini yönetme](../extensibility/managing-side-by-side-file-associations.md) yan yana yüklemeleri, nasıl ele alınacağını açıklar belirli bir sürümü [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] bir dosyayı açmak için çağrılmalıdır.

## <a name="related-sections"></a>İlgili bölümler
- [Visual Studio'nun birden çok sürümünü destekleyen](../extensibility/supporting-multiple-versions-of-visual-studio.md) için birden çok sürümünü ilgili sorunlar açıklanmaktadır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] ve geliştirme ve son kullanıcıların dağıtım sırasında VSPackage'ı.