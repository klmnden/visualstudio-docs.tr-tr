---
title: Araç penceresi kaydetme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- tool windows, registering managed
- tool windows, registering
ms.assetid: 8c8c4a24-3da4-497b-9db2-0ddd7cfbfdd2
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2ae53481b773cfdad5d4ac70f90202fcfd9d1ad4
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66334318"
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
