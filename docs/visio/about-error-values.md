---
title: Sobre valores de erro
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: Os valores de erro são exibidos em células que contêm fórmulas incorretas para essa célula.
ms.openlocfilehash: 5219becdd1af888e424a2fe33faa7df5a06f61fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423864"
---
# <a name="about-error-values"></a><span data-ttu-id="b30df-103">Sobre valores de erro</span><span class="sxs-lookup"><span data-stu-id="b30df-103">About Error Values</span></span>

<span data-ttu-id="b30df-104">Os valores de erro são exibidos em células que contêm fórmulas incorretas para essa célula.</span><span class="sxs-lookup"><span data-stu-id="b30df-104">Error values are displayed in cells that have incorrect formulas for that cell.</span></span>
  
<span data-ttu-id="b30df-p101">Se uma fórmula fizer referência a uma célula que contenha um valor de erro, essa fórmula também exibirá um valor de erro. Use as funções ISERR, ISERRNA, ISERROR ou ISERRVALUE para procurar valores de erro.</span><span class="sxs-lookup"><span data-stu-id="b30df-p101">If a formula references a cell that contains an error value, that formula also displays an error value. You can use the function ISERR, ISERRNA, ISERROR, or ISERRVALUE to look for error values.</span></span>
  
<span data-ttu-id="b30df-107">**Valores de erro**</span><span class="sxs-lookup"><span data-stu-id="b30df-107">**Error values**</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="b30df-108">**Se a célula exibir**</span><span class="sxs-lookup"><span data-stu-id="b30df-108">**If the cell displays**</span></span> <br/> |<span data-ttu-id="b30df-109">**A fórmula inclui**</span><span class="sxs-lookup"><span data-stu-id="b30df-109">**The formula includes**</span></span> <br/> |<span data-ttu-id="b30df-110">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="b30df-110">**Example**</span></span> <br/> |
| <span data-ttu-id="b30df-111">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="b30df-111">#DIV/0!</span></span>  <br/> |<span data-ttu-id="b30df-112">Divisão por 0</span><span class="sxs-lookup"><span data-stu-id="b30df-112">Division by 0</span></span>  <br/> |<span data-ttu-id="b30df-113">10/0</span><span class="sxs-lookup"><span data-stu-id="b30df-113">10/0</span></span>  <br/> |
| <span data-ttu-id="b30df-114">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="b30df-114">#VALUE!</span></span>  <br/> | <span data-ttu-id="b30df-115">Um argumento ou operando do tipo errado</span><span class="sxs-lookup"><span data-stu-id="b30df-115">An argument or operand of the wrong type</span></span>  <br/> | <span data-ttu-id="b30df-116">5 + "House"</span><span class="sxs-lookup"><span data-stu-id="b30df-116">5 + "House"</span></span>  <br/> |
| <span data-ttu-id="b30df-117">#REF!</span><span class="sxs-lookup"><span data-stu-id="b30df-117">#REF!</span></span>  <br/> | <span data-ttu-id="b30df-118">Uma referência a uma célula que não existe</span><span class="sxs-lookup"><span data-stu-id="b30df-118">A reference to a cell that does not exist</span></span>  <br/> | <span data-ttu-id="b30df-119">Uma célula que faz referência a uma outra célula que não existe mais</span><span class="sxs-lookup"><span data-stu-id="b30df-119">A cell that refers to another cell that no longer exists</span></span>  <br/> |
| <span data-ttu-id="b30df-120">#NUM!</span><span class="sxs-lookup"><span data-stu-id="b30df-120">#NUM!</span></span>  <br/> | <span data-ttu-id="b30df-121">Um número inválido</span><span class="sxs-lookup"><span data-stu-id="b30df-121">An invalid number</span></span>  <br/> | <span data-ttu-id="b30df-122">Raiz quadrada de um número negativo</span><span class="sxs-lookup"><span data-stu-id="b30df-122">Square root of a negative number</span></span>  <br/> |
| <span data-ttu-id="b30df-123">#N/A!</span><span class="sxs-lookup"><span data-stu-id="b30df-123">#N/A!</span></span>  <br/> | <span data-ttu-id="b30df-124">Não é um valor disponível</span><span class="sxs-lookup"><span data-stu-id="b30df-124">Not an available value</span></span>  <br/> | <span data-ttu-id="b30df-125">Função NA( )</span><span class="sxs-lookup"><span data-stu-id="b30df-125">NA( ) function</span></span>  <br/> |
| <span data-ttu-id="b30df-126">#DIM!</span><span class="sxs-lookup"><span data-stu-id="b30df-126">#DIM!</span></span>  <br/> | <span data-ttu-id="b30df-127">Um valor dimensional que excede o intervalo de dimensão (as potências válidas são \<números inteiros \<-128 = n = 127)</span><span class="sxs-lookup"><span data-stu-id="b30df-127">A dimensional value that exceeds the dimension range (valid powers are integers -128 \<= n \<= 127)</span></span>  <br/> <span data-ttu-id="b30df-128">Um valor dimensional usado com uma operação inadequada</span><span class="sxs-lookup"><span data-stu-id="b30df-128">A dimensional value used with an inappropriate operation</span></span>  <br/> |<span data-ttu-id="b30df-129">1in ^ 100 \* 1in ^ 100 (o resultado é 1in ^ 200, que está além do intervalo de dimensão)</span><span class="sxs-lookup"><span data-stu-id="b30df-129">1in^100 \* 1in^100 (the result is 1in^200, which is beyond the dimension range)</span></span>  <br/> <span data-ttu-id="b30df-130">5,2cm^1,5 (não é uma potência inteira)</span><span class="sxs-lookup"><span data-stu-id="b30df-130">5.2cm^1.5 (not an integer power)</span></span>  <br/> |
   

