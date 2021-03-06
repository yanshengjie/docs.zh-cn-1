---
title: 如何：为应用程序设置 ToolStrip 呈现程序
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Renderer property [Windows Forms]
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
- toolbars [Windows Forms], customizing
ms.assetid: 46acef3e-9844-4ae8-9a2e-3006fe99cadf
ms.openlocfilehash: f4189b19b78ce3cda1981220caa1fce3f2ec708d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33533710"
---
# <a name="how-to-set-the-toolstrip-renderer-for-an-application"></a>如何：为应用程序设置 ToolStrip 呈现程序
可以单独自定义 <xref:System.Windows.Forms.ToolStrip> 控件的外观，或应用程序中所有 <xref:System.Windows.Forms.ToolStrip> 控件的外观。  
  
## <a name="example"></a>示例  
 下面的代码示例演示如何有选择地应用自定义呈现器到 <xref:System.Windows.Forms.ToolStrip> 控件和 <xref:System.Windows.Forms.MenuStrip> 控件。  
  
 若要使用此代码示例，请编译并运行该应用程序，然后从 <xref:System.Windows.Forms.ComboBox> 控件中选择自定义呈现的作用域。 单击“应用”设置呈现器。  
  
 若要查看自定义菜单项呈现，选择<xref:System.Windows.Forms.MenuStrip>选项从<xref:System.Windows.Forms.ComboBox>控件中，单击**应用**，然后打开**文件**菜单项。  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#70](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#70)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#70](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#70)]  
  
 设置 <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType> 属性，将自定义呈现器应用到你的应用程序中所有的 <xref:System.Windows.Forms.ToolStrip> 控件。  
  
 设置 <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> 属性，将自定义呈现器应用到单个 <xref:System.Windows.Forms.ToolStrip> 控件。  
  
## <a name="compiling-the-code"></a>编译代码  
 此示例需要：  
  
-   对 System.Design、System.Drawing 和 System.Windows.Forms 程序集的引用。  
  
 有关生成此示例从 visual Basic 或 Visual C# 的命令行的信息，请参阅[从命令行生成](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)或[命令行上使用 csc.exe 生成](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)。 你也可以通过将代码粘贴到新项目中生成 Visual Studio 中的此示例。  另请参阅 [如何：使用 Visual Studio 编译和运行完整的 Windows 窗体代码示例](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\))。  
  
## <a name="see-also"></a>请参阅  
 <xref:System.Windows.Forms.ToolStripManager>  
 <xref:System.Windows.Forms.MenuStrip>  
 <xref:System.Windows.Forms.ToolStrip>  
 <xref:System.Windows.Forms.ToolStripProfessionalRenderer>  
 [ToolStrip 控件](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
