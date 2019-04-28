---
title: 'Nasıl yapılır: Office çözümlerini imzalama'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- certificates [Office development in Visual Studio], Office solutions
- security [Office development in Visual Studio], signing Office solutions
- signing manifests [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 1fff7555c17f4fdac43de2690f8e133cc32881db
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62971127"
---
# <a name="how-to-sign-office-solutions"></a>Nasıl yapılır: Office çözümlerini imzalama
  Bir çözüm oturum açarsanız, kanıt olarak sertifika kullanarak çözüme güven verebilirsiniz. Birden çok çözüm için aynı sertifikayı kullanabilirsiniz ve tüm çözümleri hiçbir ek güvenlik ilkesi güncelleştirmeleriyle güvenilen olacaktır.

 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]

 Uygulamayı el ile düzenlemeniz ve dağıtım bildirimlerini bildirim oluşturma ve düzenleme aracı kullanarak (*mage.exe* ve *mageui.exe*), kullanabilmeniz için önce bildirimleri yeniden imzalamanız gerekir. Daha fazla bilgi için [nasıl yapılır: Uygulama ve dağıtım bildirimlerini yeniden imzalama](../deployment/how-to-re-sign-application-and-deployment-manifests.md).

## <a name="sign-by-using-a-certificate"></a>Bir sertifika kullanarak oturum açın
 Bir sertifika benzersiz bir anahtar ve çözüm yayıncısı kimliğini içeren bir dosyadır. Bir sertifika yetkilisinden sertifika satın alın veya kendi sertifikanızı oluşturun ve sahip bir sertifika yetkilisi imzalayın.

 Visual Studio Office çözümleri hata ayıklamayı etkinleştirmek için geçici bir sertifika ile imzalar. Dağıtılan çözümleri durum kanıtı geçici bir sertifika kullanmamalıdır.

### <a name="to-sign-an-office-solution-by-using-a-certificate"></a>Bir sertifika kullanarak Office çözümü imzalamak için

1. Üzerinde **proje** menüsünü tıklatın _SolutionName_**özellikleri**.

2. Tıklayın **imzalama** sekmesi.

3. Seçin **ClickOnce bildirimlerini imzala**.

4. Tıklayarak sertifikayı bulun **Store ' seçin** veya **dosyadan Seç** ve sertifikada gezinin.

5. Doğru sertifikayı kullanılmakta olduğunu doğrulamak için tıklayın **daha fazla ayrıntı** sertifika bilgileri görüntülemek için.

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümleri güvenliğini sağlama](../vsto/securing-office-solutions.md)
- [Office çözümlerine güven verme](../vsto/granting-trust-to-office-solutions.md)
- [İmzalama Sayfası, Proje Tasarımcısı](../ide/reference/signing-page-project-designer.md)
