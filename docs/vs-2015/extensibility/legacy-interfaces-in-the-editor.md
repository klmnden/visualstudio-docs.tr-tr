---
title: Eski arabirimleri Düzenleyicisi'nde | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy
ms.assetid: 741d45f5-0ea3-4614-972a-8728fe054e07
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 8483068ae03c9a57fc67b528393e5d6830c3ec33
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54772649"
---
# <a name="legacy-interfaces-in-the-editor"></a>Eski arabirimleri Düzenleyicisi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio Düzenleyicisi eski arabirimlerden erişebilirsiniz. Visual Studio SDK'sı olarak da bilinen bağdaştırıcıları içerir *dolgular*, bu arabirimleri Düzenleyicisi ile etkileşim kurmak etkinleştirin. Bununla birlikte, yeni bir düzenleyici API kullanmak için eski kodunuzu güncelleştirmenizi öneririz. Kodunuzu daha iyi performans ve Windows Presentation Foundation (WPF) ve Yönetilen Genişletilebilirlik Çerçevesi (MEF) gibi yeni teknolojileri kullanabilirsiniz.  
  
## <a name="related-topics"></a>İlgili Konular  
  
|Başlık|Açıklama|  
|-----------|-----------------|  
|[Eski Kodu Düzenleyiciye Uyarlama](../extensibility/adapting-legacy-code-to-the-editor.md)|Kodunuzu yeni bir düzenleyici uyum açıklanmaktadır.|  
|[Düzenleyici Bağdaştırıcılarıyla Yeni veya Değiştirilmiş Davranış](../extensibility/new-or-changed-behavior-with-editor-adapters.md)|Düzenleyici bağdaştırıcıları davranışını Düzenleyicisi önceki sürümlerinde, farkı açıklar.|  
|[Temel Düzenleyicinin İçinde](../extensibility/inside-the-core-editor.md)|Düzenleyicinin önceki sürümlerinden farklı bileşenlerini açıklar.|  
|[Eski API'yi Kullanarak Temel Düzenleyiciyi Başlatma](../extensibility/instantiating-the-core-editor-by-using-the-legacy-api.md)|Çekirdek Düzenleyici örneği oluşturmak için eski API'sini kullanmayı açıklar.|  
|[Düzenleyici Fabrikaları](../extensibility/editor-factories.md)|Düzenleyici fabrikaları eski API ile kullanmayı açıklar.|  
|[Nasıl yapılır: Register Editor dosya türleri](../extensibility/how-to-register-editor-file-types.md)|Bir dosya adı uzantısı düzenleyiciniz için bağlantı açıklanmaktadır.|  
|[İzlenecek yol: Çekirdek düzenleyici oluşturma ve bir düzenleyici dosya türü kaydetme](../extensibility/walkthrough-creating-a-core-editor-and-registering-an-editor-file-type.md)|Çekirdek düzenleyici oluşturma ve bir dosya adı uzantısı bağlantısına açıklanmaktadır.|  
|[Nasıl yapılır: Düzenleyiciler için bağlam sağlayın](../extensibility/how-to-provide-context-for-editors.md)|Bağlam düzenleyiciniz için sağlamayı açıklar.|  
|[Dil Hizmetleri ve Temel Düzenleyici](../extensibility/language-services-and-the-core-editor.md)|Dil hizmeti ve düzenleyici arasındaki etkileşimler açıklanmaktadır.|  
|[Eski API'yi Kullanarak Metin Arabelleğine Erişme](../extensibility/accessing-the-text-buffer-by-using-the-legacy-api.md)|Eski API'yi kullanarak metin arabelleğini erişimi açıklar.|  
|[Eski API'yi Kullanarak Metin Görünümüne Erişme](../extensibility/accessing-thetext-view-by-using-the-legacy-api.md)|Eski API'yi kullanarak metin görünümünü erişimi açıklar.|  
|[Eski API'yi Kullanarak Kod Penceresini Özelleştirme](../extensibility/customizing-code-windows-by-using-the-legacy-api.md)|Kodu windows eski API'yi kullanarak özelleştirmek nasıl açıklar.|  
|[Eski API'yi Kullanarak Metin Katmanlarına Erişme](../extensibility/accessing-text-layers-by-using-the-legacy-api.md)|Eski API'yi kullanarak metin farklı katmanlara erişimi açıklar.|  
|[Eski API ile Metin İşaretçilerini Kullanma](../extensibility/using-text-markers-with-the-legacy-api.md)|Metin işaretçileri eski API'sini kullanarak ekleme işlemi açıklanmaktadır.|  
|[Eski API'yi Kullanarak Düzenleyici Denetimlerini ve Menüleri Özelleştirme](../extensibility/customizing-editor-controls-and-menus-by-using-the-legacy-api.md)|Düzenleyici denetimleri eski API'yi kullanarak özelleştirmek nasıl açıklar.|  
|[Eski API'yi Kullanarak Geri Alma ve Yineleme](../extensibility/managing-undo-and-redo-by-using-the-legacy-api.md)|Geri alma yönetmek ve eski API'yi kullanarak yineleme açıklanmaktadır.|  
|[Nasıl yapılır: Uygulama Bul ve Değiştir mekanizması](../extensibility/how-to-implement-the-find-and-replace-mechanism.md)|Bul yönetmek ve eski API'yi kullanarak değiştirin açıklanmaktadır.|  
|[Nasıl yapılır: Dosya değişiklik bildirimlerini gösterme](../extensibility/how-to-suppress-file-change-notifications.md)|Eski API'yi kullanarak dosya değişiklik bildirimlerini bastır açıklanmaktadır.|  
|[Özel Düzenleyiciler ve Tasarımcılar Oluşturma](../extensibility/creating-custom-editors-and-designers.md)|Özel düzenleyiciler ve tasarımcılar oluşturma açıklanır.|  
|[Eski Dil Hizmeti Geliştirme](../extensibility/internals/developing-a-legacy-language-service.md)|Özelleştirme olanağı sağlayan özellikleri ilgili belgelerin bağlantılarını sağlar [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] dil hizmeti için destek ekleyerek çekirdek Düzenleyici.|  
|[Yazı Tiplerini ve Renkleri Kullanma](../extensibility/using-fonts-and-colors.md)|Yazı tipleri ve renkler eski arabirimleri ile kullanmayı açıklar.|
