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
description: A janela Gerenciador de estilo fornece aos desenvolvedores de formas uma maneira rápida para determinar quais células de forma herdam um dado estilo, ou o estilo do qual uma determinada célula herda seu valor.
ms.openlocfilehash: 25af478b8ac4e35c7ae0b88bf69aad21d679da17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771225"
---
# <a name="about-the-style-explorer-window"></a><span data-ttu-id="16270-103">Sobre a Janela Gerenciador de Estilo</span><span class="sxs-lookup"><span data-stu-id="16270-103">About the Style Explorer Window</span></span>

<span data-ttu-id="16270-104">A janela **Gerenciador de estilo** fornece aos desenvolvedores de formas uma maneira rápida para determinar quais células de forma herdam um dado estilo, ou o estilo do qual uma determinada célula herda seu valor.</span><span class="sxs-lookup"><span data-stu-id="16270-104">The **Style Explorer** window provides shape developers with a quick way to determine which shape cells inherit from a given style, or the style from which a given cell inherits its value.</span></span> 
  
<span data-ttu-id="16270-p101">Os estilos são denominados coleções de atributos de formatação que você pode aplicar a uma forma. No Microsoft Visio, um único estilo pode definir texto, linha e atributos de preenchimento como uma maneira eficiente de garantir consistência nas formas. Além disso, é possível definir ainda um estilo para qualquer classe de atributo (texto, linha ou preenchimento) ou qualquer combinação de atributos.</span><span class="sxs-lookup"><span data-stu-id="16270-p101">Styles are named collections of formatting attributes that you can apply to a shape. In Microsoft Visio, a single style can define text, line, and fill attributes as an efficient way to ensure consistency in your shapes. Additionally, you can also define a style for any one class of attribute (text, line, or fill) or any combination of attributes.</span></span> 
  
<span data-ttu-id="16270-108">Ao contrário das formas às quais você aplicou os atributos de formatação individualmente, as formas cuja formatação provém de um estilo não apenas garantem a consistência mas também reagem melhor quando são criadas, movidas, dimensionadas ou giradas.</span><span class="sxs-lookup"><span data-stu-id="16270-108">Unlike shapes to which you've applied formatting attributes individually, shapes that derive their formatting from a style not only ensure consistency but also respond better when they are created, moved, scaled, or rotated.</span></span> 
  
<span data-ttu-id="16270-109">A janela **Gerenciador de estilo** fornece as informações que você precisa entender melhor as implicações das alterações que faz nas formas.</span><span class="sxs-lookup"><span data-stu-id="16270-109">The **Style Explorer** window provides the information you need to understand better the implications of changes you make to shapes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="16270-110">Os valores das células que aparecem em preto na janela ShapeSheet são herdados; os que aparecem em azul são locais.</span><span class="sxs-lookup"><span data-stu-id="16270-110">Cell values that appear black in the ShapeSheet window are inherited; those that appear blue are local.</span></span> 
  
## <a name="using-the-style-explorer-window"></a><span data-ttu-id="16270-111">Usando a janela Gerenciador de Estilo</span><span class="sxs-lookup"><span data-stu-id="16270-111">Using the Style Explorer window</span></span>

<span data-ttu-id="16270-112">Para exibir a janela do **Gerenciador de estilo** , com a janela ShapeSheet ativa, na guia **Design de ferramentas do ShapeSheet** , no grupo **Exibir** , selecione **Gerenciador de estilo**.</span><span class="sxs-lookup"><span data-stu-id="16270-112">To view the **Style Explorer** window, with the ShapeSheet window active, on the **ShapeSheet Tools Design** tab, in the **View** group, select **Style Explorer**.</span></span> <span data-ttu-id="16270-113">A janela **Gerenciador de estilo** é exibida encaixada na janela ShapeSheet por padrão, mas é uma janela ancorada que pode ser encaixada, flutuada ou combinada com outras disponíveis janelas ShapeSheet ancoradas, por exemplo, a janela **Rastreamento de fórmula** .</span><span class="sxs-lookup"><span data-stu-id="16270-113">The **Style Explorer** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated, or merged with other available anchored ShapeSheet windows, for example, the **Formula Tracing** window.</span></span> <span data-ttu-id="16270-114">A janela **Gerenciador de estilo** contém uma exibição em árvore de todos os estilos definidos no desenho atual.</span><span class="sxs-lookup"><span data-stu-id="16270-114">The **Style Explorer** window contains a treeview display of all the styles defined in the current drawing.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="16270-115">Para obter informações sobre um estilo, você pode com o botão direito no estilo na janela **Gerenciador** de estilo para exibir sua ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="16270-115">To get information about a style, you can right-click the style in the **Style Explorer** window to view its ShapeSheet.</span></span> 
  
<span data-ttu-id="16270-116">A janela **Gerenciador de estilo** fornece as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="16270-116">The **Style Explorer** window provides the following information:</span></span> 
  
- <span data-ttu-id="16270-117">As células que herdam seus valores de um estilo selecionado. Quando você seleciona um estilo na janela **Gerenciador de estilo** , todas as células na janela ShapeSheet que herdam desse estilo aparecem sem hachura, enquanto as células que não herdam desse estilo aparecem com uma ligeira hachura.</span><span class="sxs-lookup"><span data-stu-id="16270-117">The cells that inherit their values from a selected style.When you select a style in the **Style Explorer** window, all cells in the ShapeSheet window that inherit from that style appear without hatching, while cells that do not inherit from that style appear lightly hatched.</span></span> 
    
- <span data-ttu-id="16270-118">O estilo do qual uma célula selecionada herda seu valor.Quando você seleciona uma célula na ShapeSheet, o estilo do qual ela herda seu valor é é exibido na barra de tarefas abaixo da janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="16270-118">The style from which a selected cell inherits its value.When you select a ShapeSheet cell, the style from which it inherits its value is displayed on the taskbar under the ShapeSheet window.</span></span> 
    

