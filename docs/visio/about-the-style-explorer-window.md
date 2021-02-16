---
title: Sobre a Janela Gerenciador de Estilo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60119
localization_priority: Normal
ms.assetid: bfdc1a63-c355-c759-bdfa-ce27e3ad10e7
description: A janela Gerenciador de Estilo fornece aos desenvolvedores de formas uma maneira rápida de determinar quais as células de formas que herdam valores de um determinado estilo, ou o estilo do qual uma determinada célula herda seu valor.
ms.openlocfilehash: 55800b692443bae3720b433e5a6178f2709d3675
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431782"
---
# <a name="about-the-style-explorer-window"></a><span data-ttu-id="fc523-103">Sobre a janela do Gerenciador de Estilo</span><span class="sxs-lookup"><span data-stu-id="fc523-103">About the Style Explorer Window</span></span>

<span data-ttu-id="fc523-104">A janela **Gerenciador de Estilo** fornece aos desenvolvedores de formas uma maneira rápida de determinar quais as células de formas que herdam valores de um determinado estilo, ou o estilo do qual uma determinada célula herda seu valor.</span><span class="sxs-lookup"><span data-stu-id="fc523-104">The **Style Explorer** window provides shape developers with a quick way to determine which shape cells inherit from a given style, or the style from which a given cell inherits its value.</span></span> 
  
<span data-ttu-id="fc523-p101">Os estilos são denominados coleções de atributos de formatação que você pode aplicar a uma forma. No Microsoft Visio, um único estilo pode definir texto, linha e atributos de preenchimento como uma maneira eficiente de garantir consistência nas formas. Além disso, é possível definir ainda um estilo para qualquer classe de atributo (texto, linha ou preenchimento) ou qualquer combinação de atributos.</span><span class="sxs-lookup"><span data-stu-id="fc523-p101">Styles are named collections of formatting attributes that you can apply to a shape. In Microsoft Visio, a single style can define text, line, and fill attributes as an efficient way to ensure consistency in your shapes. Additionally, you can also define a style for any one class of attribute (text, line, or fill) or any combination of attributes.</span></span> 
  
<span data-ttu-id="fc523-108">Ao contrário das formas às quais você aplicou os atributos de formatação individualmente, as formas cuja formatação provém de um estilo não apenas garantem a consistência mas também reagem melhor quando são criadas, movidas, dimensionadas ou giradas.</span><span class="sxs-lookup"><span data-stu-id="fc523-108">Unlike shapes to which you've applied formatting attributes individually, shapes that derive their formatting from a style not only ensure consistency but also respond better when they are created, moved, scaled, or rotated.</span></span> 
  
<span data-ttu-id="fc523-109">A **janela Do Explorador** de Estilo fornece as informações de que você precisa para entender melhor as implicações das alterações feitas nas formas.</span><span class="sxs-lookup"><span data-stu-id="fc523-109">The **Style Explorer** window provides the information you need to understand better the implications of changes you make to shapes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fc523-110">Os valores das células que aparecem em preto na janela ShapeSheet são herdados; os que aparecem em azul são locais.</span><span class="sxs-lookup"><span data-stu-id="fc523-110">Cell values that appear black in the ShapeSheet window are inherited; those that appear blue are local.</span></span> 
  
## <a name="using-the-style-explorer-window"></a><span data-ttu-id="fc523-111">Usando a janela Gerenciador de Estilo</span><span class="sxs-lookup"><span data-stu-id="fc523-111">Using the Style Explorer window</span></span>

<span data-ttu-id="fc523-112">Para exibir a **janela Do Explorador** de Estilos, com a janela ShapeSheet ativa, na guia Design de Ferramentas do **ShapeSheet,** no grupo Exibir, selecione **Explorer de Estilo.** </span><span class="sxs-lookup"><span data-stu-id="fc523-112">To view the **Style Explorer** window, with the ShapeSheet window active, on the **ShapeSheet Tools Design** tab, in the **View** group, select **Style Explorer**.</span></span> <span data-ttu-id="fc523-113">A janela **Do** Explorador de Estilo aparece encaixada na janela ShapeSheet por padrão, mas é uma janela ancorada que pode ser encaixada, flutuante ou mesclada com outras janelas ShapeSheet ancoradas disponíveis, por exemplo, a janela Rastreamento de Fórmula. </span><span class="sxs-lookup"><span data-stu-id="fc523-113">The **Style Explorer** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated, or merged with other available anchored ShapeSheet windows, for example, the **Formula Tracing** window.</span></span> <span data-ttu-id="fc523-114">A janela **Gerenciador de Estilo** contém um modo de exibição em árvore de todos os estilos definidos no desenho atual.</span><span class="sxs-lookup"><span data-stu-id="fc523-114">The **Style Explorer** window contains a treeview display of all the styles defined in the current drawing.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fc523-115">Para obter informações sobre um estilo, clique com o botão direito do mouse no estilo na janela **Gerenciador de Estilo** para exibir sua ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fc523-115">To get information about a style, you can right-click the style in the **Style Explorer** window to view its ShapeSheet.</span></span> 
  
<span data-ttu-id="fc523-116">A janela **Gerenciador de Estilo** fornece as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="fc523-116">The **Style Explorer** window provides the following information:</span></span> 
  
- <span data-ttu-id="fc523-117">As células cujos valores são herdados de um estilo selecionado.Quando você seleciona um estilo na janela **Gerenciador de Estilo**, todas as células da janela ShapeSheet que herdam seus valores desse estilo são exibidas sem hachura, e as células que não herdam valores desse estilo são exibidas com uma ligeira hachura.</span><span class="sxs-lookup"><span data-stu-id="fc523-117">The cells that inherit their values from a selected style.When you select a style in the **Style Explorer** window, all cells in the ShapeSheet window that inherit from that style appear without hatching, while cells that do not inherit from that style appear lightly hatched.</span></span> 
    
- <span data-ttu-id="fc523-118">O estilo do qual uma célula selecionada herda seu valor.Quando você seleciona uma célula na ShapeSheet, o estilo do qual ela herda seu valor é é exibido na barra de tarefas abaixo da janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fc523-118">The style from which a selected cell inherits its value.When you select a ShapeSheet cell, the style from which it inherits its value is displayed on the taskbar under the ShapeSheet window.</span></span> 
    

