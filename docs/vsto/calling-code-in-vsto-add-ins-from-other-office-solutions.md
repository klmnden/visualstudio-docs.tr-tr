---
title: Diğer Office çözümlerindeki VSTO eklentilerindeki kodu çağırma
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- VBA [Office development in Visual Studio], calling code in application-level add-ins
- application-level add-ins [Office development in Visual Studio], calling code from other solutions
- calling add-in code
- add-ins [Office development in Visual Studio], calling code from other solutions
- interoperability [Office development in Visual Studio]
- calling code from VBA
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 584406098f058c17b3dd215dda9c8c4e9498cf46
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255322"
---
# <a name="call-code-in-vsto-add-ins-from-other-office-solutions"></a>Diğer Office çözümlerindeki VSTO eklentilerindeki kodu çağırma
  VSTO eklentiinizdeki bir nesneyi diğer Microsoft Office çözümleri de dahil olmak üzere diğer çözümlere kullanıma sunabilirsiniz. Bu, VSTO eklentisinin diğer çözümlerin kullanmasını sağlamak istediğiniz bir hizmet sağlıyorsa yararlı olur. Örneğin, bir Web hizmetinden finans verilerinde hesaplamalar gerçekleştiren Microsoft Office Excel için bir VSTO eklentileriniz varsa, diğer çözümler çalışma zamanında Excel VSTO eklentisini çağırarak bu hesaplamaları gerçekleştirebilir.

 [!INCLUDE[appliesto_allapp](../vsto/includes/appliesto-allapp-md.md)]

 Bu işlemde iki ana adım vardır:

- VSTO eklentilerinizde, bir nesneyi diğer çözümlere sunun.

- Başka bir çözümde, VSTO eklentisi tarafından kullanıma sunulan nesneye erişin ve nesnesinin üyelerini çağırın.

## <a name="types-of-solutions-that-can-call-code-in-an-add-in"></a>Bir eklentideki kodu çağırabilirler çözüm türleri
 Bir VSTO eklentisinin içindeki bir nesneyi aşağıdaki türlerde çözümler halinde kullanıma sunabilirsiniz:

- VSTO eklentiinizdeki aynı uygulama işleminde yüklü olan bir belgedeki Visual Basic for Applications (VBA) kodu.

- VSTO eklentilerinizle aynı uygulama sürecinde yüklenen belge düzeyi özelleştirmeleri.

- Visual Studio 'da Office proje şablonları kullanılarak oluşturulan diğer VSTO eklentileri.

- COM VSTO eklentileri (diğer bir deyişle, <xref:Extensibility.IDTExtensibility2> arabirimi doğrudan uygulayan VSTO eklentileri).

- VSTO eklentiinizdeki farklı bir işlemde çalışan herhangi bir çözüm (Bu tür çözümler, *işlem dışı istemciler*olarak da adlandırılır). Bunlar, bir Office uygulamasını otomatikleştiren bir Windows Forms veya konsol uygulaması ve farklı bir işlemde yüklenen VSTO eklentileri gibi uygulamaları içerir.

## <a name="expose-objects-to-other-solutions"></a>Nesneleri diğer çözümlere sunma
 VSTO eklentiinizdeki bir nesneyi diğer çözümlere sunmak için, VSTO eklentilerinizde aşağıdaki adımları gerçekleştirin:

1. Diğer çözümlere sunmak istediğiniz bir sınıf tanımlayın.

2. <xref:Microsoft.Office.Tools.AddInBase.RequestComAddInAutomationService%2A> Sınıfında yöntemi`ThisAddIn` geçersiz kılın. Diğer çözümlere sunmak istediğiniz sınıfın bir örneğini döndürün.

