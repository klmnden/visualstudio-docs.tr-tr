---
title: Hata ayıklama görevleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], tasks
ms.assetid: 5d60e9e8-305e-4a48-829f-b9440fc8af7b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 299db84fb06679bfbf9dff92234c944cbdec6295
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56695212"
---
# <a name="debug-tasks"></a>Hata ayıklama görevleri
Bir programda hata ayıklamak için onu başlatan gerekir ve bir hata ayıklama altyapısı (DE) bağlı gerekir, aksi takdirde DE daha önce başlatılan bir program için'e bağlı olması gerekir. Bağlandıktan sonra DE bazı başlangıç olayları oluşturmanız gerekir. Yanıt olarak, hata ayıklama paketi IDE içinde ayarlanan kesme noktaları bağlama dener. Programı ilişkili bir kesme noktasına ulaştığında, durdurur ve kullanıcı girdisini bekler.

## <a name="in-this-section"></a>Bu bölümde
 [Güvenlik sorunları](../../extensibility/debugger/security-issues.md) bir programda hata ayıklamak için gerekli olan güvenlik adımları ele alınmıştır.

 [Bir program Başlat](../../extensibility/debugger/launching-a-program.md) programını başlatmak için işletim sistemini çağıran bir DE belirtmek adım adım yönergeler sağlar.

 [Doğrudan programa ekleme](../../extensibility/debugger/attaching-directly-to-a-program.md) bir programda zaten çalışan bir işlemde hata ayıklamak için kullanılan işlem açıklanır.

 [Başlatmadan sonra Başlangıç olaylarını gönderme](../../extensibility/debugger/sending-startup-events-after-a-launch.md) program kendi ana giriş noktasıdır ve hata ayıklama için hazır olana kadar DE programa ekledikten sonra gerçekleşecek olaylar listeler.

 [Yürütme denetimi](../../extensibility/debugger/control-of-execution.md) nasıl DE genellikle bir giriş noktası olayı, bir yük tamamlama olayı veya koşullara bağlı olarak bir durdurma olay gönderir açıklar.

 [Kesme noktaları bağlama](../../extensibility/debugger/binding-breakpoints.md) nasıl, kullanıcı bir kesme noktası ayarlar, IDE istek formulates ve kesme noktası oluşturmak için hata ayıklama oturumu ister açıklar.

 [Nevyhodnocovat](../../extensibility/debugger/evaluating-expressions.md) ifadeler nasıl oluşturulduğunu ve bir ifade değerlendirildiğinde ne olacağını açıklar.

 [Görselleştirme ve verileri görüntüleme](../../extensibility/debugger/visualizing-and-viewing-data.md) tür görselleştiricileri ve özel görüntüleyiciler (EE) ifade değerlendiricisi tarafından nasıl desteklendiği anlatılır.

## <a name="related-sections"></a>İlgili bölümler
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md) ana hata ayıklama mimari kavramlarını açıklar.

 [Hata ayıklayıcı bileşenleri](../../extensibility/debugger/debugger-components.md) Visual Studio bileşenleri DE EE ve sembol işleyici (SH) hata ayıklama genel bir bakış sağlar.

 [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md) DE kod, belgeler ve ifade değerlendirme bağlamı içinde aynı anda nasıl çalıştığı açıklanmaktadır. , Her üç bağlamları, konumu, konum veya değerlendirme için ilgili açıklar.

## <a name="see-also"></a>Ayrıca bkz.
 [Kullanmaya başlama](../../extensibility/debugger/getting-started-with-debugger-extensibility.md)