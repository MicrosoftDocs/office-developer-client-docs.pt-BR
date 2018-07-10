---
title: Se... Então... Bloco de Macro Else (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Você pode usar a se bloco de macro para executar condicionalmente um grupo de ações, dependendo do valor de uma expressão.
ms.openlocfilehash: 8ac78ff0eaf22c1d821e306654ebfa8fac4ed34a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765080"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a><span data-ttu-id="a0fb1-103">Se... Então... Bloco de Macro Else (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="a0fb1-103">If...Then...Else Macro Block (Access custom web app)</span></span>

<span data-ttu-id="a0fb1-104">Você pode usar o bloco de macro **Se** para executar condicionalmente um grupo de ações, dependendo do valor de uma expressão.</span><span class="sxs-lookup"><span data-stu-id="a0fb1-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a0fb1-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="a0fb1-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a0fb1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0fb1-107">Syntax</span></span>

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a><span data-ttu-id="a0fb1-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="a0fb1-108">Setting</span></span>

<span data-ttu-id="a0fb1-109">Para **Se** e ** Senão Se **, os seguintes argumentos são requeridos.</span><span class="sxs-lookup"><span data-stu-id="a0fb1-109">For both **If** and ** Else If **, the following arguments are required.</span></span> 
  
|<span data-ttu-id="a0fb1-110">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="a0fb1-110">**Action argument**</span></span>|<span data-ttu-id="a0fb1-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a0fb1-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0fb1-112">**Expressão**</span><span class="sxs-lookup"><span data-stu-id="a0fb1-112">**Expression**</span></span> <br/> |<span data-ttu-id="a0fb1-113">A condição que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="a0fb1-113">The condition that you wish to test.</span></span> <span data-ttu-id="a0fb1-114">Ela deve ser uma expressão que é avaliada como True ou False.</span><span class="sxs-lookup"><span data-stu-id="a0fb1-114">It must be an expression that evaluates to True or False.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0fb1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0fb1-115">Remarks</span></span>

<span data-ttu-id="a0fb1-p103">Quando você seleciona o bloco de macro **Se**, uma caixa de texto é exibida para que você digite uma expressão que representa a condição a ser testada. Além disso, uma caixa de combinação é exibida para que você insira uma ação de macro, abaixo da qual o texto "Encerrar Se" é exibido automaticamente. Se e Encerrar Se delimitam uma área na qual é possível digitar um grupo ou um bloco de ações. O bloco será executado somente se a expressão inserida tiver o valor True.</span><span class="sxs-lookup"><span data-stu-id="a0fb1-p103">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span> 
  
<span data-ttu-id="a0fb1-p104">Para avaliar outra expressão quando a primeira expressão tiver o valor False, clique em **Adicionar Senão Se** para inserir um bloco **Senão Se** adicional. A expressão inserida deve avaliar como True ou False. Nesse caso, o bloco será executado somente se a expressão tiver o valor True e a primeira expressão tiver o valor False.</span><span class="sxs-lookup"><span data-stu-id="a0fb1-p104">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span></span> 
  
<span data-ttu-id="a0fb1-123">Você pode adicionar a quantidade necessária de **Senão Se** a um bloco Se.</span><span class="sxs-lookup"><span data-stu-id="a0fb1-123">You can add as many **Else If** blocks as you like to an If block.</span></span> 
  
<span data-ttu-id="a0fb1-p105">Clique em **Adicionar Senão** para inserir um bloco **Senão** adicional. Nesse caso, as ações inseridas abaixo de **Senão** formam o bloco **Senão**, que será executado somente se as ações acima não forem executadas. É possível adicionar um único bloco **Senão** a um bloco **Se**.</span><span class="sxs-lookup"><span data-stu-id="a0fb1-p105">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span> 
  
<span data-ttu-id="a0fb1-p106">No exemplo de código a seguir, as ações de macro no primeiro bloco serão executadas se o valor de [Status] for maior que 0. Se o valor de [Status] não for maior que 0, a expressão após **Senão Se** será avaliada. As ações de macro no bloco **Senão Se** serão executadas se o valor de [Status] for igual a 0. Finalmente, se nem o primeiro bloco, nem o segundo forem executados, as ações no bloco **Senão** serão executadas.</span><span class="sxs-lookup"><span data-stu-id="a0fb1-p106">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0. If the value of [Status] is not greater than 0, the expression that follows the **Else If** is evaluated. The macro actions in the **Else If** block execute if the value of [Status] is equal to 0. Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span> 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

<span data-ttu-id="a0fb1-p107">Você pode aninhar blocos **Se**. Considere o aninhamento do bloco **Se** em um bloco **Se** se você deseja avaliar uma segunda expressão, quando a primeira expressão tiver o valor True. No exemplo de código a seguir, o bloco **Se** interno somente será executado quando o valor de [Status] for maior que 0  *e*  maior que 100.</span><span class="sxs-lookup"><span data-stu-id="a0fb1-p107">You can nest **If** blocks. You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True. In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span></span> 
  

