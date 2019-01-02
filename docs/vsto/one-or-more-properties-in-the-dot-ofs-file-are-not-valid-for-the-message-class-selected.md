---
title: .ofs dosyasındaki bir veya daha fazla özellik seçilen ileti sınıfı için geçerli değil
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VSTO.NewFormRegionWizard.OFSPropertyError
dev_langs:
- VB
- CSharp
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 6d6469c48def1a5d21eb160cb4ad6d14704bc101
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53909131"
---
# <a name="one-or-more-properties-in-the-ofs-file-are-not-valid-for-the-message-class-selected"></a>.ofs dosyasındaki bir veya daha fazla özellik seçilen ileti sınıfı için geçerli değil
  Outlook'ta tasarlanan form bölgesini içeri aktardığınızda, bu hata görüntülenir, ancak bir veya daha fazla form bölgesinin alanlarda son sayfasında, seçtiğiniz ileti sınıfları ile uyumlu olmayan **Yeni Form bölgesi** Sihirbazı.  

Örneğin, seçtiğiniz **görev (IPM. Görev)** son sayfasında **Yeni Form bölgesi** Sihirbazı. Form bölgesi varsa bir **iş adresi** alan, bir görev bir iş adresi olmadığı için bu hatayı alırsınız. Bu nedenle, **iş adresi** alan ile uyumlu değil `IPM.Task` ileti sınıfı.  
  
 Seçtiğiniz **görev (IPM. Görev)** son sayfasında **Yeni Form bölgesi** Sihirbazı. Form bölgesi varsa bir **iş adresi** alan, bir görev bir iş adresi olmadığı için bu hatayı alırsınız. Bu nedenle, **iş adresi** alan ile uyumlu değil `IPM.Task` ileti sınıfı.  
  
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Son sayfasında **Yeni Form bölgesi** Sihirbazı, form bölgesi ile sekmesindeki alanları ile uyumlu bir ileti sınıfı seçin.  
  
-   Outlook Form tasarımcısında ileti sınıfları ile uyumlu olmayan alanlarını kaldırın. Son sayfasında, seçin planladığınız alanları kaldırma **Yeni Form bölgesi** Sihirbazı.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [İzlenecek yol: Outlook'ta tasarlanan form bölgesini içeri aktarma](../vsto/walkthrough-importing-a-form-region-that-is-designed-in-outlook.md)  
