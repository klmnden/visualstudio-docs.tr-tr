---
title: Office belgelerinde parola koruması
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- permissions [Office development in Visual Studio]
- workbooks [Office development in Visual Studio], restricted permissions
- passwords [Office development in Visual Studio], document protections
- documents [Office development in Visual Studio], restricted permissions
- Office documents [Office development in Visual Studio, restricted permissions
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: e3c9521389ce348a482f35ec95c9766edea49f5f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62977906"
---
# <a name="password-protection-on-office-documents"></a>Office belgelerinde parola koruması
  Böylece bunlar parola bilmeyen kişi tarafından açılamıyor, Microsoft Office Word belgelerini ve Microsoft Office Excel çalışma kitaplarını parola ayarlamak mümkündür. Bu seçenek olarak adlandırılan **açık parola**.

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

 Mevcut belgeler ve sahip çalışma kitaplarını kullanarak belge düzeyinde projeler oluşturabilir **açık parola** etkin. Visual Studio'da olan Word ve Excel belgeleri için farklı bir davranıştır **açık parola** etkin.

 Etkinleştirme hakkında bilgi için **açık parola**, Word veya Excel'deki yardımına bakın.

## <a name="behavior-of-excel-and-word"></a>Excel ve Word davranışı
 Visual Studio'da olan her bir Excel çalışma kitabını açtığınızda **açık parola** etkin Excel parolasını ister. Çözümünüzü oluşturduğunuzda belge derleme sırasında açık olduğundan, parolasını yeniden istenir.

 İlk kez açtığınızda bir Word belgesi Visual Studio'da sahip **açık parola** etkin, Word için parolayı ister. Parolanızı başarıyla girdikten sonra **açık parola** belgeden kaldırılır ve belgeyi açmayı parola artık gerekir. Çözümünüzde belgenin istiyorsanız, önce bir parola gerektirecek şekilde açılabilir, etkinleştirmelisiniz **açık parola** , son derlemeden sonra ve çözümü dağıtmadan önce.

## <a name="see-also"></a>Ayrıca bkz.
- [Belge düzeyi çözümlerde belge koruması](../vsto/document-protection-in-document-level-solutions.md)
- [Bilgi Hakları Yönetimine ve yönetilen kod uzantılarına genel bakış](../vsto/information-rights-management-and-managed-code-extensions-overview.md)
- [Nasıl yapılır: Kodun kısıtlı izinle belgelerin arkasında çalışmasına izin](../vsto/how-to-permit-code-to-run-behind-documents-with-restricted-permissions.md)
- [Office çözümleri oluşturma ve tasarlama](../vsto/designing-and-creating-office-solutions.md)
