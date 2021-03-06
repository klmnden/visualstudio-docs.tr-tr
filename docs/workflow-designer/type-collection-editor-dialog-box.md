---
title: İş Akışı Tasarımcısı - tür Koleksiyonu Düzenleyicisi iletişim kutusu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- TypeCollectionEditor.UI
ms.assetid: 63cdea6b-bca2-4c06-b8b4-c8faabd40726
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 191635364c445bc3959ee2f5f63c7c72c71f171d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62433935"
---
# <a name="type-collection-editor-dialog-box"></a>Tür Koleksiyonu Düzenleyicisi İletişim Kutusu

**Editor Typu Kolekce** iletişim kutusu için bilinen türleri eklemek için kullanılan **Gönder** ve **alma** etkinlikler. Bu iletişim için genel tür bağımsız değişkeni eklemek için de kullanılır **InvokeMethod** etkinlik. İçin kullanıldığında **Gönder** ve **alma** bilinen türleri eklenecek etkinlikleri **Editor Typu Kolekce** iletişim kutusu türü eklemeleri benzersiz olmasını gerektirir. Yinelenen tür eklenir ve değişiklik tıklayarak kararlıdır **Tamam**, bir hata iletisi döndürülür. İçin kullanıldığında **InvokeMethod** genel tür bağımsız değişkenleri, eklemek için etkinlik **Editor Typu Kolekce** yinelenen türlerinin eklenmesi iletişim kutusu sağlar.

Daha fazla bilgi için [veri anlaşması bilinen türler](/dotnet/framework/wcf/feature-details/data-contract-known-types).

Aşağıdaki tabloda kullanıcı arabirimi (UI) öğelerini açıklar **türü koleksiyonu** iletişim kutusu.

|Arabirim Öğesi|Açıklama|
|-|-----------------|
|**Tür Listesi**|Eklenen veya kaldırılan türlerinin listesi.|

## <a name="to-bring-up-the-type-collection-editor-for-the-send-and-receive-activities"></a>Editor Typu Kolekce yedeklemek için Gönder getirin ve etkinlikleri almak için

1. Seçin **Gönder** veya **alma** Tasarım görünümünde etkinlik.

2. Tuşuna **F4** ortaya çıkarmak için **özellikleri** penceresi.

3. İçinde **özellikleri** penceresinde, yanındaki üç nokta düğmesini tıklatın **KnownTypes** özelliği.

## <a name="to-bring-up-the-type-collection-editor-for-the-invokemethod-activity"></a>InvokeMethod etkinliği için tür Koleksiyonu Düzenleyicisi'kurmak getirmek için

1. Seçin **InvokeMethod** Tasarım görünümünde etkinlik.

2. Tuşuna **F4** ortaya çıkarmak için **özellikleri** penceresi.

3. İçinde **özellikleri** penceresinde, yanındaki üç nokta düğmesini tıklatın **GenericTypeArguments** özelliği.