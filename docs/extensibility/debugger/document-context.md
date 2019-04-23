---
title: Belge bağlamı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], contexts
ms.assetid: 8e8b5702-5c16-4988-953d-69dd807d8b84
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3a60b95faf9c22ccec45dc560031bf517f53028b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60080223"
---
# <a name="document-context"></a>Belge bağlamı
İçinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklama, bir *belge bağlamına*:

- Kaynak dosyada bir konumu temsil eder. Burada kaynak dosyanın mevcut olmayabilir diller için tipik olarak çalışma zamanı ortamı tarafından oluşturulan bir belge bir konumda bir belge bağlamı tanımlar. Örneğin, bir komut dosyası altyapısı bir belge betikten üretebilir. Daha fazla bilgi için [belge konumu](../../extensibility/debugger/document-position.md).

- Bir konuma karşılık gelen bir kod bağlamı için bir kaynak belgedeki açıklar. Sembol işleyici belgeleri bağlam, bir derleyici veya yorumlayıcısı tarafından oluşturulan bilgileri kullanarak bir kod bağlamı eşlenir.

- Tarafından uygulanan bir [IDebugDocumentContext2](../../extensibility/debugger/reference/idebugdocumentcontext2.md) arabirimi.

## <a name="see-also"></a>Ayrıca bkz.
- [Kod bağlamı](../../extensibility/debugger/code-context.md)
- [Sembol sağlayıcısı](../../extensibility/debugger/symbol-provider.md)
- [Sembol sağlayıcısı arabirimleri](../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md)