### <a name="define-the-class-you-want-to-expose-to-other-solutions"></a>Diğer çözümlere sunmak istediğiniz sınıfı tanımlayın
 En azından, göstermek istediğiniz sınıfın public olması gerekir, <xref:System.Runtime.InteropServices.ComVisibleAttribute> özniteliği **true**olarak ayarlanmalıdır ve [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) arabirimini kullanıma sunmalıdır.

 [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) arabirimini kullanıma sunmak için önerilen yol aşağıdaki adımları gerçekleştirmedir:

1. Diğer çözümlere sunmak istediğiniz üyeleri bildiren bir arabirim tanımlayın. Bu arabirimi, VSTO eklenti projenizde tanımlayabilirsiniz. Ancak, sınıfı VBA olmayan çözümlere göstermek istiyorsanız bu arabirimi ayrı bir sınıf kitaplığı projesinde tanımlamak isteyebilirsiniz. bu sayede, VSTO eklentisini çağıran çözümlerin, VSTO eklenti projenize başvurulmadan arabirime başvurabilmesi gerekir.

2. Özniteliği bu arabirime uygulayın ve bu özniteliği true olarak ayarlayın. <xref:System.Runtime.InteropServices.ComVisibleAttribute>

3. Bu arabirimi uygulamak için sınıfınızı değiştirin.

4. Özniteliğini sınıfınıza uygulayın ve bu özniteliği <xref:System.Runtime.InteropServices.ClassInterfaceType> numaralandırmanın **none** değerine ayarlayın. <xref:System.Runtime.InteropServices.ClassInterfaceAttribute>

