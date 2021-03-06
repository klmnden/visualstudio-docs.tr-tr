---
title: Güvenli dağıtım
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- deploying applications [Office development in Visual Studio], security
- Office development in Visual Studio, security
- Office applications [Office development in Visual Studio], security
- ClickOnce deployment [Office development in Visual Studio], security
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 1000504ad83706bd028af4bd668da7483e478b7a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62978386"
---
# <a name="secure-deployment"></a>Güvenli dağıtım
  Bir Office çözümü oluşturduğunuzda, geliştirme bilgisayarınıza kod projenize çalışmasına izin vermek için otomatik olarak güncelleştirilir. Ancak, çözümünüzü dağıtırken kanıt güven kararı çözümü ile bir sertifika imzalama veya kullanarak temel sağlamalısınız [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)] güven istemi anahtarı. Daha fazla bilgi için [Office çözümlerine güven verme](../vsto/granting-trust-to-office-solutions.md).

 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]

 Bir ağ konumuna belgeyi dağıtırsanız, belge düzeyinde özelleştirmeler için Ayrıca belgenin konumunu Office uygulamasının Güven Merkezi'ndeki güvenilir konum listesine eklemeniz gerekir. Son kullanıcı bilgisayarlarında belge izinleri ayarlama hakkında daha fazla bilgi için bkz. [belgelere güven verme](../vsto/granting-trust-to-documents.md).

## <a name="prevent-office-solutions-from-running-code"></a>Office çözümlerinde kod çalıştırmasını engelleyebilir.
 Yöneticiler, tüm Office çözümlerini bir bilgisayar üzerinde çalışmasını önlemek için kayıt defteri kullanabilirsiniz. Yönetilen kod uzantıları bir Office çözümü açıldığında, Office çalışma zamanı denetimleri için Visual Studio Araçları bir giriş olmadığını adıyla `Disabled` bilgisayara aşağıdaki kayıt defteri anahtarlarından biri altında bulunmaktadır:

- **HKEY_CURRENT_USER\Software\Microsoft\VSTO**

- **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\vsto**

  Office çözümlerinde kod çalıştırılmasını engellemek için oluşturun bir `Disabled` giriş birine veya ikisine de bu kayıt defteri anahtarları altında ve aşağıdaki veri türlerini ve değerlerini belirtin `Disabled`:

- REG_SZ veya "0" (sıfır) dışında herhangi bir dize olarak ayarlanmış REG_EXPAND_SZ.

- 0 (sıfır) dışında herhangi bir değere ayarlanmış REG_DWORD.

  Office çözümlerini kod etkinleştirmek için her ikisi de ayarlayın `Disabled` 0 (sıfır) girişleri veya kayıt defteri girdilerini silin.

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümünü dağıtma](../vsto/deploying-an-office-solution.md)
- [Çalıştırın veya Office çözümlerini barındırmak için bilgisayarları hazırlama](https://msdn.microsoft.com/be1b173f-7261-4d74-aa4e-94ccd43db8d8)
- [Office çözümleri güvenliğini sağlama](../vsto/securing-office-solutions.md)
