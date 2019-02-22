---
title: 'Nasıl yapılır: Program aracılığıyla belgeleri ve belge parçalarını koruma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- document protection
- documents [Office development in Visual Studio], document protection
- Word documents, protection
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 2c7d284e116f72b5f1c19017cf234ea42832c202
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56613420"
---
# <a name="how-to-programmatically-protect-documents-and-parts-of-documents"></a>Nasıl yapılır: Program aracılığıyla belgeleri ve belge parçalarını koruma
  Kullanıcılar belgeyi düzenlemeler yapmasını önlemek için Microsoft Office Word belgeleri koruma ekleyebilirsiniz.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

 Böylece belirtilen kullanıcılar yalnızca belgenin alanları düzenleyebilir, belgedeki belirli alanların özel durumlar olarak işaretleyebilirsiniz. Örneğin, belirli bir yer işareti hariç tüm belgeyi korumak isteyebilirsiniz. Böylece parola alışık oldukları sürece kullanıcılar Belge korumasını kaldıramaz, isteğe bağlı olarak bir parola ekleyebilirsiniz.

> [!NOTE]
>  Aşağıdaki örnek, parola koruması kullanmaz; Ancak, bir parola belge koruması eklerken göz önünde bulundurmak isteyebilirsiniz. Daha fazla bilgi için belge koruyucu örneğine bakın [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md).

 İçerik denetimleri, belge bölümlerini koruma için de kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: İçerik denetimlerini kullanarak belge bölümlerini koruma](../vsto/how-to-protect-parts-of-documents-by-using-content-controls.md).

## <a name="protect-a-document-that-is-part-of-a-document-level-customization"></a>Belge düzeyi özelleştirmesi parçası olan bir belgeyi koru

### <a name="to-protect-a-document-that-is-part-of-a-document-level-customization"></a>Belge düzeyi özelleştirmesi parçası olan bir belgeyi korumak için

1.  Çağrı <xref:Microsoft.Office.Tools.Word.Document.Protect%2A> yöntemi `ThisDocument` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomation#111](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#111)]
     [!code-csharp[Trin_VstcoreWordAutomation#111](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#111)]

### <a name="to-exclude-a-bookmark-control-from-document-protection"></a>Bir yer işareti denetimi belge korumadan dışlamak için

1.  Kullanarak tüm belgeyi korumak <xref:Microsoft.Office.Tools.Word.Document.Protect%2A> yöntemi.

     [!code-vb[Trin_VstcoreWordAutomation#111](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#111)]
     [!code-csharp[Trin_VstcoreWordAutomation#111](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#111)]

2.  Dışlama `Bookmark1` belge koruması.

     [!code-vb[Trin_VstcoreWordAutomation#112](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#112)]
     [!code-csharp[Trin_VstcoreWordAutomation#112](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#112)]

### <a name="compile-the-code"></a>Kod derleme
 Bu kod örnekleri kullanmak için onlardan çalıştırın `ThisDocument` projenizdeki sınıfı. Bu kod örnekleri, varsayılır <xref:Microsoft.Office.Tools.Word.Bookmark> adlı Denetim `Bookmark1` bu kodu göründüğü belgesi.

## <a name="protect-a-document-by-using-a-vsto-add-in"></a>Bir VSTO eklentisi kullanarak belgeyi koruma

### <a name="to-protect-a-document-by-using-an-application-level-vsto-add-in"></a>Bir uygulama düzeyinde VSTO eklentisi kullanarak bir belgeyi korumak için

1.  Çağrı <xref:Microsoft.Office.Interop.Word._Document.Protect%2A> yöntemi <xref:Microsoft.Office.Interop.Word.Document> korumak istediğiniz.

     Aşağıdaki kod örneği, etkin belgeyi korur. Bu kod örneği kullanmak için çalıştırın `ThisAddIn` projenizdeki sınıfı.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#111](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#111)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#111](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#111)]

## <a name="see-also"></a>Ayrıca bkz.
- [Belge düzeyi çözümlerde belge koruması](../vsto/document-protection-in-document-level-solutions.md)
- [Office belgelerinde parola koruması](../vsto/password-protection-on-office-documents.md)
- [Nasıl yapılır: Kodun kısıtlı izinle belgelerin arkasında çalışmasına izin](../vsto/how-to-permit-code-to-run-behind-documents-with-restricted-permissions.md)
- [Nasıl yapılır: Word belgelerine yer işareti denetimi ekleme](../vsto/how-to-add-bookmark-controls-to-word-documents.md)
- [Office çözümleri oluşturma ve tasarlama](../vsto/designing-and-creating-office-solutions.md)
