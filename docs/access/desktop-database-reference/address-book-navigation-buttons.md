---
title: Botões de navegação do Catálogo de Endereços
TOCTitle: Address Book Navigation Buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f37a188fd3ddb3608eda414fbdcea6402cd9d41
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603942"
---
# <a name="address-book-navigation-buttons"></a><span data-ttu-id="7a78e-102">Botões de navegação do Catálogo de Endereços</span><span class="sxs-lookup"><span data-stu-id="7a78e-102">Address Book Navigation Buttons</span></span>


<span data-ttu-id="7a78e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a78e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7a78e-104"><<<<<<< Aplicativo cabeça o catálogo de endereços exibe os botões de navegação na parte inferior da página da Web.</span><span class="sxs-lookup"><span data-stu-id="7a78e-104"><<<<<<< HEAD The Address Book application displays the navigation buttons at the bottom of the Web page.</span></span> <span data-ttu-id="7a78e-105">Você pode utilizar os botões de navegação para navegar através dos dados na exibição da grade HTML, selecionando a primeira e a última linha de dados ou linhas adjacentes à seleção atual.</span><span class="sxs-lookup"><span data-stu-id="7a78e-105">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>
<span data-ttu-id="7a78e-106">=== O aplicativo de catálogo de endereços exibe os botões de navegação na parte inferior da página da Web.</span><span class="sxs-lookup"><span data-stu-id="7a78e-106">======= The Address Book application displays the navigation buttons at the bottom of the webpage.</span></span> <span data-ttu-id="7a78e-107">Você pode utilizar os botões de navegação para navegar através dos dados na exibição da grade HTML, selecionando a primeira e a última linha de dados ou linhas adjacentes à seleção atual.</span><span class="sxs-lookup"><span data-stu-id="7a78e-107">You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>
>>>>>>> <span data-ttu-id="7a78e-108">mestre</span><span class="sxs-lookup"><span data-stu-id="7a78e-108">master</span></span>

## <a name="navigation-sub-procedures"></a><span data-ttu-id="7a78e-109">Subprocedimentos de navegação</span><span class="sxs-lookup"><span data-stu-id="7a78e-109">Navigation Sub Procedures</span></span>

<span data-ttu-id="7a78e-110">O aplicativo de Catálogo de Endereço contém vários procedimentos que permitem aos usuários clicarem nos botões **Primeiro**, **Próximo**, **Anterior** e **Último** para mover-se ap redor dos dados.</span><span class="sxs-lookup"><span data-stu-id="7a78e-110">The Address Book application contains several procedures that allow users to click the **First**, **Next**, **Previous**, and **Last** buttons to move around the data.</span></span>

<span data-ttu-id="7a78e-111">Por exemplo, clicando no botão **primeiro** ativa a primeira VBScript\_procedimento OnClick Sub.</span><span class="sxs-lookup"><span data-stu-id="7a78e-111">For example, clicking the **First** button activates the VBScript First\_OnClick Sub procedure.</span></span> <span data-ttu-id="7a78e-112">O procedimento executa um método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md), que torna a primeira linha de dados a seleção atual.</span><span class="sxs-lookup"><span data-stu-id="7a78e-112">The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection.</span></span> <span data-ttu-id="7a78e-113">Clicar no botão **último** ativa a última\_procedimento OnClick Sub, que chama o método [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) , tornando a última linha de dados da seleção atual.</span><span class="sxs-lookup"><span data-stu-id="7a78e-113">Clicking the **Last** button activates the Last\_OnClick Sub procedure, which invokes the [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, making the last row of data the current selection.</span></span> <span data-ttu-id="7a78e-114">Os demais botões de navegação trabalham de uma maneira semelhante.</span><span class="sxs-lookup"><span data-stu-id="7a78e-114">The remaining navigation buttons work in a similar fashion.</span></span>

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

