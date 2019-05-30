---
title: Kaydetmeden önce verilere bağlı denetimler üzerinde işlem içi düzenlemeler yürütme
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- committing edited records
- data-bound controls, in-process edits
- DataBinding class, committing edited records
- hierarchical update, committing edited records
- BindingSource class, committing edited records
- EndEdit method
ms.assetid: 61af4798-eef7-468c-b229-5e1497febb2f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 129ab5be6264f566de284b2736664c8c0d8c07d7
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66261833"
---
# <a name="commit-in-process-edits-on-data-bound-controls-before-saving-data"></a>Verileri kaydetmeden önce verilere bağlı denetimler üzerinde işlem içi düzenlemeler yürütme

Verilere bağlı denetimler değerleri düzenlerken, kullanıcılar güncelleştirilmiş değeri denetimin bağlı olduğu temel alınan veri kaynağına kaydetmek için geçerli kayıt devre dışı gitmeniz gerekir. Öğeleri sürüklediğinizde [veri kaynakları penceresi](add-new-data-sources.md) formunuza, koda bıraktığınız ilk öğeyi oluşturur **Kaydet** düğme tıklatma olayını, <xref:System.Windows.Forms.BindingNavigator>. Bu kod <xref:System.Windows.Forms.BindingSource.EndEdit%2A> yöntemi <xref:System.Windows.Forms.BindingSource>. Bu nedenle, çağrı <xref:System.Windows.Forms.BindingSource.EndEdit%2A> yöntemi yalnızca ilk oluşturulduğunda <xref:System.Windows.Forms.BindingSource> formuna eklenir.

<xref:System.Windows.Forms.BindingSource.EndEdit%2A> Çağrı işleminde şu anda düzenlenmekte olan herhangi bir veriye bağlı denetim değişiklikleri kaydeder. Odak ve bu nedenle, bir veri bağlı denetim hala varsa tıklayın **Kaydet** denetim kaydedilir, gerçek kaydetme önce tüm bekleyen düzenlemeler düğmesine ( `TableAdapterManager.UpdateAll` yöntemi).

Bir kullanıcı kayıt işleminin bir parçası olarak değişikliklerin, taahhüt vermek zorunda kalmadan verileri kaydetmeyi denediğinde olsa bile, uygulamanızın otomatik olarak değişiklikleri yapılandırabilirsiniz işlem.

> [!NOTE]
> Tasarımcı ekler `BindingSource.EndEdit` kod yalnızca ilk öğe için bir forma bırakılan. Bu nedenle, bir çağırmak için kod satırı eklemeniz gerekir <xref:System.Windows.Forms.BindingSource.EndEdit%2A> yöntemi her <xref:System.Windows.Forms.BindingSource> form üzerinde. Bir satır kod çağırmak için el ile ekleyebilirsiniz <xref:System.Windows.Forms.BindingSource.EndEdit%2A> yöntemi her <xref:System.Windows.Forms.BindingSource>. Alternatif olarak, ekleme `EndEditOnAllBindingSources` forma yöntemi ve kaydetmeyi gerçekleştirmeden önce onu çağırabilir.

Aşağıdaki kod bir [LINQ (dil ile tümleşik sorgu)](/dotnet/csharp/linq/) tüm yapılacağını sorgu <xref:System.Windows.Forms.BindingSource> bileşenleri ve çağrı <xref:System.Windows.Forms.BindingSource.EndEdit%2A> yöntemi her <xref:System.Windows.Forms.BindingSource> bir form üzerinde.

## <a name="to-call-endedit-for-all-bindingsource-components-on-a-form"></a>Formdaki tüm BindingSource bileşenlerin EndEdit çağırmak için

1. İçeren formuna aşağıdaki kodu ekleyin <xref:System.Windows.Forms.BindingSource> bileşenleri.

     [!code-csharp[VSProDataOrcasEndEditOnAll#1](../data-tools/codesnippet/CSharp/commit-in-process-edits-on-data-bound-controls-before-saving-data_1.cs)]
     [!code-vb[VSProDataOrcasEndEditOnAll#1](../data-tools/codesnippet/VisualBasic/commit-in-process-edits-on-data-bound-controls-before-saving-data_1.vb)]

2. Kod form verilerini kaydetmek için tüm çağrıları hemen önce aşağıdaki satırı ekleyin ( `TableAdapterManager.UpdateAll()` yöntemi):

     [!code-csharp[VSProDataOrcasEndEditOnAll#2](../data-tools/codesnippet/CSharp/commit-in-process-edits-on-data-bound-controls-before-saving-data_2.cs)]
     [!code-vb[VSProDataOrcasEndEditOnAll#2](../data-tools/codesnippet/VisualBasic/commit-in-process-edits-on-data-bound-controls-before-saving-data_2.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da verilere Windows Forms denetimleri bağlama](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)
- [Hiyerarşik güncelleştirme](../data-tools/hierarchical-update.md)