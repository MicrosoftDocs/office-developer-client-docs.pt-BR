---
title: Sobre Fórmulas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: A chave para controlar ações de forma é gravar fórmulas que definam o comportamento desejado. É possível editar uma fórmula de célula para alterar o valor da célula e, como resultado, modificar um determinado comportamento da forma. Por exemplo, a célula Height da seção Shape Transform contém uma fórmula que pode ser alterada para modificar a altura da forma.
ms.openlocfilehash: e8e1a2b77cc355e930af6f31f0b375dfba321e74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426258"
---
# <a name="about-formulas"></a><span data-ttu-id="0270d-105">Sobre Fórmulas</span><span class="sxs-lookup"><span data-stu-id="0270d-105">About Formulas</span></span>

<span data-ttu-id="0270d-p102">A chave para controlar ações de forma é gravar fórmulas que definam o comportamento desejado. É possível editar uma fórmula de célula para alterar o valor da célula e, como resultado, modificar um determinado comportamento da forma. Por exemplo, a célula Height da seção Shape Transform contém uma fórmula que pode ser alterada para modificar a altura da forma.</span><span class="sxs-lookup"><span data-stu-id="0270d-p102">The key to controlling shape actions is to write formulas that define the behavior you want. You can edit a cell's formula to change the value of the cell and, as a result, change a particular shape's behavior. For example, the Height cell in the Shape Transform section contains a formula that you can change to alter the shape's height.</span></span>
  
<span data-ttu-id="0270d-p103">As fórmulas do Microsoft Visio são semelhantes às fórmulas de planilhas comuns em diversos aspectos. O Visio considera tudo na célula, mesmo que seja um valor numérico ou uma simples referência de célula, como uma fórmula.</span><span class="sxs-lookup"><span data-stu-id="0270d-p103">Microsoft Visio formulas are similar to typical spreadsheet formulas in many ways. Visio regards anything in a cell, even if it is a numeric value or simple cell reference, as a formula.</span></span>
  
<span data-ttu-id="0270d-p104">A fórmula em uma célula pode ser herdada da célula equivalente de um mestre ou de um estilo, ou pode ser definida localmente. O Visio avalia a fórmula e converte os resultados para o valor e as unidades apropriados para a célula. Em uma janela do ShapeSheet, você pode exibir o conteúdo da célula como fórmulas ou valores.</span><span class="sxs-lookup"><span data-stu-id="0270d-p104">A formula in a cell can be inherited from the equivalent cell of a master or a style or defined locally. Visio evaluates the formula and then converts the results to an appropriate value and appropriate units for the cell. In a ShapeSheet window, you can display cell contents as either formulas or values.</span></span>
  
## <a name="elements-of-a-formula"></a><span data-ttu-id="0270d-114">Elementos de uma fórmula</span><span class="sxs-lookup"><span data-stu-id="0270d-114">Elements of a formula</span></span>

<span data-ttu-id="0270d-p105">Uma fórmula sempre começa com um sinal de igual, inserido automaticamente, e pode conter qualquer um dos elementos a seguir:</span><span class="sxs-lookup"><span data-stu-id="0270d-p105">A formula always starts with an equal sign, which is inserted automatically. A formula can include any of the following elements:</span></span>
  
- <span data-ttu-id="0270d-117">Números</span><span class="sxs-lookup"><span data-stu-id="0270d-117">Numbers</span></span>
    
- <span data-ttu-id="0270d-118">Coordenadas</span><span class="sxs-lookup"><span data-stu-id="0270d-118">Coordinates</span></span>
    
- <span data-ttu-id="0270d-119">Valores booleanos</span><span class="sxs-lookup"><span data-stu-id="0270d-119">Boolean values</span></span>
    
- <span data-ttu-id="0270d-120">Operadores</span><span class="sxs-lookup"><span data-stu-id="0270d-120">Operators</span></span>
    
- <span data-ttu-id="0270d-121">Funções</span><span class="sxs-lookup"><span data-stu-id="0270d-121">Functions</span></span>
    
- <span data-ttu-id="0270d-122">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="0270d-122">Strings</span></span>
    
- <span data-ttu-id="0270d-123">Referências de célula</span><span class="sxs-lookup"><span data-stu-id="0270d-123">Cell references</span></span>
    
- <span data-ttu-id="0270d-124">Unidades de medida</span><span class="sxs-lookup"><span data-stu-id="0270d-124">Units of measure</span></span>
    
## <a name="default-formulas"></a><span data-ttu-id="0270d-125">Fórmulas padrão</span><span class="sxs-lookup"><span data-stu-id="0270d-125">Default formulas</span></span>

