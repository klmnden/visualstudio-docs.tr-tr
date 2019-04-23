---
title: İçinde çekirdek Düzenleyicisi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - core editor
ms.assetid: 8265f31c-c45b-4858-882c-6d9f1e3b9083
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a188116b09b846e81023c239d64d6386c7f2c6ae
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60086526"
---
# <a name="inside-the-core-editor"></a>Çekirdek Düzenleyicisi içinde
[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Çekirdek Düzenleyicisi değiştirebilir ve sorgu metin tabanlı bilgiler sağlayan çeşitli bileşenleri kümesidir. Eski API'yi kullanarak çekirdek Düzenleyici özelleştirdiyseniz, düzenleyici bağdaştırıcıları fabrikamserverpool'a yönlendirilebilir bu özelleştirmeler kullanmaya devam edebilir. Bu, ancak yeni bir düzenleyici API özelleştirmelerinizi uyum önerilir.

 Çekirdek Düzenleyici önemli bazı yönleri şunlardır:

- Metin arabelleği

- Metin görünümü

- Kod penceresi

- Metin işaretçileri

- Metin Yöneticisi

- Dil Hizmetleri ile tümleştirme

## <a name="in-this-section"></a>Bu bölümde
- [Eski API'yi kullanarak çekirdek Düzenleyici örneği](../extensibility/instantiating-the-core-editor-by-using-the-legacy-api.md) nasıl kullanılacağını hakkında adım adım yönergeler sağlar <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> Düzenleyici çekirdek örneğini oluşturmak için.

- [Eski API'yi kullanarak metin arabelleğini erişim](../extensibility/accessing-the-text-buffer-by-using-the-legacy-api.md) çekirdek Düzenleyici içindeki metin arabelleği rolü açıklar, arabellek erişmek için kullanılır ve metin arabelleği nesne tarafından uygulanan arabirimler listesini sağlayan ilişkili sistemleri açıklanmaktadır <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>.

- [Metin arabelleği olayları eski API'sindeki](../extensibility/text-buffer-events-in-the-legacy-api.md) metin arabelleği olay bildirimi için kullanılan arabirimlerin listesini sağlar.

- [Nasıl yapılır: Metin arabelleği olayları eski API'si ile kaydolun](../extensibility/how-to-register-for-text-buffer-events-with-the-legacy-api.md) metin arabelleği olayları için öneri açıklar.

- [Genel ayarlar izlemek için metin Yöneticisi'ni kullanın](../extensibility/using-the-text-manager-to-monitor-global-settings.md) metin Yöneticisi ile çekirdek Düzenleyicisi bileşenleri genel tercih bilgi paylaşımı için nasıl kullanıldığını ve metin Yöneticisi olaylarını bildirim almak nasıl ele alır.

- [Eski API'yi kullanarak erişimcisinde görünümü erişim](../extensibility/accessing-thetext-view-by-using-the-legacy-api.md) çekirdek Düzenleyici içindeki metin görünümün rolü açıklar ve tarafından uygulanan arabirimler listeler <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView> nesne.

- [Eski API'sini kullanarak kod windows özelleştirme](../extensibility/customizing-code-windows-by-using-the-legacy-api.md) nasıl bir kod penceresinde metin görünümünü içine almak için kullanılan, kod penceresi Yöneticisi kod penceresine süslemeleri sağlamak için nasıl kullanıldığını açıklar ve bildirim yeni bir görünüm sağlar hakkında bilgi sağlar .

- [Eski API'yi kullanarak görünüm ayarlarını değiştirme](../extensibility/changing-view-settings-by-using-the-legacy-api.md) görünümü ayarları zorlamak ve zorunlu ayarlarını kaldırmak hakkında adım adım yönergeler sağlar.

- [Dil Hizmetleri ve çekirdek düzenleyici](../extensibility/language-services-and-the-core-editor.md) denetimi kod süslemeleri için bir dil hizmeti örneğinin açıklar.

## <a name="related-sections"></a>İlgili bölümler
- [İzlenecek yol: Çekirdek düzenleyici oluşturma ve bir düzenleyici dosya türü kaydetme](../extensibility/walkthrough-creating-a-core-editor-and-registering-an-editor-file-type.md) çekirdek Düzenleyici yönetilen koddan başlama hakkında adım adım yönergeler sağlar.

- [Aşağı açılan çubuğu](../extensibility/drop-down-bar.md) kod penceresinde açılan çubuğunun nasıl kullanıldığını açıklar ve bir açılan çubuğu uygularken kullanılan arabirimler açıklanmaktadır.

- [Metin işaretçileri eski API'si ile kullanma](../extensibility/using-text-markers-with-the-legacy-api.md) metin işaretçileri ve çekirdek Düzenleyicisi'nde nasıl kullanılacağını kavramını açıklar ve erişmek ve metin işaretçileri yönetmek için kullanılan arabirimlerini listeler.

- [Nasıl yapılır: Standart metin işaretçileri ekleme](../extensibility/how-to-add-standard-text-markers.md) metin işaretçisi oluşturmak ve özel komut için kısayol menüsü ekleme hakkında adım adım yönergeler sağlar.

- [Nasıl yapılır: Özel metin işaretçileri oluşturma](../extensibility/how-to-create-custom-text-markers.md) ve işaret türü bir hizmet olarak sağlamak bir özel metin işaretçisi oluşturma hakkında adım adım yönergeler sağlar.