---
title: Azure komut satırı ile derlemeyi | Microsoft Docs
description: Azure komut satırı derleme
services: visual-studio-online
author: ghogen
manager: douge
assetId: 94b35d0d-0d35-48b6-b48b-3641377867fd
ms.prod: visual-studio-dev15
ms.technology: vs-azure
ms.custom: vs-azure
ms.workload: azure-vs
ms.topic: conceptual
origin.date: 03/05/2017
ms.date: 09/10/2018
ms.author: v-junlch
ms.openlocfilehash: 8c96713a06c66fe34e34417e9e8595ba07e50485
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62989812"
---
# <a name="building-azure-projects-from-the-command-line"></a>Komut satırından Azure projeler derleme
Microsoft Build Engine (MSBuild) kullanarak, Visual Studio yüklü olduğu yapı Laboratuvar ortamlarında ürünleri oluşturabilirsiniz. MSBuild, genişletilebilir ve tamamen Microsoft tarafından desteklenen proje dosyaları için bir XML biçimini kullanır. MSBuild dosyası biçimini kullanarak, hangi öğe olmalıdır açıklayabilirsiniz bir veya daha fazla platform ve yapılandırmaları için yerleşik.

MSBuild komut satırında çalıştırabilirsiniz ve bu konuda, bu yaklaşımı açıklanmaktadır. Komut satırında özelliklerini ayarlayarak, bir projenin belirli yapılandırmalar oluşturabilirsiniz. Benzer şekilde, MSBuild'ı oluşturan hedefleri tanımlayabilirsiniz. Komut satırı parametreleri ve MSBuild hakkında daha fazla bilgi için bkz. [MSBuild komut satırı başvurusu](https://msdn.microsoft.com/library/ms164311.aspx).

## <a name="msbuild-parameters"></a>MSBuild parametreleri
MSBuild ile çalıştırmak için bir paket oluşturmak için en kolay yolu olan `/t:Publish` seçeneği. Varsayılan olarak, bu komut bir proje kök klasörü ile ilgili gibi dizini `<ProjectDirectory>\bin\Configuration\app.publish\`. Bir Azure projesi oluşturma sırasında iki dosya oluşturulur: Paket dosyası kendisi ve eşlik eden yapılandırma dosyası:

- Paket dosyası (`project.cspkg`)
- Yapılandırma dosyası (`ServiceConfiguration.TargetProfile.cscfg`)

Yerel (hata ayıklama) derlemeleri için bir hizmet yapılandırma dosyası, diğeri bulut (hazırlık veya üretim) derlemeleri için varsayılan olarak, her bir Azure projesi içerir. Ancak, ekleyebilir veya gerektiği gibi hizmet yapılandırma dosyalarını kaldırın. Visual Studio içinden bir paket oluşturduğunuzda, hangi hizmet yapılandırma dosyasının yanı sıra paketini içerecek şekilde istenir. MSBuild kullanarak bir paket oluşturduğunuzda, yerel hizmet yapılandırma dosyasını varsayılan olarak dahil edilir. Farklı bir hizmet yapılandırma dosyası içerecek şekilde `TargetProfile` MSBuild komut özelliğini (`MSBuild /t:Publish /p:TargetProfile=ProfileName`).

Depolanan paket ve yapılandırma dosyaları için alternatif bir dizin kullanmak istiyorsanız, yolu kullanarak ayarlamak `/p:PublishDir=Directory\` seçeneği, sondaki eğik çizgi ayırıcı dahil.

## <a name="next-steps"></a>Sonraki adımlar
Paket oluşturulduktan sonra Azure'a dağıtabilirsiniz.

<!-- Update_Description: update metedata properties -->