5. Bu sınıfı işlem dışı istemcilere göstermek istiyorsanız aşağıdakileri de yapmanız gerekebilir:

   - Sınıfından türet <xref:System.Runtime.InteropServices.StandardOleMarshalObject>. Daha fazla bilgi için bkz. [sınıfları işlem dışı istemcilere](#outofproc)sunma.

   - Arabirimini tanımladığınız projede **com birlikte çalışma özelliğini kaydet** özelliğini ayarlayın. Bu özellik yalnızca, istemcilerin VSTO eklentisini çağırmak için erken bağlamayı kullanmasını etkinleştirmek istiyorsanız gereklidir.

   Aşağıdaki kod örneği, diğer çözümler `AddInUtilities` tarafından çağrılabilecek `ImportData` bir yöntemi olan bir sınıfı gösterir. Daha büyük bir anlatım bağlamında bu kodu görmek için bkz [. İzlenecek yol: Bir VSTO eklentisinde VBA](../vsto/walkthrough-calling-code-in-a-vsto-add-in-from-vba.md)'dan kod çağırma.

   [!code-csharp[Trin_AddInInteropWalkthrough #3](../vsto/codesnippet/CSharp/Trin_AddInInteropWalkthrough/AddInUtilities.cs#3)]
   [!code-vb[Trin_AddInInteropWalkthrough#3](../vsto/codesnippet/VisualBasic/Trin_AddInInteropWalkthrough/AddInUtilities.vb#3)]

### <a name="expose-classes-to-vba"></a>Sınıfları VBA 'da kullanıma sunma
 Yukarıda belirtilen adımları gerçekleştirdiğinizde, VBA kodu yalnızca arabirimde bildirdiğiniz yöntemleri çağırabilir. VBA kodu, sınıfınızın gibi temel sınıflardan <xref:System.Object>elde ettiği yöntemler de dahil olmak üzere sınıfınıza başka yöntemler çağrılamaz.

 Alternatif olarak, sıralamasının oto ya da oto <xref:System.Runtime.InteropServices.ClassInterfaceType> Dual <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> değerine ayarlayarak [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) arabirimini kullanıma sunabilirsiniz. Arabirimi kullanıma sunmanız durumunda, yöntemleri ayrı bir arabirimde bildirmeniz gerekmez. Ancak, VBA kodu, gibi temel sınıflardan <xref:System.Object>edinilen yöntemler de dahil olmak üzere sınıfınızdan ortak ve statik olmayan yöntemleri çağırabilir. Ayrıca, erken bağlama kullanan işlem dışı istemciler sınıfınızı çağıramaz.

### <a name="outofproc"></a>Sınıfları işlem dışı istemcilerde kullanıma sunma
 VSTO eklentiinizdeki bir sınıfı işlem dışı istemcilere sunmak istiyorsanız, işlem dışı istemcilerin sunulan VSTO eklenti nesnesini çağırabilecekleri <xref:System.Runtime.InteropServices.StandardOleMarshalObject> şekilde sınıfından sınıfını türetirsiniz... Aksi takdirde, işlem dışı bir istemcide kullanıma sunulan nesnenizin bir örneğini alma girişimleri beklenmedik şekilde başarısız olabilir.

 Bu hata, bir Office uygulamasının nesne modeline yapılan tüm çağrıların ana kullanıcı arabirimi iş parçacığında yapılması gerekir, ancak işlem dışı bir istemciden nesnenizin çağrısı, rastgele bir RPC (uzak yordam çağrısı) iş parçacığına ulaşır. .NET Framework COM sıralama mekanizması iş parçacıklarını değiştirmez ve bunun yerine, ana UI iş parçacığı yerine gelen RPC iş parçacığında nesneniz için çağrıyı sıralaması gerekir. Nesneniz öğesinden <xref:System.Runtime.InteropServices.StandardOleMarshalObject>türetilen bir sınıfın bir örneği ise, nesneniz için gelen çağrılar, ana bilgisayar uygulamasının ana kullanıcı arabirimi iş parçacığı olacak şekilde, gösterilen nesnenin oluşturulduğu iş parçacığına otomatik olarak sıralanır.

 Office çözümlerinde iş parçacıklarını kullanma hakkında daha fazla bilgi için bkz. [Office 'Te Iş parçacığı desteği](../vsto/threading-support-in-office.md).

### <a name="override-the-requestcomaddinautomationservice-method"></a>RequestComAddInAutomationService yöntemini geçersiz kılma
 Aşağıdaki kod örneği, VSTO eklentiinizdeki <xref:Microsoft.Office.Tools.AddInBase.RequestComAddInAutomationService%2A> `ThisAddIn` sınıfında nasıl geçersiz kılınacağını göstermektedir. Örnek, diğer çözümlere sunmak istediğiniz adlı `AddInUtilities` bir sınıf tanımlamış olduğunuzu varsayar. Daha büyük bir anlatım bağlamında bu kodu görmek için bkz [. İzlenecek yol: Bir VSTO eklentisinde VBA](../vsto/walkthrough-calling-code-in-a-vsto-add-in-from-vba.md)'dan kod çağırma.

 [!code-csharp[Trin_AddInInteropWalkthrough#1](../vsto/codesnippet/CSharp/Trin_AddInInteropWalkthrough/ThisAddIn.cs#1)]
 [!code-vb[Trin_AddInInteropWalkthrough#1](../vsto/codesnippet/VisualBasic/Trin_AddInInteropWalkthrough/ThisAddIn.vb#1)]

 VSTO eklentisi yüklendiğinde [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] , <xref:Microsoft.Office.Tools.AddInBase.RequestComAddInAutomationService%2A> yöntemini çağırır. Çalışma zamanı, döndürülen nesneyi VSTO eklentisini temsil eden bir <xref:Microsoft.Office.Core.COMAddIn> nesnenin COMAddIn. Object özelliğine atar. Bu <xref:Microsoft.Office.Core.COMAddIn> nesne diğer Office çözümleri ve Office 'i otomatikleştiren çözümler için kullanılabilir.

## <a name="access-objects-from-other-solutions"></a>Diğer çözümlerdeki nesnelere erişme
 VSTO eklentiinizdeki sunulan nesneyi çağırmak için, istemci çözümünde aşağıdaki adımları gerçekleştirin:

1. Sunulan VSTO eklentisini temsil eden nesneyialır.<xref:Microsoft.Office.Core.COMAddIn> İstemciler, ana bilgisayar Office uygulamasının nesne modelindeki `Application.COMAddIns` özelliğini kullanarak tüm kullanılabilir VSTO eklentilerine erişebilir.

2. <xref:Microsoft.Office.Core.COMAddIn> Nesnenin COMAddIn. Object özelliğine erişin. Bu özellik, VSTO eklentiden sunulan nesneyi döndürür.

3. Gösterilen nesnenin üyelerini çağırın.

   COMAddIn. Object özelliğinin dönüş değerini kullanma yöntemi, VBA istemcileri ve VBA olmayan istemciler için farklıdır. İşlem dışı istemcilerde, olası bir yarış durumundan kaçınmak için ek kod gereklidir.

### <a name="access-objects-from-vba-solutions"></a>VBA çözümlerinde nesnelere erişme
 Aşağıdaki kod örneği, bir VSTO eklentisi tarafından sunulan bir yöntemi çağırmak için VBA 'Yı nasıl kullanacağınızı gösterir. Bu VBA makrosu, `ImportData` **ExcelImportData**adlı bir VSTO eklentisinde tanımlanmış adlı bir yöntemi çağırır. Daha büyük bir anlatım bağlamında bu kodu görmek için bkz [. İzlenecek yol: Bir VSTO eklentisinde VBA](../vsto/walkthrough-calling-code-in-a-vsto-add-in-from-vba.md)'dan kod çağırma.

```vb
Sub CallVSTOMethod()
    Dim addIn As COMAddIn
    Dim automationObject As Object
    Set addIn = Application.COMAddIns("ExcelImportData")
    Set automationObject = addIn.Object
    automationObject.ImportData
End Sub
```

### <a name="access-objects-from-non-vba-solutions"></a>VBA olmayan çözümlerden nesnelere erişme
 VBA olmayan bir çözümde, COMAddIn. Object Özellik değerini uyguladığı arabirime atamalısınız ve sonra arabirim nesnesi üzerinde sunulan yöntemleri çağırabilirsiniz. Aşağıdaki kod örneği, Visual Studio 'da Office Geliştirici `ImportData` araçları kullanılarak oluşturulmuş farklı bir VSTO eklentisinin yönteminin nasıl çağrılacağını gösterir.

```vb
Dim addIn As Office.COMAddIn = Globals.ThisAddIn.Application.COMAddIns.Item("ExcelImportData")
Dim utilities As ExcelImportData.IAddInUtilities = TryCast( _
    addIn.Object, ExcelImportData.IAddInUtilities)
utilities.ImportData()
```

```csharp
object addInName = "ExcelImportData";
Office.COMAddIn addIn = Globals.ThisAddIn.Application.COMAddIns.Item(ref addInName);
ExcelImportData.IAddInUtilities utilities = (ExcelImportData.IAddInUtilities)addIn.Object;
utilities.ImportData();
```

 Bu örnekte, COMAddIn. Object özelliğinin `AddInUtilities` değerini `IAddInUtilities` arabirimi yerine sınıfına dönüştürmeye çalışırsanız, kod bir <xref:System.InvalidCastException>oluşturur.

## <a name="see-also"></a>Ayrıca bkz.
- [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md)
- [İzlenecek yol: Bir VSTO eklentisinde VBA 'dan kod çağırma](../vsto/walkthrough-calling-code-in-a-vsto-add-in-from-vba.md)
- [Office çözümleri geliştirme](../vsto/developing-office-solutions.md)
- [Nasıl yapılır: Visual Studio 'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md)
- [VSTO Eklentileri Mimarisi](../vsto/architecture-of-vsto-add-ins.md)
- [Genişletilebilirlik arabirimlerini kullanarak Kullanıcı arabirimi özelliklerini özelleştirme](../vsto/customizing-ui-features-by-using-extensibility-interfaces.md)
