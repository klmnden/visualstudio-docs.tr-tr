---
title: Görüntü Özellikleri kılavuz | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- properties [Visual Studio SDK], grid
ms.assetid: 318e41b0-acf5-4842-b85e-421c9d5927c5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 83c443dba0e77809ec9a2d4093f6581b260a2d2d
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/18/2019
ms.locfileid: "56335122"
---
# <a name="properties-display-grid"></a>Özellikler görüntü Kılavuzu

**Özellikleri** penceresi bir grid'in içindeki alanları görüntüler. Sol sütunda, özellik adlarını içerir. Sağ sütun, özellik değerlerini içerir.

## <a name="work-with-the-grid"></a>Kılavuz ile çalışma

İki sütunlu bir liste, tasarım zamanı ve geçerli ayarlarının değiştirilebilir bağımsız yapılandırma özelliklerini gösterir. Tüm özellikleri gösterilmez unutmayın. Bir özellik ayarlanabilir gizli olarak, örneğin, uygulama tarafından <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing.HideProperty%2A> yöntemi. Özellikle, alt özelliklerine sahip Gizle özellikleri:

1. Ayarlama `pfDisplay` parametresinde <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing.DisplayChildProperties%2A> için `FALSE`.

2. Ayarlama `pfHide` parametresinde <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing.HideProperty%2A> için `TRUE`.

Anında iletme bilgilerine **özellikleri** penceresi, IDE'nin kullanan <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer>. <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer> VSPackage'ları tarafından seçilebilir nesneleriyle görüntülenmesi için ilgili özellikleri içeren her bir pencere için çağrılır **özellikleri** penceresi. **Çözüm Gezgini**'s uygulaması <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer> çağrıları `GetProperty` kullanarak [__VSHPROPID. VSHPROPID_BrowseObject](<xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID.VSHPROPID_BrowseObject>) hiyerarşideki göz nesneleri almak için proje hiyerarşinizdeki.

VSPackage'ı desteklemiyorsa [__VSHPROPID. VSHPROPID_BrowseObject](<xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID.VSHPROPID_BrowseObject>), IDE kullanmayı dener <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.GetProperty%2A> değeri kullanarak [__VSHPROPID. VSHPROPID_SelContainer](<xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID.VSHPROPID_SelContainer>) hiyerarşi öğesi veya öğelerini sağlayın.

VSPackage'ı oluşturmak için ihtiyacınız olmayan projenize <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer> pencere IDE tarafından sağlanan paket, onu uyguladığından (örneğin, **Çözüm Gezgini**) oluşturur <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer> kendi adına.

<xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer> IDE tarafından çağrılan üç yöntemi oluşur:

- <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer.CountObjects%2A> Görüntülenecek seçili nesne sayısını içeren **özellikleri** penceresi.

- <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer.GetObjects%2A> döndürür `IDispatch` görüntülenmesi için seçilen nesneleri **özellikleri** penceresi.

- <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer.SelectObjects%2A> tarafından döndürülen nesnelerden herhangi birini mümkün kılar <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer.GetObjects%2A> kullanıcı tarafından seçilmelidir. Bu, kullanıcı arabiriminde görüntülenen seçim görsel olarak güncelleştirilecek VSPackage sağlar.

**Özellikleri** penceresi ayıklar bilgilerinden `IDispatch` konumundayken özelliklerini almak için nesneleri. Özellik tarayıcısını kullanır `IDispatch` nesnenin hangi özelliklerin sormak sorgulayarak desteklediği `ITypeInfo`, öğesinden alınan `IDispatch::GetTypeInfo`. Tarayıcı ardından doldurmak için bu değerleri kullanır **özellikleri** penceresinde ve özellikler için değerleri kılavuzunda görüntülenen Değiştir. Özellikleri bilgileri, nesne içinde saklanır.

Döndürülen nesneleri desteklemediğinden `IDispatch`, çağırana nesnenin adı gibi bilgileri ya da çağırarak elde edebileceğiniz `IDispatch::Invoke` veya `ITypeInfo::Invoke` istenen bilgileri temsil eden bir tanımlayıcıyla tanımlanmış gönderme (DISPID). Kullanıcı tanımlı tanımlayıcıları ile çakışmadığından emin olmak için bildirilen DISPID değeri negatiftir.

**Özellikleri** penceresi farklı alanların özniteliklerini seçilen bir nesne belirli özelliklerini bağlı olarak görüntüler. Bu alanları düzenleme kutuları, açılan listeler ve özel Düzenleyici iletişim kutularına bağlantılar içerir.

- Numaralandırılmış bir listede yer alan değerleri tarafından alınır bir <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer.GetObjects%2A> için sorgu `IDispatch`. Bir liste alınan değerleri özellik kılavuzunda alan adına çift tıklayarak ya da değer tıklayarak ve aşağı açılan listeden yeni bir değer seçerek değiştirilebilir. Numaralandırılmış listelere ayarlarından önceden tanımlanmış özellikler için kullanılabilir seçenekleri özellikler listesinde bulunan bir özellik adını çift geçiş yapar. Önceden tanımlanmış özellikler doğru/yanlış gibi yalnızca iki seçenek için seçenekler arasında geçiş yapmak için özellik adına çift tıklayın.

- Varsa <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing.HasDefaultValue%2A> olduğu `false`, gösteren değeri değiştirildi, değeri kalın metin olarak görüntülenir. <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing.CanResetPropertyValue%2A> özgün değerine sıfırlanabilir değeri belirlemek için kullanılır. Bu nedenle, değer sağ tıklayıp seçerek varsayılan olarak değiştirebileceğiniz durumlarda **sıfırlama** görüntülenen menüden. Aksi takdirde, değeri varsayılan olarak el ile değiştirmeniz gerekir. <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing> Ayrıca yerelleştirmek ve tasarım sırasında görüntülenen özelliklerin adları gizleme olanak tanır, ancak özellik adları çalışma zamanı sırasında etkilemez.

- Üç nokta (…) düğmesine tıklayarak özellik değerlerini (Renk Seçici veya yazı tipi listesi gibi), kullanıcının seçebileceği listesini görüntüler. <xref:Microsoft.VisualStudio.Shell.Interop.IProvidePropertyBuilder> Bu değerleri sağlar.

## <a name="see-also"></a>Ayrıca bkz.

- [Özellikleri genişletme](../../extensibility/internals/extending-properties.md)