<span data-ttu-id="0270d-p106">Como padrão, quando você cria uma forma, o Visio cria fórmulas para ela. Para ver quais são essas fórmulas padrão, desenhe uma forma simples (como um retângulo, uma elipse ou uma linha reta) e abra sua janela do ShapeSheet (na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md), clique em **Mostrar ShapeSheet**).</span><span class="sxs-lookup"><span data-stu-id="0270d-p106">When you create a shape, Visio creates formulas for it by default. To see what the default formulas are, draw a simple shape (such as a rectangle, ellipse, or straight line) and open its ShapeSheet window (on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, click **Show ShapeSheet**).</span></span>
  
## <a name="inherited-formulas"></a><span data-ttu-id="0270d-128">Fórmulas herdadas</span><span class="sxs-lookup"><span data-stu-id="0270d-128">Inherited formulas</span></span>

<span data-ttu-id="0270d-p107">O Visio herda as fórmulas sempre que possível. Em vez de fazer uma cópia local de cada fórmula na instância, uma instância herda as fórmulas de seu mestre no estêncil do documento e a formatação da definição de estilo armazenada com o desenho. Esse comportamento resulta em arquivos menores, mas também permite fazer alterações nas fórmulas do mestre ou na definição de estilo para serem propagadas a todas as instâncias.</span><span class="sxs-lookup"><span data-stu-id="0270d-p107">Visio inherits formulas whenever possible. Rather than make a local copy of every formula in the instance, an instance inherits formulas from its master on the document stencil and inherits formatting from the style definition stored with the drawing. This behavior results in smaller files, but also allows changes to the master's formulas or the style definition to be propagated to all instances.</span></span>
  
<span data-ttu-id="0270d-132">O texto preto em uma célula indica uma fórmula herdada.</span><span class="sxs-lookup"><span data-stu-id="0270d-132">Black text in a cell indicates an inherited formula.</span></span>
  
## <a name="local-formulas"></a><span data-ttu-id="0270d-133">Fórmulas locais</span><span class="sxs-lookup"><span data-stu-id="0270d-133">Local formulas</span></span>

<span data-ttu-id="0270d-p108">Ao gravar uma fórmula local para uma instância, você está substituindo a fórmula herdada na célula por uma substituição local. Futuras alterações nessa célula no mestre ou no estilo não afetam essa instância porque ela tem uma herança protegida para a célula com a substituição local.</span><span class="sxs-lookup"><span data-stu-id="0270d-p108">When you write a local formula for an instance, you are replacing the inherited formula in the cell with a local override. Future changes to that cell in the master or style do not affect this instance because it has blocked inheritance for the cell with the local override.</span></span>
  
<span data-ttu-id="0270d-136">A aplicação de um estilo exclui todas as fórmulas locais nas células relacionadas, a menos que você use a função GUARD para protegê-las.</span><span class="sxs-lookup"><span data-stu-id="0270d-136">Applying a style deletes all local formulas in the related cells unless you use the GUARD function to protect them.</span></span>
  
<span data-ttu-id="0270d-137">O texto azul indica uma fórmula local, que pode ser o resultado da edição da fórmula em uma janela ShapeSheet ou alguma alteração na forma que fez com que o Visio redefinisse a fórmula da célula.</span><span class="sxs-lookup"><span data-stu-id="0270d-137">Blue text indicates a local formula, either the result of editing the formula in a ShapeSheet window or some change to the shape that caused Visio to reset the formula for that cell.</span></span>
  
## <a name="automatic-updates-to-formulas"></a><span data-ttu-id="0270d-138">Atualizações automáticas das fórmulas</span><span class="sxs-lookup"><span data-stu-id="0270d-138">Automatic updates to formulas</span></span>

 <span data-ttu-id="0270d-p109">O Visio atualiza automaticamente determinadas células sempre que uma forma for alterada em um desenho. Isso significa que, em certas circunstâncias, as fórmulas inseridas podem ser substituídas. Por exemplo, se você arrastar a alça do canto para redimensionar uma forma, o Visio redefinirá as fórmulas nas células PinX, PinY, Width e Height.</span><span class="sxs-lookup"><span data-stu-id="0270d-p109">Visio automatically updates certain cells whenever you change a shape in a drawing. This means that under some circumstances formulas you enter can be replaced. For example, if you drag a corner handle to resize a shape, Visio resets formulas in the PinX, PinY, Width, and Height cells.</span></span> 
  
<span data-ttu-id="0270d-142">Se necessário, proteja as fórmulas contra alterações utilizando a função GUARD.</span><span class="sxs-lookup"><span data-stu-id="0270d-142">If necessary, you can protect formulas against changes by using the GUARD function.</span></span>
  

