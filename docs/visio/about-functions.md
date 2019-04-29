---
title: Sobre Funções
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251825
localization_priority: Normal
ms.assetid: 871b8601-8117-bc51-17b9-6002234b4bfb
description: 'Uma função executa uma única tarefa bem definida. A maioria das funções assume vários argumentos como entrada. Embora o tipo e o número de argumentos dependam da função, todas as funções têm uma mesma sintaxe geral:'
ms.openlocfilehash: 14995b0f7e3c1cc8346d47965038902b8ca4e8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415975"
---
# <a name="about-functions"></a><span data-ttu-id="76fe0-105">Sobre Funções</span><span class="sxs-lookup"><span data-stu-id="76fe0-105">About Functions</span></span>

<span data-ttu-id="76fe0-p102">Uma função executa uma única tarefa bem definida. A maioria das funções assume vários argumentos como entrada. Embora o tipo e o número de argumentos dependam da função, todas as funções têm uma mesma sintaxe geral:</span><span class="sxs-lookup"><span data-stu-id="76fe0-p102">A function performs a single well-defined task. Most functions take a number of arguments as input. Although the type and number of arguments depend on the function, all functions have the same general syntax:</span></span>
  
 <span data-ttu-id="76fe0-109">**Função (** _argument1_, _argument2_,...</span><span class="sxs-lookup"><span data-stu-id="76fe0-109">**FUNCTION(** _argument1_,  _argument2_, …</span></span>  <span data-ttu-id="76fe0-110">_argumenton_ [, argumento _argumento_ |  __ **])**</span><span class="sxs-lookup"><span data-stu-id="76fe0-110">_argumentN_ [,  _argumentA_ |  _argument_ **])**</span></span>
  
|<span data-ttu-id="76fe0-111">**Elemento de sintaxe**</span><span class="sxs-lookup"><span data-stu-id="76fe0-111">**Syntax element**</span></span>|<span data-ttu-id="76fe0-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="76fe0-112">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="76fe0-113">( )</span><span class="sxs-lookup"><span data-stu-id="76fe0-113"></span></span>  <br/> | <span data-ttu-id="76fe0-114">Se a função não assumir nenhum argumento, ela deverá ser seguida por parênteses vazios ( ).</span><span class="sxs-lookup"><span data-stu-id="76fe0-114">If a function takes no arguments, it must be followed by an empty set of parentheses ( ).</span></span>  <br/> |
| <span data-ttu-id="76fe0-115">,</span><span class="sxs-lookup"><span data-stu-id="76fe0-115"></span></span>  <br/> | <span data-ttu-id="76fe0-116">Os argumentos são separados por uma vírgula.</span><span class="sxs-lookup"><span data-stu-id="76fe0-116">Arguments are separated by a comma.</span></span>  <br/> |
| <span data-ttu-id="76fe0-117">...</span><span class="sxs-lookup"><span data-stu-id="76fe0-117"></span></span>  <br/> | <span data-ttu-id="76fe0-118">Usado somente para notação; não inclui uma função.</span><span class="sxs-lookup"><span data-stu-id="76fe0-118">Used for notation only; do not include in a function.</span></span>  <br/> |
| <span data-ttu-id="76fe0-119">[ ]</span><span class="sxs-lookup"><span data-stu-id="76fe0-119"></span></span>  <br/> | <span data-ttu-id="76fe0-p104">Argumento opcional. Usado somente para notação; não inclui uma função.</span><span class="sxs-lookup"><span data-stu-id="76fe0-p104">Optional argument. Used for notation only; do not include in a function.</span></span>  <br/> |
| |  <br/> | <span data-ttu-id="76fe0-122">Uma opção; Você pode incluir _argumentoum_ ou _argumento_.</span><span class="sxs-lookup"><span data-stu-id="76fe0-122">A choice; you can include  _argumentA_ or  _argument_.</span></span> <span data-ttu-id="76fe0-123">Usado somente para notação; não inclui uma função.</span><span class="sxs-lookup"><span data-stu-id="76fe0-123">Used for notation only; do not include in a function.</span></span>  <br/> |
   
<span data-ttu-id="76fe0-p106">Muitas funções utilizadas em fórmulas são semelhantes àquelas usadas em programas de planilha eletrônica: matemáticas, como SUM ou SQRT; trigonométricas, como SIN ou COS; ou lógicas, como IF ou NOT. Várias outras funções são exclusivas do Microsoft Office Visio, como GUARD, GRAVITA e RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="76fe0-p106">Many functions that you can use in formulas resemble those you have seen in spreadsheet programs: mathematical, such as SUM or SQRT; trigonometric, such as SIN or COS; or logical, such as IF or NOT. Many other functions are unique to Microsoft Office Visio, such as GUARD, GRAVITY, and RUNADDON.</span></span>
  
<span data-ttu-id="76fe0-126">Para obter mais informações sobre funções específicas, consulte a Referência do ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="76fe0-126">For more information on specific functions, see this ShapeSheet Reference.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="76fe0-127">Determinadas funções aparecem em fórmulas geradas pelo Visio, mas não são mostradas na caixa de diálogo **Editar fórmula** ou descritas nesta referência porque são reservadas para uso interno e não devem ser usadas em outras fórmulas.</span><span class="sxs-lookup"><span data-stu-id="76fe0-127">Certain functions appear in formulas generated by Visio, but are not shown in the **Edit Formula** dialog box or described in this reference because they are reserved for internal use and should not be used in other formulas.</span></span> <span data-ttu-id="76fe0-128">Veja alguns exemplos: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1 e _SHAPEMIN.</span><span class="sxs-lookup"><span data-stu-id="76fe0-128">Following are examples: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1, and _SHAPEMIN.</span></span> 
  

