---
title: Seçenekler, Windows Form Tasarımcısı, veri UI özelleştirmesi
ms.date: 08/09/2019
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.WindowsFormsDesigner.Data_UI_Customization
helpviewer_keywords:
- Data UI customization options
- Options dialog box, Windows Forms Designer, Data UI Customization
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: ca68a944002d743c6f3d2f89b309b8b77c5dfdb3
ms.sourcegitcommit: 6b0503ed8d25454d6e39a8e606910b3fa58cf1d2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2019
ms.locfileid: "68984210"
---
# <a name="options-dialog-box-windows-forms-designer--data-ui-customization"></a>Seçenekler iletişim kutusu: Windows Form Tasarımcısı > veri ARABIRIMI özelleştirmesi

Bu iletişim kutusu, veri kaynakları penceresinde öğelerin kullanılabilir denetimleri listesinde hangi denetimlerin göründüğünü tanımlar. Açmak için **Araçlar** > **Seçenekler**' i seçin ve ardından **Windows Form Tasarımcısı** > **veri UI özelleştirmesi**' nı seçin.

Bir Windows Forms uygulamasındaki form üzerine sürüklemeden önce veri kaynakları penceresinde bir öğeden denetim seçebilirsiniz. Kullanılabilir denetimler öğenin veri türüne göre belirlenir. Her veri türü, varsayılan bir denetim dahil olmak üzere, bu iletişim kutusunda tanımlanan geçerli ilişkili denetimlerin bir listesini içerir. Bir öğeyi veri kaynakları penceresinden bir denetim seçmeden bir form üzerine sürüklediğinizde, seçili öğenin veri türü için varsayılan denetim forma eklenir.

Her veri türü için kullanılabilir denetimlerin onay kutularını seçip temizleyerek ilişkili denetimlerin listesini özelleştirin. Listeye bir denetim eklemek için, araç kutusuna <xref:System.ComponentModel.DefaultBindingPropertyAttribute> ya <xref:System.ComponentModel.ComplexBindingPropertiesAttribute> da veri bağlama özniteliğini uygulayan bir denetim ekleyin. Daha sonra Denetim, veri türü için denetim listesinde görünür. Daha fazla bilgi için [nasıl yapılır: Veri Kaynakları penceresine](../..//data-tools/add-custom-controls-to-the-data-sources-window.md)özel denetimler ekleyin.

## <a name="data-type"></a>Veri türü

Denetimleri ilişkilendirdiğiniz türlerin bir listesini görüntüler. Tablolar `[List]` veri türü olarak temsil edilir. Sütunlar, temel alınan veri deposundaki sütunun gerçek veri türü olarak gösterilir.

## <a name="associated-controls"></a>İlişkili denetimler

Seçili veri türüyle ilişkili denetimlerin listesini görüntüler. İlişkilendirmek veya ilişkiyi kaldırmak için denetimin yanındaki onay kutusunu işaretleyin veya temizleyin. Seçili denetimler, ilişkili veri türüne bağlanan bir veritabanı sütunu için veri kaynakları penceresinde görünür.

## <a name="set-default"></a>Varsayılanı ayarla

Seçili denetim türünü seçili veri türü için varsayılan değer olacak şekilde atar. Varsayılan denetim, veri kaynakları penceresinde bir veritabanı sütunu için kısayol menüsünde ilk seçim olarak görünür. Bir öğeyi veri kaynakları penceresinden bir denetim seçmeden bir form üzerine sürüklediğinizde, seçili öğenin veri türü için varsayılan denetim forma eklenir.

Bir veri türü için yalnızca bir denetim türü varsayılan olarak atanabilir.

## <a name="clear-default"></a>Varsayılanı Temizle

Bir denetimin atamasını seçili veri türü için varsayılan olarak kaldırır. Seçili veri türü için varsayılan değer yoksa, `[None]` bu türdeki bir veritabanı sütunu için kısayol menüsünde ilk seçim olarak görünür.