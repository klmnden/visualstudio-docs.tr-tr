---
title: Visual Studio içinde Office işlevselliğini kullanma
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- security [Office development in Visual Studio], document protection
- Office applications [Office development in Visual Studio]
- Office functionality inside Visual Studio
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: c47ed9639a33ecdea3451c63b729d959f6855e5d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62982341"
---
# <a name="use-office-functionality-inside-of-visual-studio"></a>Visual Studio içinde Office işlevselliğini kullanma
  Bir belge düzeyi projesi oluşturduğunuzda, belge ve ilişkili uygulama tasarlayın ve doğrudan belge ile çalışmak için Visual Studio içinde barındırılır. Uygulamayı açmak Visual Studio'da Microsoft Office olduğunda, genellikle beklendiği gibi çalışır. Ancak, uygulamanın işlevselliğini bazıları, farklı veya erişilemez.

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

## <a name="document-protection"></a>Belge koruması
 Microsoft Office Word ve Microsoft Office Excel belge projelerinizde kullanabileceğiniz koruma özellikleri sunar. Belge, Visual Studio'da açıkken belge koruması etkinleştirilirse, ancak bu, bazı tasarım değişiklikleri yapmasını engelleyebilirsiniz. Daha fazla bilgi için [koruma belge düzeyi çözümlerde belge](../vsto/document-protection-in-document-level-solutions.md).

## <a name="information-rights-management"></a>Bilgi Hakları Yönetimi
 Bilgi Hakları Yönetimi (IRM), Microsoft Office Excel ve Microsoft Office Word'ü de kullanılabilir. IRM, yetkisiz kişilerin hassas bilgileri görmesini veya değiştirmesini önlemeye yardımcı olabilir. Ancak, IRM kodunuzu de çalışmasını engelleyebilir. Daha fazla bilgi için [bilgi hakları yönetimine ve yönetilen kod uzantılarına genel bakış](../vsto/information-rights-management-and-managed-code-extensions-overview.md).

## <a name="password-protection"></a>Parola koruması
 Böylece bunlar parola bilmeyen kişi tarafından açılamıyor, Microsoft Office Word belgelerini ve Microsoft Office Excel çalışma kitaplarını ayarlanabilir. Parola koruması, Word ve Excel'de farklı şekilde ele alınır ve geliştirme sürecinizin etkileyebilir. Daha fazla bilgi için [Office belgelerinde parola koruması](../vsto/password-protection-on-office-documents.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Belge düzeyi çözümlerde belge koruması](../vsto/document-protection-in-document-level-solutions.md)
- [Bilgi Hakları Yönetimine ve yönetilen kod uzantılarına genel bakış](../vsto/information-rights-management-and-managed-code-extensions-overview.md)
- [Office belgelerinde parola koruması](../vsto/password-protection-on-office-documents.md)
- [Nasıl yapılır: Kod çalıştırmadan Office çözümlerini açma](../vsto/how-to-open-office-solutions-without-running-code.md)
