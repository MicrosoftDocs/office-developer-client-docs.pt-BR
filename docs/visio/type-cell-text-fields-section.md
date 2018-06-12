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
description: Especifica um tipo de dado para o valor do campo de texto.
ms.openlocfilehash: 68bfa8a84adb0d46d9621e6fc5383f4b6606f542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773197"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="f6c6e-103">Célula Type (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="f6c6e-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="f6c6e-104">Especifica um tipo de dado para o valor do campo de texto.</span><span class="sxs-lookup"><span data-stu-id="f6c6e-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="f6c6e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f6c6e-105">**Value**</span></span>|<span data-ttu-id="f6c6e-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f6c6e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6c6e-107">0</span><span class="sxs-lookup"><span data-stu-id="f6c6e-107">0</span></span>  <br/> |<span data-ttu-id="f6c6e-108">Sequência de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f6c6e-108">String.</span></span>  <br/> |
|<span data-ttu-id="f6c6e-109">2</span><span class="sxs-lookup"><span data-stu-id="f6c6e-109">2</span></span>  <br/> |<span data-ttu-id="f6c6e-p101">Número. Inclui valores de data, hora, duração e moeda, bem como grandezas escalares, dimensões e ângulos. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="f6c6e-p101">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="f6c6e-113">5</span><span class="sxs-lookup"><span data-stu-id="f6c6e-113">5</span></span>  <br/> |<span data-ttu-id="f6c6e-p102">Valor de data ou hora. Exibe dias, meses e anos ou segundos, minutos e horas ou, ainda, um valor combinado de data e hora. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="f6c6e-p102">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="f6c6e-117">6</span><span class="sxs-lookup"><span data-stu-id="f6c6e-117">6</span></span>  <br/> |<span data-ttu-id="f6c6e-p103">Valor de duração. Exibe o tempo decorrido. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="f6c6e-p103">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="f6c6e-121">7</span><span class="sxs-lookup"><span data-stu-id="f6c6e-121">7</span></span>  <br/> |<span data-ttu-id="f6c6e-p104">Valor de moeda. Utiliza as configurações regionais de moeda do sistema. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="f6c6e-p104">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6c6e-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6c6e-125">Remarks</span></span>

<span data-ttu-id="f6c6e-126">Você também pode definir o valor desta célula usando a caixa de diálogo **campo** (com a forma selecionada, na guia **Inserir** , no grupo **texto** , clique em **campo** ).</span><span class="sxs-lookup"><span data-stu-id="f6c6e-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="f6c6e-127">Para obter uma referência à célula Type pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="f6c6e-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6c6e-128">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f6c6e-128">Cell name:</span></span>  <br/> |<span data-ttu-id="f6c6e-129">Fields.Type [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f6c6e-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f6c6e-130">Para obter uma referência à célula Type pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f6c6e-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6c6e-131">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f6c6e-131">Section index:</span></span>  <br/> |<span data-ttu-id="f6c6e-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="f6c6e-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="f6c6e-133">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f6c6e-133">Row index:</span></span>  <br/> |<span data-ttu-id="f6c6e-134">**visRowField** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f6c6e-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f6c6e-135">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f6c6e-135">Cell index:</span></span>  <br/> |<span data-ttu-id="f6c6e-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="f6c6e-136">**visFieldType**</span></span> <br/> |
   

