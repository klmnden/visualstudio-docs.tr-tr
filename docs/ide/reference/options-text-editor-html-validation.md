---
title: Seçenekler, metin düzenleyici, HTML (Web formları), doğrulama
ms.date: 1/15/2019
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.HTML.Validation
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d06674d476dd671f715d2f4c88bdd23852f78687
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62778485"
---
# <a name="options-text-editor-html-web-forms-validation"></a>Seçenekler, metin düzenleyici, HTML (Web formları), doğrulama

Kullanım **doğrulama** nasıl HTML düzenleyicisinin belgenizdeki HTML biçimlendirme sözdizimi denetler tercihleri ayarlamak için seçenekler sayfası. Menü çubuğunda, bu sayfaya erişmek için seçin **Araçları** > **seçenekleri**ve ardından **metin düzenleyici** > **HTML (Web Forms)**   >  **Doğrulama**.

## <a name="validation"></a>Doğrulama

- **Doğrulama şeması tespiti için doctype kullan**

   Hangi öğe, öznitelik ve büyük/küçük harf Bu şemayı geçerli şema belirler. Ayrıca IntelliSense içinde kullanılabilir olan öznitelikler ve etiketler belirler.

   Sayfanın içeriğini kullanmak için Visual Studio istiyorsanız bu seçeneği belirleyin **<! DOCTYPE >** bildirimi ve **html** şema belirlemek için öğesi. Bu seçenek ve sayfa seçerseniz bildirimi gibi sahiptir `<!DOCTYPE html>`, Visual Studio, HTML5 şemayı kullanır. Ancak, varsa **html** etiketine sahip bir **xmlns** gibi öznitelik `<html xmlns="http://www.w3.org/1999/xhtml">`, Visual Studio XHTML5 şemayı kullanır.

- **Hiçbir doctype bulunmadığındaki hedef**

   Olduğunda karşı doğrulamak için bir şema seçin hiçbir **<! DOCTYPE >** sayfasında bildirimi.

  - **Hataları göster**

     Doğrulamayı etkinleştirmek için onay kutusunu seçin. Onay kutusu seçili değilse, doğrulama hataları Düzenleyici işaretlemiyor.

     Bir onay kutularını doğrulama işaretlemek için düzenleyici istediğiniz hataları tek tek tür belirterek ince ayar olanak tanır.

     > [!NOTE]
     > Bazı şemaları hataları tek tek türleri işaretle seçeneğini sunmaz. Örneğin, seçtiğiniz **XHTML 1.1** hedef şema tüm seçeneği onay kutularını devre dışı bırakılır. Bu örnekte, tüm hata türleri işaretlenir.

## <a name="see-also"></a>Ayrıca bkz.

- [Genel, Ortam, Seçenekler İletişim Kutusu](../../ide/reference/general-environment-options-dialog-box.md)