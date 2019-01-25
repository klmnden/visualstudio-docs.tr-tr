---
title: 'Nasıl yapılır: Kodun kısıtlı izinle belgelerin arkasında çalışmasına izin'
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
ms.openlocfilehash: 6030165e7b24bdba5c7fa6e223b915e5cf4c85c8
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54870262"
---
# <a name="how-to-permit-code-to-run-behind-documents-with-restricted-permissions"></a>Nasıl yapılır: Kodun kısıtlı izinle belgelerin arkasında çalışmasına izin
  Microsoft Office Bilgi Hakları Yönetimi (IRM) özelliğini, bir belge veya çalışma kitabı izinlerini kısıtlamak için kullanabilirsiniz. Varsayılan olarak, kısıtlı Microsoft Office Word belgesi veya Microsoft Office Excel çalışma kitabını arkasındaki kodun, çalışmasına izin verilmez. Varsayılan nesne modeli, yönetilen kod uzantıları erişebilir ve çözümünüzü çalışır böylece değiştirebilirsiniz.  
  
 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]  
  
 Belge veya çalışma kitabı yazarı olması veya izin ayarlarını değiştirmek için tam denetim erişimi olması gerekir.  
  
## <a name="to-permit-code-to-run-behind-documents-with-restricted-permissions"></a>Kodun kısıtlı izinle belgelerin arkasında çalışmasına izin için  
  
1. Belge veya çalışma kitabı Word veya Excel'de açın.  
  
2. Tıklayın **dosya** sekmesinde, işaret **hazırlama**, işaret **izinleri kısıtla**ve ardından **kısıtlı erişim**.  
  
   > [!NOTE]  
   >  İlk kez kullanıldığında, Windows Rights Management istemcisi yüklemeniz istenir. İstemciyi yükledikten sonra adımları tekrarlamanız gerekebilir.  
  
3. İçinde **izni** iletişim kutusunda **bu belgeye erişimi kısıtlamak**ve ardından **diğer seçenekler**.  
  
4. Altında **kullanıcılar için ek izinler**seçin **içeriği programlamayla erişme**.  
  
   Word veya Excel nesne modeline programlı erişim izin verir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Bilgi Hakları Yönetimine ve yönetilen kod uzantılarına genel bakış](../vsto/information-rights-management-and-managed-code-extensions-overview.md)   
 [Belge düzeyi çözümlerde belge koruması](../vsto/document-protection-in-document-level-solutions.md)   
 [Office belgelerinde parola koruması](../vsto/password-protection-on-office-documents.md)   
 [Office çözümleri oluşturma ve tasarlama](../vsto/designing-and-creating-office-solutions.md)   
 [Office çözümleri güvenliğini sağlama](../vsto/securing-office-solutions.md)   
 [Office çözümünü dağıtma](../vsto/deploying-an-office-solution.md)  
