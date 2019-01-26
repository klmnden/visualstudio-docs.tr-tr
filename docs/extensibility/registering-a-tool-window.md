---
title: Araç penceresi kaydetme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- tool windows, registering managed
- tool windows, registering
ms.assetid: 8c8c4a24-3da4-497b-9db2-0ddd7cfbfdd2
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f09788cb69e90114839a66ff0652c779535b066b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54944052"
---
# <a name="register-a-tool-window"></a>Araç penceresi kaydetme
Kullanarak, araç pencerelerini kaydedebilirsiniz <xref:Microsoft.VisualStudio.Shell.ProvideToolWindowAttribute> ve <xref:Microsoft.VisualStudio.Shell.ProvideToolWindowVisibilityAttribute>.  
  
## <a name="example"></a>Örnek  
  
```csharp
  
[ProvideToolWindow(typeof(PersistedWindowPane), Style = MsVsShell.VsDockStyle.Tabbed, Window = "3ae79031-e1bc-11d0-8f78-00a0c9110057")]
[ProvideToolWindow(typeof(DynamicWindowPane), PositionX=250, PositionY=250, Width=160, Height=180, Transient=true)]
[ProvideToolWindowVisibility(typeof(DynamicWindowPane), /*UICONTEXT_SolutionExists*/"f1536ef8-92ec-443c-9ed7-fdadf150da82")]  
[ProvideMenuResource(1000, 1)]  
[PackageRegistration(UseManagedResourcesOnly = true)]  
[Guid("01069CDD-95CE-4620-AC21-DDFF6C57F012")]  
public class PackageToolWindow : Package  
{  
```
  
 Yukarıdaki kodda <xref:Microsoft.VisualStudio.Shell.ProvideToolWindowAttribute> kaydeder `PersistedWindowPane` ve `DynamicWindowPane` araç penceresi Visual Studio ile. Kalıcı araç penceresi yerleştirilmiş ve ile sekmeli **Çözüm Gezgini**, ve dinamik pencerenin başlangıç konumu ve boyutu varsayılan verilir. Dinamik pencerenin başlangıç oluşturulmaz belirten geçici yapılır. Bu Yazar bir `DontForceCreate` değerini `ToolWindows` sistem kayıt defterinde anahtar. Daha fazla bilgi için [araç penceresi ekran yapılandırması](../extensibility/tool-window-display-configuration.md).
