---
title: 'Nasıl yapılır: Bir VSTO devre dışı bırakılmış eklentiyi yeniden etkinleştirme'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VST.Warning.DisabledAddIn
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- disabled add-ins
- add-ins [Office development in Visual Studio], disabled
- add-ins [Office development in Visual Studio], enabling
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 8da3d003ea156ea3182ddbb5a5fd0da3c2681304
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60095080"
---
# <a name="how-to-re-enable-a-vsto-add-in-that-has-been-disabled"></a>Nasıl yapılır: Bir VSTO devre dışı bırakılmış eklentiyi yeniden etkinleştirme
  Microsoft Office uygulamaları, beklenmedik şekilde davranmasına VSTO Add-Ins devre dışı bırakabilirsiniz. Uygulamanın VSTO eklenti yüklemez, hata ayıklamayı denediğinizde, uygulama sabit devre dışı ya da geçici olarak devre dışı bırakılmış VSTO eklenti gerekebilir.

 [!INCLUDE[appliesto_allapp](../vsto/includes/appliesto-allapp-md.md)]

## <a name="hard-disabled-vsto-add-ins"></a>Sabit özelliği devre dışı bırakılmış VSTO eklentileri
 Sabit devre dışı bırakma, uygulama beklenmedik bir şekilde kapatmak VSTO eklentisi neden olduğunda oluşabilir. Hata ayıklayıcıyı, ayrıca geliştirme bilgisayarınızda oluşabilir <xref:Microsoft.Office.Tools.AddIn.Startup> olay işleyicisinde, VSTO eklentisi yürütülüyor.

### <a name="to-re-enable-a-vsto-add-in"></a>Bir VSTO eklentisini yeniden etkinleştirmek için

1. Uygulamada, tıklayın **dosya** sekmesi.

2. Tıklayın *ApplicationName* **seçenekleri** düğmesi.

3. Kategorileri bölmesinden **eklentileri**.

4. Ayrıntılar bölmesinde, VSTO eklentisi göründüğünü doğrulayın **devre dışı uygulama eklentileri** listesi.

     **Adı** sütunu derlemenin adını belirtir ve **konumu** sütun uygulama bildiriminin tam yolu belirtir.

5. İçinde **Yönet** kutusunun **devre dışı öğeler**ve ardından **Git**.

6. VSTO eklentisi seçip tıklayın **etkinleştirme**.

7. **Kapat**'ı tıklatın.

## <a name="soft-disabled-vsto-add-ins"></a>Yazılım özelliği devre dışı bırakılmış VSTO eklentileri
 Bir VSTO eklentisi beklenmedik bir şekilde kapatmak uygulamanın neden olmayan bir hata oluşturursa, geçici olarak devre dışı bırakma ortaya çıkabilir. Sırasında işlenmeyen bir özel durum oluşturursa, bir uygulama geçici bir VSTO eklentisi devre dışı bırakabilir <xref:Microsoft.Office.Tools.AddIn.Startup> olay işleyicisi yürütüyordur.

> [!NOTE]
>  Bir yazılım özelliği devre dışı bırakılmış VSTO eklentisini yeniden etkinleştirmeniz, uygulamayı hemen VSTO eklentisi yüklemeye çalışır. Başlangıçta VSTO eklentisi geçici olarak devre dışı bırakma uygulamaya neden olan sorunu düzelttik değil, uygulama geçici VSTO eklentisi tekrar devre dışı bırakır.

### <a name="to-re-enable-a-vsto-add-in"></a>Bir VSTO eklentisini yeniden etkinleştirmek için

1. Uygulamada, tıklayın **dosya** sekmesi.

2. Tıklayın *ApplicationName* **seçenekleri** düğmesi.

3. Kategorileri bölmesinden **eklentileri**.

4. Ayrıntılar bölmesinde, VSTO eklentisi göründüğünü doğrulayın **etkin olmayan uygulama eklentileri** listesi.

     **Adı** sütunu derlemenin adını belirtir ve **konumu** sütun uygulama bildiriminin tam yolu belirtir.

5. İçinde **Yönet** kutusunun **COM eklentileri**ve ardından **Git**.

6. İçinde **COM eklentileri** devre dışı bırakılmış VSTO eklentisi yanındaki onay kutusunu iletişim kutusunda seçin.

7. **Tamam**'ı tıklatın.

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümleri oluşturun](../vsto/building-office-solutions.md)
- [Office projelerinde hata ayıklama](../vsto/debugging-office-projects.md)
- [VSTO eklentilerini programlama](../vsto/programming-vsto-add-ins.md)
