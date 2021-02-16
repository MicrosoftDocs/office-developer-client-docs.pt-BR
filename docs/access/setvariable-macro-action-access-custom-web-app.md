---
title: Ação de macro SetVariable (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a4ffbd02-eed7-43ed-9da2-f0d1ff5d8014
description: Você pode usar a ação SetVariable para criar uma variável temporária e defini-la para um valor específico. A variável pode ser usada como uma condição ou argumento em ações subsequentes ou você pode usar a variável em outra macro de interface do usuário.
ms.openlocfilehash: 54c23868a5bfb66a2fb08465361583c6e9b5ed49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433917"
---
# <a name="setvariable-macro-action-access-custom-web-app"></a><span data-ttu-id="cac2f-104">Ação de macro SetVariable (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="cac2f-104">SetVariable Macro Action (Access custom web app)</span></span>

<span data-ttu-id="cac2f-105">Você pode usar a **ação SetVariable** para criar uma variável temporária e defini-la para um valor específico.</span><span class="sxs-lookup"><span data-stu-id="cac2f-105">You can use the **SetVariable** action to create a temporary variable and set it to a specific value.</span></span> <span data-ttu-id="cac2f-106">A variável pode ser usada como uma condição ou argumento em ações subsequentes ou você pode usar a variável em outra macro de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="cac2f-106">The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="cac2f-p103">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="cac2f-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="cac2f-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="cac2f-109">Setting</span></span>

<span data-ttu-id="cac2f-110">A **ação DefinirVariável** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="cac2f-110">The **SetVariable** action has the following arguments.</span></span> 
  
|<span data-ttu-id="cac2f-111">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="cac2f-111">**Action argument**</span></span>|<span data-ttu-id="cac2f-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cac2f-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cac2f-113">**Variável**</span><span class="sxs-lookup"><span data-stu-id="cac2f-113">**Variable**</span></span> <br/> |<span data-ttu-id="cac2f-114">Digite o nome da variável temporária.</span><span class="sxs-lookup"><span data-stu-id="cac2f-114">Enter the name of the temporary variable.</span></span>  <br/> |
|<span data-ttu-id="cac2f-115">**Valor =**</span><span class="sxs-lookup"><span data-stu-id="cac2f-115">**Value =**</span></span> <br/> |<span data-ttu-id="cac2f-116">Insira a expressão a ser usada para definir o valor dessa variável temporária.</span><span class="sxs-lookup"><span data-stu-id="cac2f-116">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="cac2f-117">Não preceda a expressão com o sinal de igual ( **=** ).</span><span class="sxs-lookup"><span data-stu-id="cac2f-117">Do not precede the expression with the equal (**=** ) sign.</span></span> <span data-ttu-id="cac2f-118">Você pode clicar no **botão Criar** ![Fórmula](media/buildbut_ZA06047218.gif "para") usar o Construtor de Expressões para definir esse argumento.</span><span class="sxs-lookup"><span data-stu-id="cac2f-118">You can click the **Build** button ![Formula](media/buildbut_ZA06047218.gif "Formula") to use the Expression Builder to set this argument.</span></span>  <br/> |
   

