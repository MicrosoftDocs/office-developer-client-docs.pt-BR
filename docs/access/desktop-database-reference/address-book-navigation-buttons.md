---
title: Botões de navegação do Catálogo de Endereços
TOCTitle: Address Book navigation buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7c87acd433df4a303c1e6a15a60184cadf994c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282461"
---
# <a name="address-book-navigation-buttons"></a><span data-ttu-id="a06ae-102">Botões de navegação do Catálogo de Endereços</span><span class="sxs-lookup"><span data-stu-id="a06ae-102">Address Book navigation buttons</span></span>

<span data-ttu-id="a06ae-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a06ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a06ae-104">O aplicativo de Agenda exibe os botões de navegação na parte inferior da página da Web.</span><span class="sxs-lookup"><span data-stu-id="a06ae-104">The Address Book application displays the navigation buttons at the bottom of the webpage.</span></span> <span data-ttu-id="a06ae-105">Você pode utilizar os botões de navegação para navegar através dos dados na exibição da grade HTML, selecionando a primeira e a última linha de dados ou linhas adjacentes à seleção atual.</span><span class="sxs-lookup"><span data-stu-id="a06ae-105">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>

## <a name="navigation-sub-procedures"></a><span data-ttu-id="a06ae-106">Subprocedimentos de navegação</span><span class="sxs-lookup"><span data-stu-id="a06ae-106">Navigation Sub Procedures</span></span>

<span data-ttu-id="a06ae-107">O aplicativo de Catálogo de Endereço contém vários procedimentos que permitem aos usuários clicarem nos botões **Primeiro**, **Próximo**, **Anterior** e **Último** para mover-se ap redor dos dados.</span><span class="sxs-lookup"><span data-stu-id="a06ae-107">The Address Book application contains several procedures that allow users to click the **First**, **Next**, **Previous**, and **Last** buttons to move around the data.</span></span>

<span data-ttu-id="a06ae-108">Por exemplo, clicar no **botão Primeiro** ativa o procedimento VBScript First \_ OnClick Sub.</span><span class="sxs-lookup"><span data-stu-id="a06ae-108">For example, clicking the **First** button activates the VBScript First\_OnClick Sub procedure.</span></span> <span data-ttu-id="a06ae-109">O procedimento executa um método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md), que torna a primeira linha de dados a seleção atual.</span><span class="sxs-lookup"><span data-stu-id="a06ae-109">The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection.</span></span> <span data-ttu-id="a06ae-110">Clicar no **último botão** ativa o último procedimento OnClick Sub, que invoca o método \_ [MoveLast,](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) tornando a última linha de dados a seleção atual.</span><span class="sxs-lookup"><span data-stu-id="a06ae-110">Clicking the **Last** button activates the Last\_OnClick Sub procedure, which invokes the [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, making the last row of data the current selection.</span></span> <span data-ttu-id="a06ae-111">Os demais botões de navegação trabalham de uma maneira semelhante.</span><span class="sxs-lookup"><span data-stu-id="a06ae-111">The remaining navigation buttons work in a similar fashion.</span></span>

```vb 
 
' Move to the first record in the bound Recordset. 
Sub First_OnClick 
 DC1.Recordset.MoveFirst 
End Sub 
 
' Move to the next record from the current position 
' in the bound Recordset. 
Sub Next_OnClick 
 If Not DC1.Recordset.EOF Then ' Cannot move beyond bottom record. 
 DC1.Recordset.MoveNext 
 Exit Sub 
 End If 
End Sub 
 
' Move to the previous record from the current position in the bound 
' Recordset. 
Sub Prev_OnClick 
 If Not DC1.Recordset.BOF Then ' Cannot move beyond top record. 
 DC1.Recordset.MovePrevious 
 Exit Sub 
 End If 
End Sub 
 
' Move to the last record in the bound Recordset. 
Sub Last_OnClick 
 DC1.Recordset.MoveLast 
End Sub 
```

