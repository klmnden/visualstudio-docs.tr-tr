---
title: Bir bağlantı noktası sağlayıcısı uygulama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], implementing port suppliers
- port suppliers, implementing
ms.assetid: 6b8579df-58df-4c7f-8112-6015993e8765
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5d6875baf72d94494a1abaea9260e344b236f83c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56685930"
---
# <a name="implement-a-port-supplier"></a>Bağlantı noktası sağlayıcısı uygulama
Bağlantı noktası sağlayıcısı oturum hata ayıklama Yöneticisi (SDM) istek bağlantı noktaları sağlar. Bağlantı noktası sağlayıcısı, DCOM olmayan bir makine ya da yeni bir cihaz desteği gerektirdiğinde için hata ayıklama sırasında uygulanmalıdır. Örneğin, bir cep telefonu için hata ayıklama sağlamak için cep telefonu (belki de yoluyla veya bir hücre bağlantı IR) bağlanma ve bir telefonda çalışan programlar ve işlemleri numaralandırır bağlantı noktaları sağlayan bir bağlantı noktası sağlayıcısı ayarlayabilirsiniz.

 Kendi bağlantı noktası sağlayıcısı bu durumlarda ayarlama gerekmez. Bu nedenle Windows tabanlı makineler (uzaktan hata ayıklama dahil) üzerinde hata ayıklama programları için bağlantı noktası sağlayıcıları için yerel ve ortak dil çalışma zamanı (CLR) işlemleri, Visual Studio sağlar.

## <a name="in-this-section"></a>Bu bölümde
 [Uygulama ve bağlantı noktası sağlayıcısı kaydetme](../../extensibility/debugger/implementing-and-registering-a-port-supplier.md) SDM bağlantı noktalarını ve bağlantı noktası sağlayıcısı ile nasıl etkileşim kurduğu açıklanır.

 [Gerekli bağlantı noktası sağlayıcısı arabirimleri](../../extensibility/debugger/required-port-supplier-interfaces.md) bağlantı noktası sağlayıcısı almak için uygulanmalı arabirimleri belgeleri.

## <a name="related-sections"></a>İlgili bölümler
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md) ana hata ayıklama mimari kavramlarını açıklar.

## <a name="see-also"></a>Ayrıca bkz.
 [Visual Studio hata ayıklayıcı genişletilebilirliği](../../extensibility/debugger/visual-studio-debugger-extensibility.md)