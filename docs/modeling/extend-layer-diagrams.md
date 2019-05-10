---
title: Bağımlılık diyagramlarını genişletme
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- dependency diagrams, creating extensions
- layer models
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9c164174b88ca9fdd815668084c1447e20de072c
ms.sourcegitcommit: 6a19c5ece38a70731496a38f2ef20676ff18f8a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65476562"
---
# <a name="extend-dependency-diagrams"></a>Bağımlılık diyagramlarını genişletme

Bağımlılık diyagramları oluşturmak için ve program kodunuza Visual Studio'da bağımlılık diyagramlarına karşı yapısı doğrulamak için kod yazabilirsiniz. Diyagramların (bağlam) kısayol menüsünde görünür, sürükle ve bırak hareketlerini özelleştirme ve metin şablonlarından katman modeline erişme komutlar ekleyebilirsiniz. Bu uzantılar bir Visual Studio Tümleştirme Uzantısı (VSIX) paketini ve diğer Visual Studio kullanıcılara dağıtın.

## <a name="requirements"></a>Gereksinimler

Aşağıdaki katman uzantılarınızı geliştirmek istediğiniz bilgisayarda yüklü olması gerekir:

- Visual Studio

- [Visual Studio SDK](../extensibility/visual-studio-sdk.md)

- Visual Studio için modelleme SDK'sı

[!INCLUDE[modeling_sdk_info](includes/modeling_sdk_info.md)]

Uygun bir sürümü Visual Studio'nun katman uzantılarınızı çalıştırmak istediğiniz bilgisayarda yüklü olması gerekir. Bağımlılık diyagramları Visual Studio'nun hangi sürümlerinin desteklediğini görmek için bkz: [mimari ve Modelleme Araçları sürüm desteği](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport).

## <a name="see-also"></a>Ayrıca bkz.

- [Bağımlılık diyagramları: Başvuru](../modeling/layer-diagrams-reference.md)
- [Bağımlılık diyagramları: Yönergeler](../modeling/layer-diagrams-guidelines.md)
- [Kodunuz aracılığıyla bağımlılık diyagramları oluşturma](../modeling/create-layer-diagrams-from-your-code.md)
- [Bağımlılık diyagramları ile kod doğrulama](../modeling/validate-code-with-layer-diagrams.md)
