---
title: Bilgi Hakları Yönetimine ve yönetilen kod uzantılarına genel bakış
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Information Rights Management [Office development in Visual Studio]
- workbooks [Office development in Visual Studio], restricted permissions
- IRM [Office development in Visual Studio]
- documents [Office development in Visual Studio], restricted permissions
- rights management [Office development in Visual Studio]
- Office documents [Office development in Visual Studio, restricted permissions
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 109f6b85653a842f7c6fc9ce2d2c09b74113bbc7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62583926"
---
# <a name="information-rights-management-and-managed-code-extensions-overview"></a>Bilgi Hakları Yönetimine ve yönetilen kod uzantılarına genel bakış
  Microsoft Office Word ve Microsoft Office Excel, yetkisiz kişilerin hassas bilgileri görmesini veya değiştirmesini önlemeye yardımcı olabilecek bir özellik olan Bilgi Hakları Yönetimi (IRM) sağlayın. Bilgi hakları yönetimini nasıl çalıştığı hakkında daha fazla bilgi için belirli Office uygulamasında yardımına bakın.

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

## <a name="run-code-behind-documents-with-restricted-permissions"></a>Belgelerin arkasındaki kod kısıtlı izinlerle çalıştırın
 Çözümünüz bir belge veya varsayılan olarak, IRM kullanan çalışma kitabı içeriyorsa, Word ve Excel çalıştırmak için herhangi bir kod izin vermez. Belgenin yazarı olan veya tam denetim erişimi varsa, böylece çözümünüzün çalışması varsayılan değiştirebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Kodun kısıtlı izinle belgelerin arkasında çalışmasına izin](../vsto/how-to-permit-code-to-run-behind-documents-with-restricted-permissions.md).

 IRM kullanımını engeller <xref:Microsoft.VisualStudio.Tools.Applications.Runtime.ServerDocument> almak veya belgede önbelleğe alınmış verileri işlemek için.

## <a name="end-users-to-restrict-permissions-to-documents-that-use-managed-code-extensions"></a>Son kullanıcıların yönetilen kod uzantıları kullanan belgeler için izinleri kısıtla
 Çözümünüzde belge veya çalışma kitabını tam denetim erişimi olan herkes IRM izinlerini kısıtlamak için kullanabilirsiniz. Örneğin, muhasebe departmanındaki bir son kullanıcı otomatik olarak bir çalışma sayfasına bir veritabanındaki verilerle dolduran bir çözümü kullanıyorsa, bu kullanıcı yalnızca kendi kişilere erişimi değiştir ve diğerleri için okuma erişimi izin vermek isteyebilirsiniz. Kullanıcı, kısıtlı izinleri eklediğinde, varsayılan olarak, çalışma arka plan kod çalıştırılamaz ve çalışma verilerle doldurulmaz.

 Sorunu gidermek için belge veya çalışma kitabını tam denetim erişimi olan nesne modeli programlı erişim izni vermek için varsayılan izin ayarları değiştirmeniz gerekir. Daha fazla bilgi için [nasıl yapılır: Kodun kısıtlı izinle belgelerin arkasında çalışmasına izin](../vsto/how-to-permit-code-to-run-behind-documents-with-restricted-permissions.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Belge düzeyi çözümlerde belge koruması](../vsto/document-protection-in-document-level-solutions.md)
- [Office belgelerinde parola koruması](../vsto/password-protection-on-office-documents.md)
- [Office çözümleri güvenliğini sağlama](../vsto/securing-office-solutions.md)
- [Office çözümünü dağıtma](../vsto/deploying-an-office-solution.md)
- [Office çözümleri oluşturma ve tasarlama](../vsto/designing-and-creating-office-solutions.md)
