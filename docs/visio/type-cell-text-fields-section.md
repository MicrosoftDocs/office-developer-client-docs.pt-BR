---
title: Célula Type (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: Especifica um tipo de dados para o campo de texto.
ms.openlocfilehash: 91a2d60133d9a39e152656558f168742a5409883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407981"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="1a627-103">Célula Type (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="1a627-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="1a627-104">Especifica um tipo de dados para o campo de texto.</span><span class="sxs-lookup"><span data-stu-id="1a627-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="1a627-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1a627-105">**Value**</span></span>|<span data-ttu-id="1a627-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1a627-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a627-107">0</span><span class="sxs-lookup"><span data-stu-id="1a627-107">0</span></span>  <br/> |<span data-ttu-id="1a627-108">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1a627-108">String.</span></span>  <br/> |
|<span data-ttu-id="1a627-109">2 </span><span class="sxs-lookup"><span data-stu-id="1a627-109">2</span></span>  <br/> |<span data-ttu-id="1a627-p101">Número. Inclui valores de data, hora, duração e moeda, bem como grandezas escalares, dimensões e ângulos. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="1a627-p101">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="1a627-113">5 </span><span class="sxs-lookup"><span data-stu-id="1a627-113">5</span></span>  <br/> |<span data-ttu-id="1a627-p102">Valor de data ou hora. Exibe dias, meses e anos ou segundos, minutos e horas ou, ainda, um valor combinado de data e hora. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="1a627-p102">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="1a627-117">6 </span><span class="sxs-lookup"><span data-stu-id="1a627-117">6</span></span>  <br/> |<span data-ttu-id="1a627-p103">Valor de duração. Exibe o tempo decorrido. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="1a627-p103">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="1a627-121">7 </span><span class="sxs-lookup"><span data-stu-id="1a627-121">7</span></span>  <br/> |<span data-ttu-id="1a627-p104">Valor de moeda. Utiliza as configurações regionais de moeda do sistema. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="1a627-p104">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a627-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a627-125">Remarks</span></span>

<span data-ttu-id="1a627-126">Você também pode definir o valor  dessa célula usando a caixa  de diálogo Campo  (com uma forma selecionada, na guia Inserir, no grupo Texto, clique em **Campo** ).</span><span class="sxs-lookup"><span data-stu-id="1a627-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="1a627-127">Para obter uma referência à célula Type pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="1a627-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a627-128">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="1a627-128">Cell name:</span></span>  <br/> |<span data-ttu-id="1a627-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1a627-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1a627-130">Para obter uma referência para a célula Type pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="1a627-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a627-131">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="1a627-131">Section index:</span></span>  <br/> |<span data-ttu-id="1a627-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="1a627-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="1a627-133">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="1a627-133">Row index:</span></span>  <br/> |<span data-ttu-id="1a627-134">**visRowField**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1a627-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="1a627-135">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="1a627-135">Cell index:</span></span>  <br/> |<span data-ttu-id="1a627-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="1a627-136">**visFieldType**</span></span> <br/> |
   

