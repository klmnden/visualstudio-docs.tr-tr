---
title: .NET Framework 4/4,5 ' e geçirilen Excel veya Word projesini güncelleştir
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office projects [Office development in Visual Studio], migrating to .NET Framework 4
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 4bc211f4d30359c885b22a45910363bbadca236f
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253714"
---
# <a name="update-excel-and-word-projects-that-you-migrate-to-the-net-framework-4-or-the-net-framework-45"></a>.NET Framework 4 ' e veya .NET Framework 4,5 ' ye geçirebileceğiniz Excel ve Word projelerini güncelleştirme
  Aşağıdaki özelliklerden herhangi birini kullanan bir Excel veya Word projeniz varsa, hedef Framework [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya daha yeni olarak değiştirilirse kodunuzu değiştirmeniz gerekir:

- [GetVstoObject ve HasVstoObject yöntemleri](#GetVstoObject)

- [Belge düzeyi projelerinde oluşturulan sınıflar](#generatedclasses)

- [Belgelerde denetim Windows Forms](#winforms)

- [Word içerik denetimi olayları](#ccevents)

- [OLEObject ve OLEControl sınıfları](#ole)

- [Controls. Item (nesne) özelliği](#itemproperty)

- [CollectionBase 'den türetilen Koleksiyonlar](#collections)

  Ayrıca, [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya daha sonra `Microsoft.Office.Tools.Excel.ExcelLocale1033Attribute` yeniden hedeflenen Excel projelerinin `Microsoft.Office.Tools.Excel.ExcelLocale1033Proxy` sınıfına olan başvurularını da kaldırmanız gerekir. Visual Studio bu özniteliği veya sınıf başvurusunu sizin için kaldırmaz.

## <a name="remove-the-excellocale1033-attribute-from-excel-projects"></a>ExcelLocale1033 özniteliğini Excel projelerinden kaldırma
 , `Microsoft.Office.Tools.Excel.ExcelLocale1033Attribute` [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya üstünü hedefleyen çözümler için kullanılan Office çalışma zamanı için Visual Studio 2010 Araçları ' nın bölümünden kaldırılmıştır. [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Ve sonrasındaki ortak dil çalışma zamanı (CLR), her zaman 1033 yerel ayar kimliğini Excel nesne modeline geçirir ve bu özelliği artık bu davranışı devre dışı bırakmak için kullanamazsınız. Daha fazla bilgi için bkz. [Excel Çözümlerini Genelleştirme ve yerelleştirme](../vsto/globalization-and-localization-of-excel-solutions.md).

### <a name="to-remove-the-excellocale1033attribute"></a>ExcelLocale1033Attribute 'yi kaldırmak için

1. Visual Studio 'da proje açıkken **Çözüm Gezgini**açın.

2. **Özellikler** düğümü (için C#) veya **projem** düğümü altında (Visual Basic için), AssemblyInfo kod dosyasına çift tıklayarak kodu düzenleyici 'de açın.

    > [!NOTE]
    > Visual Basic projelerinde, AssemblyInfo kod dosyasını görmek için **Çözüm Gezgini** **tüm dosyaları göster** düğmesini tıklamalısınız.

3. Öğesini bulun `Microsoft.Office.Tools.Excel.ExcelLocale1033Attribute` ve dosyadan kaldırın ya da not edin.

    ```vb
    <Assembly: ExcelLocale1033Proxy(True)>
    ```

    ```csharp
    [assembly: ExcelLocale1033Proxy(true)]
    ```

## <a name="remove-a-reference-to-the-excellocal1033proxy-class"></a>ExcelLocal1033Proxy sınıfına bir başvuruyu kaldırma
 Microsoft Office sistem için Microsoft Visual Studio 2005 araçları kullanılarak oluşturulan projeler, <xref:Microsoft.Office.Interop.Excel.Application> `Microsoft.Office.Tools.Excel.ExcelLocale1033Proxy` sınıfını kullanarak Excel nesnesini başlatır. Bu sınıf, [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya daha sonra hedeflenen çözümler için kullanılan Office çalışma zamanı için Visual Studio 2010 Araçları ' nın bölümünden kaldırılmıştır. Bu nedenle, bu sınıfa başvuran kod satırını kaldırmanız veya bir açıklama satırı oluşturmanız gerekir.

### <a name="to-remove-the-reference-to-the-excellocal1033proxy-class"></a>ExcelLocal1033Proxy sınıfına başvuruyu kaldırmak için

1. Projeyi Visual Studio 'da açın ve **Çözüm Gezgini**açın.

2. **Çözüm Gezgini**' de, *ThisAddin.cs* (for C#) veya *ThisAddIn. vb* için kısayol menüsünü açın (Visual Basic için) ve sonra **kodu görüntüle**' yi seçin.

3. Kod düzenleyicisinde, `VSTO generated code` bölgesinde aşağıdaki kod satırını kaldırın veya yorum yapın.

    ```vb
    Me.Application = CType(Microsoft.Office.Tools.Excel.ExcelLocale1033Proxy.Wrap(GetType(Excel.Application), Me.Application), Excel.Application)

    ```

    ```csharp
    this.Application = (Excel.Application)Microsoft.Office.Tools.Excel.ExcelLocale1033Proxy.Wrap(typeof(Excel.Application), this.Application);

    ```

## <a name="GetVstoObject"></a>GetVstoObject ve HasVstoObject yöntemlerini kullanan kodu güncelleştirme
 .NET Framework 3,5 ' i `GetVstoObject` hedefleyen projelerde, veya `HasVstoObject` yöntemleri projenizdeki aşağıdaki yerel nesnelerden birinde uzantı yöntemleri olarak kullanılabilir: <xref:Microsoft.Office.Interop.Word.Document>, <xref:Microsoft.Office.Interop.Excel.Workbook>, <xref:Microsoft.Office.Interop.Excel.Worksheet>veya <xref:Microsoft.Office.Interop.Excel.ListObject>. Bu yöntemleri çağırdığınızda bir parametre geçirmeniz gerekmez. Aşağıdaki kod örneği, .NET Framework 3,5 ' i hedefleyen bir Word VSTO eklentisi içinde GetVstoObject yönteminin nasıl kullanılacağını gösterir.

```vb
Dim vstoDocument as Microsoft.Office.Tools.Word.Document = _
    Globals.ThisAddIn.Application.ActiveDocument.GetVstoObject()
```

```csharp
Microsoft.Office.Tools.Word.Document vstoDocument =
    Globals.ThisAddIn.Application.ActiveDocument.GetVstoObject();
```

 [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya sonraki bir sürümü hedefleyen projelerde, aşağıdaki yöntemlerden biriyle bu yöntemlere erişmek için kodunuzu değiştirmeniz gerekir:

- <xref:Microsoft.Office.Interop.Word.Document>Bu yöntemlere <xref:Microsoft.Office.Interop.Excel.Workbook> ,,veya<xref:Microsoft.Office.Interop.Excel.ListObject> nesnelerinde uzantı yöntemleri olarak erişmeye devam edebilirsiniz. <xref:Microsoft.Office.Interop.Excel.Worksheet> Ancak artık `Globals.Factory` özelliği tarafından döndürülen nesneyi bu yöntemlere geçirmeniz gerekir.

  ```vb
  Dim vstoDocument as Microsoft.Office.Tools.Word.Document = _
      Globals.ThisAddIn.Application.ActiveDocument.GetVstoObject(Globals.Factory)
  ```

  ```csharp
  Microsoft.Office.Tools.Word.Document vstoDocument =
      Globals.ThisAddIn.Application.ActiveDocument.GetVstoObject(Globals.Factory);
  ```

- Alternatif olarak, bu yöntemlere `Globals.Factory` özelliği tarafından döndürülen nesne üzerinde erişebilirsiniz. Bu yöntemlere bu şekilde eriştiğinizde, genişletmek istediğiniz yerel nesneyi yöntemine geçirmeniz gerekir.

  ```vb
  Dim vstoDocument as Microsoft.Office.Tools.Word.Document = _
      Globals.Factory.GetVstoObject(Globals.ThisAddIn.Application.ActiveDocument)
  ```

  ```csharp
  Microsoft.Office.Tools.Word.Document vstoDocument =
      Globals.Factory.GetVstoObject(Globals.ThisAddIn.Application.ActiveDocument);
  ```

  Daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

## <a name="generatedclasses"></a>Belge düzeyi projelerde oluşturulan sınıfların örneklerini kullanan kodu güncelleştirme
 .NET Framework 3,5 ' i hedefleyen belge düzeyi projelerde, projelerdeki oluşturulan sınıflar içinde [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]aşağıdaki sınıflardan türetilir:

- `ThisDocument`: <xref:Microsoft.Office.Tools.Word.Document>

- `ThisWorkbook`: <xref:Microsoft.Office.Tools.Excel.Workbook>

- `Sheet`*n*:<xref:Microsoft.Office.Tools.Excel.Worksheet>

- `Chart`*n*:<xref:Microsoft.Office.Tools.Excel.ChartSheet>

  [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya daha sonra hedeflenen projelerde, yukarıda [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] listelenen türler sınıflar yerine arayüzlerdir. [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya sonrasını hedefleyen projelerde oluşturulan sınıflar, [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]içindeki aşağıdaki yeni sınıflardan türetilir:

- `ThisDocument`: <xref:Microsoft.Office.Tools.Word.DocumentBase>

- `ThisWorkbook`: <xref:Microsoft.Office.Tools.Excel.WorkbookBase>

- `Sheet`*n*:<xref:Microsoft.Office.Tools.Excel.WorksheetBase>

- `Chart`*n*:<xref:Microsoft.Office.Tools.Excel.ChartSheetBase>

  Projenizdeki kod, tarafından türetilen temel sınıf olarak oluşturulan sınıflardan birinin bir örneğine başvuruyorsa, kodu değiştirmeniz gerekir.

  Örneğin, .NET Framework 3,5 ' i hedefleyen bir Excel çalışma kitabı projesinde, projenizde oluşturulan `Sheet` *n* sınıflarının örnekleri üzerinde bazı çalışmalar gerçekleştiren bir yardımcı yönteminiz olabilir.

```vb
Private Sub DoSomethingToSheet(ByVal worksheet As Microsoft.Office.Tools.Excel.Worksheet)
    ' Do something to the worksheet object.
End Sub
```

```csharp
private void DoSomethingToSheet(Microsoft.Office.Tools.Excel.Worksheet worksheet)
{
    // Do something to the worksheet object.
}
```

 Projeyi [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya sonraki bir sürümüne yeniden hedeflemeniz durumunda kodunuzda aşağıdaki değişikliklerden birini yapmalısınız:

- Projenizdeki bir `DoSomethingToSheet` nesnenin<xref:Microsoft.Office.Tools.Excel.WorksheetBase> özelliğini geçirmek için yöntemini çağıran herhangi bir <xref:Microsoft.Office.Tools.Excel.WorksheetBase.Base%2A> kodu değiştirin. Bu özellik bir <xref:Microsoft.Office.Tools.Excel.Worksheet> nesne döndürür.

    ```vb
    DoSomethingToSheet(Globals.Sheet1.Base)
    ```

    ```csharp
    DoSomethingToSheet(Globals.Sheet1.Base);
    ```

- Yöntem parametresini `DoSomethingToSheet` , bunun yerine bir <xref:Microsoft.Office.Tools.Excel.WorksheetBase> nesne beklediği şekilde değiştirin.

    ```vb
    Private Sub DoSomethingToSheet(ByVal worksheet As Microsoft.Office.Tools.Excel.WorksheetBase)
        ' Do something to the worksheet object.
    End Sub
    ```

    ```csharp
    private void DoSomethingToSheet (Microsoft.Office.Tools.Excel.WorksheetBase worksheet)
    {
        // Do something to the worksheet object.
    }
    ```

## <a name="winforms"></a>Belgelerde Windows Forms denetimleri kullanan kodu güncelleştirme
 Belge veya çalışma sayfasına Windows Forms denetimleriC#eklemek için Controls özelliğini kullanan herhangi bir kod dosyasının <xref:Microsoft.Office.Tools.Excel> en <xref:Microsoft.Office.Tools.Word> üstüne veya ad alanı için bir **using** () veya **Imports** (Visual Basic) ifadesini eklemeniz gerekir kullandığında.

 .NET Framework 3,5 ' i hedefleyen projelerde, Windows Forms denetimleri ( `AddButton` yöntemi gibi) ekleyen Yöntemler <xref:Microsoft.Office.Tools.Excel.ControlCollection> ve <xref:Microsoft.Office.Tools.Word.ControlCollection> sınıflarında tanımlanmıştır.

 [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya daha sonra hedeflenen projelerde, bu yöntemler denetimler özelliğinde kullanılabilen genişletme yöntemleridir. Bu uzantı yöntemlerini kullanmak için, yöntemlerini kullandığınız kod dosyası <xref:Microsoft.Office.Tools.Excel> veya <xref:Microsoft.Office.Tools.Word> ad alanı için bir **using** veya **Imports** bildirimine sahip olmalıdır. Bu ifade, [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya daha sonra hedeflenen yeni projelerde otomatik olarak oluşturulur. Ancak, bu ifade .NET Framework 3,5 ' i hedefleyen projelerde otomatik olarak eklenmez, bu nedenle projeyi yeniden hedeflediğinizde eklemeniz gerekir.

 Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

## <a name="ccevents"></a>Word içerik denetimi olaylarını işleyen kodu güncelleştirme
 .NET Framework 3,5 ' i hedefleyen projelerde, Word içerik denetimlerinin olayları genel <xref:System.EventHandler%601> temsilci tarafından işlenir. [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya daha sonra hedeflenen projelerde, bu olaylar diğer temsilciler tarafından işlenir.

 Aşağıdaki tabloda, Word içerik denetim olayları ve bunlarla [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya daha sonra hedeflenen projelerde ilişkili temsilciler listelenmektedir.

|Olay|[!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Ve sonraki projelerde kullanılacak temsilci|
|-----------| - |
|<xref:Microsoft.Office.Tools.Word.ContentControlBase.Added>|<xref:Microsoft.Office.Tools.Word.ContentControlAddedEventHandler>|
|<xref:Microsoft.Office.Tools.Word.ContentControlBase.ContentUpdating>|<xref:Microsoft.Office.Tools.Word.ContentControlContentUpdatingEventHandler>|
|<xref:Microsoft.Office.Tools.Word.ContentControlBase.Deleting>|<xref:Microsoft.Office.Tools.Word.ContentControlDeletingEventHandler>|
|<xref:Microsoft.Office.Tools.Word.ContentControlBase.Entering>|<xref:Microsoft.Office.Tools.Word.ContentControlEnteringEventHandler>|
|<xref:Microsoft.Office.Tools.Word.ContentControlBase.Exiting>|<xref:Microsoft.Office.Tools.Word.ContentControlExitingEventHandler>|
|<xref:Microsoft.Office.Tools.Word.ContentControlBase.StoreUpdating>|<xref:Microsoft.Office.Tools.Word.ContentControlStoreUpdatingEventHandler>|

## <a name="ole"></a>OLEObject ve OLEControl sınıfları kullanan kodu güncelleştirme
 .NET Framework 3,5 ' i hedefleyen projelerde, `Microsoft.Office.Tools.Excel.OLEObject` ve sınıflarını kullanarak bir belgeye veya çalışma sayfasına özel denetimler (örneğin, `Microsoft.Office.Tools.Word.OLEControl` Windows Forms Kullanıcı denetimleri) ekleyebilirsiniz.

 [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya daha sonra hedeflenen projelerde, bu sınıflar <xref:Microsoft.Office.Tools.Excel.ControlSite> ve <xref:Microsoft.Office.Tools.Word.ControlSite> arabirimleri ile değiştirilmiştir. `Microsoft.Office.Tools.Excel.OLEObject` Bunun yerine `Microsoft.Office.Tools.Word.OLEControl` öğesineveöğesinebaşvurankodudeğiştirmenizgerekir.<xref:Microsoft.Office.Tools.Excel.ControlSite> <xref:Microsoft.Office.Tools.Word.ControlSite> Yeni adlar dışında, bu denetimler .NET Framework 3,5 ' i hedefleyen projelerde yaptıkları gibi davranır.

 Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

## <a name="itemproperty"></a>Controls. Item (Object) özelliğini kullanan kodu güncelleştirme
 .NET Framework 3,5 ' i hedefleyen projelerde, bir belge veya çalışma sayfasının belirtilen denetime sahip olup olmadığını anlamak için Microsoft. Office. Tools. Word. Document. Controls veya `Microsoft.Office.Tools.Excel.Worksheet.Controls` Collection öğesinin Item (Object) özelliğini kullanabilirsiniz.

 [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya daha sonra hedeflenen projelerde, öğe (nesne) özelliği bu koleksiyonlardan kaldırılmıştır. Bir belge veya çalışma sayfasının belirtilen denetimi içerip içermediğini anlamak için, <xref:Microsoft.Office.Tools.Word.Document.Controls%2A> veya <xref:Microsoft.Office.Tools.Excel.Worksheet.Controls%2A> koleksiyonunun Contains (System. Object) yöntemini kullanın.

 Belge ve çalışma sayfalarının denetimler koleksiyonu hakkında daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

## <a name="collections"></a>CollectionBase 'den türetilen koleksiyonları kullanan kodu güncelleştirme
 .NET Framework 3,5 ' i hedefleyen projelerde,, [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] ve `Microsoft.Office.Tools.Word.ControlCollection`gibi <xref:System.Collections.CollectionBase> `Microsoft.Office.Tools.Excel.ControlCollection`sınıfından `Microsoft.Office.Tools.SmartTagCollection`türetilmiş çeşitli koleksiyon türleri.

 [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya daha sonra hedeflenen projelerde, bu koleksiyon türleri artık öğesinden <xref:System.Collections.CollectionBase>türetilmeyen arabirimlerdir. Bazı üyeler,, ve <xref:System.Collections.CollectionBase.Capacity%2A> <xref:System.Collections.CollectionBase.InnerList%2A>gibi bu koleksiyon türlerinde <xref:System.Collections.CollectionBase.List%2A>artık kullanılamaz.

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümlerini .NET Framework 4 veya sonraki sürümlere geçirme](../vsto/migrating-office-solutions-to-the-dotnet-framework-4-or-later.md)
- [İçerik denetimleri](../vsto/content-controls.md)
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Office Projelerindeki Nesnelere Genel erişim](../vsto/global-access-to-objects-in-office-projects.md)
