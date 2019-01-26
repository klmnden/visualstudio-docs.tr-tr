---
title: Visual Studio'da EditorConfig desteklemek için bir dil hizmeti genişletme | Microsoft Docs
ms.date: 11/22/2017
ms.topic: conceptual
helpviewer_keywords:
- editorconfig [extensibility]
- editorconfig, supporting in a language service
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 047545f3b2ab3c08b84fbb4af95a46c44655f1cd
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54981313"
---
# <a name="supporting-editorconfig-for-your-language-service"></a>Dil hizmetiniz için Editorconfig'i destekleme

[EditorConfig](http://editorconfig.org/) dosyaları, proje başına temelinde girinti boyutu gibi ortak metin düzenleyici seçenekleri tanımlamak etkinleştirin. EditorConfig dosyaları için Visual Studio desteği hakkında daha fazla bilgi için bkz: [EditorConfig kullanarak taşınabilir bir düzenleyici ayarları oluşturma](../ide/create-portable-custom-editor-options.md).

Çoğu durumda, bir Visual Studio dil hizmeti uyguladığınızda hiçbir ek iş EditorConfig Evrensel özellikleri desteklemek için gereklidir. Çekirdek düzenleyici otomatik olarak bulur ve kullanıcıların dosyaları açmak ve uygun metin arabelleği ve görünüm seçeneklerini ayarlar .editorconfig dosyasındaki okur. Ancak, sekmeler ve boşluk gibi düzenlemeler için genel ayarları kullanmak yerine bir ilgili bağlamsal metni Görüntüle seçeneği kullanmak için bazı dil Hizmetleri iyileştirilmiş. Bu durumlarda, dil hizmeti EditorConfig dosyaları destekleyecek şekilde güncelleştirilmesi gerekir.

Genel bir değiştirerek EditorConfig dosyaları desteklemek için bir dil hizmeti güncelleştirmek için gereken değişiklikleri şunlardır _dile özgü_ seçeneğini bir _bağlamsal_ seçeneği:

## <a name="indent-style"></a>Stil Girintile

Dile özgü seçenekleri | Bağlamsal seçenekleri
-------|--------
Microsoft.VisualStudio.TextManager.Interop.LANGPREFERENCES.fInsertTabs<br/>Microsoft.VisualStudio.Package.LanguagePreferences.InsertTabs|!textBufferOptions.GetOptionValue(DefaultOptions.ConvertTabsToSpacesOptionId)<br/>!textView.Options.GetOptionValue(DefaultOptions.ConvertTabsToSpacesOptionId)

## <a name="indent-size"></a>Girinti boyutu

Dile özgü seçenekleri | Bağlamsal seçenekleri
-------|--------
Microsoft.VisualStudio.TextManager.Interop.LANGPREFERENCES.uIndentSize<br/>Microsoft.VisualStudio.Package.LanguagePreferences.InsertTabs.IndentSize|textBufferOptions.GetOptionValue(DefaultOptions.IndentSizeOptionId)<br/>textView.Options.GetOptionValue(DefaultOptions.IndentSizeOptionId)

## <a name="tab-size"></a>Sekme boyutu

Dile özgü seçenekleri | Bağlamsal seçenekleri
-------|--------
Microsoft.VisualStudio.TextManager.Interop.LANGPREFERENCES.uTabSize<br/>Microsoft.VisualStudio.Package.LanguagePreferences.InsertTabs.TabSize|textBufferOptions.GetOptionValue(DefaultOptions.TabSizeOptionId)<br/>textView.Options.GetOptionValue(DefaultOptions.TabSizeOptionId)

## <a name="see-also"></a>Ayrıca bkz.

[EditorConfig kullanarak taşınabilir bir düzenleyici ayarları oluşturma](../ide/create-portable-custom-editor-options.md)  
[Düzenleyici ve dil hizmetlerini genişletme](../extensibility/extending-the-editor-and-language-services.md)