---
title: Kodun kısıtlı izinle docs çalışmasına izin
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Information Rights Management [Office development in Visual Studio]
- permissions [Office development in Visual Studio]
- IRM [Office development in Visual Studio]
- code [Office development in Visual Studio], running behind restricted documents
- documents [Office development in Visual Studio], restricted permissions
- Office documents [Office development in Visual Studio, restricted permissions
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 32e42954958fda71d54c3c0ac2685928644e7461
ms.sourcegitcommit: 25570fb5fb197318a96d45160eaf7def60d49b2b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66402253"
---
# <a name="how-to-permit-code-to-run-behind-documents-with-restricted-permissions"></a>Nasıl yapılır: Kodun kısıtlı izinle belgelerin arkasında çalışmasına izin
  Microsoft Office Bilgi Hakları Yönetimi (IRM) özelliğini, bir belge veya çalışma kitabı izinlerini kısıtlamak için kullanabilirsiniz. Varsayılan olarak, kısıtlı Microsoft Office Word belgesi veya Microsoft Office Excel çalışma kitabını arkasındaki kodun, çalışmasına izin verilmez. Varsayılan nesne modeli, yönetilen kod uzantıları erişebilir ve çözümünüzü çalışır böylece değiştirebilirsiniz.

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

 Belge veya çalışma kitabı yazarı olması veya izin ayarlarını değiştirmek için tam denetim erişimi olması gerekir.

## <a name="to-permit-code-to-run-behind-documents-with-restricted-permissions"></a>Kodun kısıtlı izinle belgelerin arkasında çalışmasına izin için

1. Belge veya çalışma kitabı Word veya Excel'de açın.

2. Tıklayın **dosya** sekmesinde, işaret **hazırlama**, işaret **izinleri kısıtla**ve ardından **kısıtlı erişim**.

   > [!NOTE]
   > İlk kez kullanıldığında, Windows Rights Management istemcisi yüklemeniz istenir. İstemciyi yükledikten sonra adımları tekrarlamanız gerekebilir.

3. İçinde **izni** iletişim kutusunda **bu belgeye erişimi kısıtlamak**ve ardından **diğer seçenekler**.

4. Altında **kullanıcılar için ek izinler**seçin **içeriği programlamayla erişme**.

   Word veya Excel nesne modeline programlı erişim izin verir.

## <a name="see-also"></a>Ayrıca bkz.
- [Bilgi Hakları Yönetimine ve yönetilen kod uzantılarına genel bakış](../vsto/information-rights-management-and-managed-code-extensions-overview.md)
- [Belge düzeyi çözümlerde belge koruması](../vsto/document-protection-in-document-level-solutions.md)
- [Office belgelerinde parola koruması](../vsto/password-protection-on-office-documents.md)
- [Office çözümleri oluşturma ve tasarlama](../vsto/designing-and-creating-office-solutions.md)
- [Office çözümleri güvenliğini sağlama](../vsto/securing-office-solutions.md)
- [Office çözümünü dağıtma](../vsto/deploying-an-office-solution.md)
