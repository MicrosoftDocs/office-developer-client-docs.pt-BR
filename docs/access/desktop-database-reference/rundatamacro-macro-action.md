---
title: Ação de macro ExecutarMacrodeDados
TOCTitle: RunDataMacro Macro Action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6777ae05d2ab7455016df834d17abb3406a2d710
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889921"
---
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="c6c39-102">Ação de macro ExecutarMacrodeDados</span><span class="sxs-lookup"><span data-stu-id="c6c39-102">RunDataMacro Macro Action</span></span>

<span data-ttu-id="c6c39-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6c39-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c6c39-104">Você pode usar a ação **ExecutarMacrodeDados** para executar uma macro.</span><span class="sxs-lookup"><span data-stu-id="c6c39-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="c6c39-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="c6c39-105">Setting</span></span>

<span data-ttu-id="c6c39-106">A ação **ExecutarMacrodeDados** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c6c39-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6c39-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="c6c39-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c6c39-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6c39-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6c39-109">Name</span><span class="sxs-lookup"><span data-stu-id="c6c39-109">Name</span></span></p></td>
<td><p><span data-ttu-id="c6c39-110">O nome da macro de dados a ser executada.</span><span class="sxs-lookup"><span data-stu-id="c6c39-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c6c39-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6c39-111">Remarks</span></span>

<span data-ttu-id="c6c39-112">Você pode usar a ação **ExecutarMacrodeDados** em macros, macros de dados nomeadas e nos seguintes eventos de macro: **[Evento de macro Após Exclusão](after-delete-macro-event.md)**, **[Evento de macro Após Inserir](after-insert-macro-event.md)** e **[Evento de macro Após Atualizar](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="c6c39-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete Macro Event](after-delete-macro-event.md)**, **[After Insert Macro Event](after-insert-macro-event.md)** and **[After Update Macro Event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="c6c39-113">O nome da macro de dados deve incluir a tabela à qual ele está conectado (por exemplo, **comentários**, não apenas **AddComment**).</span><span class="sxs-lookup"><span data-stu-id="c6c39-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="c6c39-114">Quando você selecionar a macro de dados que deseja executar no designer de macros, o Access determinará se a macro de dados exige parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c6c39-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="c6c39-115">Se a macro de dados requer parâmetros, caixas de texto aparecem onde você pode digitar nos argumentos.</span><span class="sxs-lookup"><span data-stu-id="c6c39-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="c6c39-p102">Quando você executa uma macro que contém a ação **ExecutarMacrodeDados** e ela alcançar a ação **ExecutarMacrodeDados**, o Access executará a macro de dados chamada. Após a conclusão da macro de dados chamada, o Access retornará à macro original e executará a próxima ação.</span><span class="sxs-lookup"><span data-stu-id="c6c39-p102">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="c6c39-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c6c39-118">Example</span></span>

<span data-ttu-id="c6c39-119">O exemplo a seguir mostra como passar um parâmetro a uma macro de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="c6c39-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="c6c39-120">A macro de dados da tabela tblServiceRequests dmGetCurrentServiceRequest é chamada usando a ação ExecutarMacrodeDados.</span><span class="sxs-lookup"><span data-stu-id="c6c39-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="c6c39-121">Quando o dmGetCurrentServiceRequest for concluído, a variável CurrentServiceRequest retornados a macro de dados está escrita à caixa de texto txtCurrentSR do formulário.</span><span class="sxs-lookup"><span data-stu-id="c6c39-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="c6c39-122">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="c6c39-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```
