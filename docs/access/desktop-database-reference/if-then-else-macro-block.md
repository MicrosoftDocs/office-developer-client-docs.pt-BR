---
title: Bloco de macro Se...Então...Senão
TOCTitle: If...Then...Else Macro Block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c7c6842e8463250f6575cfc85364ec3bff7aba1a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876040"
---
# <a name="ifthenelse-macro-block"></a><span data-ttu-id="44058-102">Bloco de macro Se...Então...Senão</span><span class="sxs-lookup"><span data-stu-id="44058-102">If...Then...Else Macro Block</span></span>


<span data-ttu-id="44058-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="44058-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44058-104">Você pode usar o bloco de macro **Se** para executar condicionalmente um grupo de ações, dependendo do valor de uma expressão.</span><span class="sxs-lookup"><span data-stu-id="44058-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span>

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a><span data-ttu-id="44058-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="44058-105">Setting</span></span>

<span data-ttu-id="44058-106">Para **se** e **Senão se**, os argumentos a seguir são necessários.</span><span class="sxs-lookup"><span data-stu-id="44058-106">For both **If** and **Else If**, the following arguments are required.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44058-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="44058-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="44058-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="44058-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44058-109"><strong>Expressão</strong>.</span><span class="sxs-lookup"><span data-stu-id="44058-109"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="44058-110">A condição que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="44058-110">The condition that you wish to test.</span></span> <span data-ttu-id="44058-111">Ela deve ser uma expressão que é avaliada como True ou False.</span><span class="sxs-lookup"><span data-stu-id="44058-111">It must be an expression that evaluates to True or False.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="44058-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="44058-112">Remarks</span></span>

<span data-ttu-id="44058-p102">Quando você seleciona o bloco de macro **Se**, uma caixa de texto é exibida para que você digite uma expressão que representa a condição a ser testada. Além disso, uma caixa de combinação é exibida para que você insira uma ação de macro, abaixo da qual o texto "Encerrar Se" é exibido automaticamente. Se e Encerrar Se delimitam uma área na qual é possível digitar um grupo ou um bloco de ações. O bloco será executado somente se a expressão inserida tiver o valor True.</span><span class="sxs-lookup"><span data-stu-id="44058-p102">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span>

<span data-ttu-id="44058-p103">Para avaliar outra expressão quando a primeira expressão tiver o valor False, clique em **Adicionar Senão Se** para inserir um bloco **Senão Se** adicional. A expressão inserida deve avaliar como True ou False. Nesse caso, o bloco será executado somente se a expressão tiver o valor True e a primeira expressão tiver o valor False.</span><span class="sxs-lookup"><span data-stu-id="44058-p103">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span></span>

<span data-ttu-id="44058-120">Você pode adicionar a quantidade necessária de **Senão Se** a um bloco Se.</span><span class="sxs-lookup"><span data-stu-id="44058-120">You can add as many **Else If** blocks as you like to an If block.</span></span>

<span data-ttu-id="44058-p104">Clique em **Adicionar Senão** para inserir um bloco **Senão** adicional. Nesse caso, as ações inseridas abaixo de **Senão** formam o bloco **Senão**, que será executado somente se as ações acima não forem executadas. É possível adicionar um único bloco **Senão** a um bloco **Se**.</span><span class="sxs-lookup"><span data-stu-id="44058-p104">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span>

<span data-ttu-id="44058-124">No exemplo de código a seguir, as ações de macro no primeiro bloco executados se o valor da \[Status\] for maior que 0.</span><span class="sxs-lookup"><span data-stu-id="44058-124">In the following code example, the macro actions in the first block execute if the value of \[Status\] is greater than 0.</span></span> <span data-ttu-id="44058-125">Se o valor da \[Status\] não for maior do que 0, a expressão que segue **Senão se** é avaliada.</span><span class="sxs-lookup"><span data-stu-id="44058-125">If the value of \[Status\] is not greater than 0, the expression that follows the **Else If** is evaluated.</span></span> <span data-ttu-id="44058-126">As ações de macro no bloco **Senão se** executados se o valor da \[Status\] for igual a 0.</span><span class="sxs-lookup"><span data-stu-id="44058-126">The macro actions in the **Else If** block execute if the value of \[Status\] is equal to 0.</span></span> <span data-ttu-id="44058-127">Finalmente, se nem o primeiro bloco, nem o segundo forem executados, as ações no bloco **Senão** serão executadas.</span><span class="sxs-lookup"><span data-stu-id="44058-127">Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

<span data-ttu-id="44058-128">Você pode aninhar blocos **Se**.</span><span class="sxs-lookup"><span data-stu-id="44058-128">You can nest **If** blocks.</span></span> <span data-ttu-id="44058-129">Considere o aninhamento do bloco **Se** em um bloco **Se** se você deseja avaliar uma segunda expressão, quando a primeira expressão tiver o valor True.</span><span class="sxs-lookup"><span data-stu-id="44058-129">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="44058-130">No exemplo de código a seguir, o bloco de **se** inner só é executado quando o valor da \[Status\] é ambos maior que 0 *e* maior que 100.</span><span class="sxs-lookup"><span data-stu-id="44058-130">In the following code example, the inner **If** block only executes when the value of \[Status\] is both greater than 0 *and* greater than 100.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
