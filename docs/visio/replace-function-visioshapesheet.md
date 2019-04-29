---
title: Função REPLACE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Substitui parte de uma sequência de caracteres de texto, baseada no número de caracteres especificado, por uma sequência de caracteres de texto diferente.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414351"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="e5ff0-103">Função REPLACE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="e5ff0-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="e5ff0-104">Substitui parte de uma sequência de caracteres de texto, baseada no número de caracteres especificado, por uma sequência de caracteres de texto diferente.</span><span class="sxs-lookup"><span data-stu-id="e5ff0-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e5ff0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5ff0-105">Syntax</span></span>

<span data-ttu-id="e5ff0-106">REPLACE (\* \* *texto_antigo* \* \*, \* \* *Núm_inicial* \* \*, \* \* *Núm_caract* \* \*, \* \* *novo_texto* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e5ff0-106">REPLACE (\*\* *old_text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\*, \*\* *new_text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e5ff0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5ff0-107">Parameters</span></span>

|<span data-ttu-id="e5ff0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5ff0-108">**Name**</span></span>|<span data-ttu-id="e5ff0-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="e5ff0-109">**Required/Optional**</span></span>|<span data-ttu-id="e5ff0-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e5ff0-110">**Data Type**</span></span>|<span data-ttu-id="e5ff0-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e5ff0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e5ff0-112">_iguais_</span><span class="sxs-lookup"><span data-stu-id="e5ff0-112">_old_text_</span></span> <br/> |<span data-ttu-id="e5ff0-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e5ff0-113">Required</span></span>  <br/> |<span data-ttu-id="e5ff0-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e5ff0-114">**String**</span></span> <br/> |<span data-ttu-id="e5ff0-115">O texto no qual você deseja substituir alguns caracteres.</span><span class="sxs-lookup"><span data-stu-id="e5ff0-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="e5ff0-116">_núm_inicial_</span><span class="sxs-lookup"><span data-stu-id="e5ff0-116">_start_num_</span></span> <br/> |<span data-ttu-id="e5ff0-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e5ff0-117">Required</span></span>  <br/> |<span data-ttu-id="e5ff0-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="e5ff0-118">**Number**</span></span> <br/> |<span data-ttu-id="e5ff0-119">A posição do caractere em _texto_antigo_ que você deseja substituir por _novo_texto_.</span><span class="sxs-lookup"><span data-stu-id="e5ff0-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="e5ff0-120">O primeiro caractere na cadeia é a posição 1.</span><span class="sxs-lookup"><span data-stu-id="e5ff0-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="e5ff0-121">_Núm_caract_</span><span class="sxs-lookup"><span data-stu-id="e5ff0-121">_num_chars_</span></span> <br/> |<span data-ttu-id="e5ff0-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e5ff0-122">Required</span></span>  <br/> |<span data-ttu-id="e5ff0-123">**Número**</span><span class="sxs-lookup"><span data-stu-id="e5ff0-123">**Number**</span></span> <br/> |<span data-ttu-id="e5ff0-124">O número de caracteres em _texto_antigo_ que você deseja substituir</span><span class="sxs-lookup"><span data-stu-id="e5ff0-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="e5ff0-125">_novo_texto_</span><span class="sxs-lookup"><span data-stu-id="e5ff0-125">_new_text_</span></span> <br/> |<span data-ttu-id="e5ff0-126">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e5ff0-126">Required</span></span>  <br/> |<span data-ttu-id="e5ff0-127">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e5ff0-127">**String**</span></span> <br/> |<span data-ttu-id="e5ff0-128">O texto que substituirá os caracteres em _texto_antigo_.</span><span class="sxs-lookup"><span data-stu-id="e5ff0-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e5ff0-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e5ff0-129">Return value</span></span>

<span data-ttu-id="e5ff0-130">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="e5ff0-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5ff0-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5ff0-131">Remarks</span></span>

<span data-ttu-id="e5ff0-p102">Use a função REPLACE para substituir o texto que ocorre em um determinado local da sequência de texto. Para substituir um texto específico na sequência de texto, use a função SUBSTITUTE.</span><span class="sxs-lookup"><span data-stu-id="e5ff0-p102">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string. If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="e5ff0-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e5ff0-134">Example</span></span>

<span data-ttu-id="e5ff0-135">REPLACE ("01/03/2002",9,2,"03")</span><span class="sxs-lookup"><span data-stu-id="e5ff0-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="e5ff0-136">Retornará 01/03/2003.</span><span class="sxs-lookup"><span data-stu-id="e5ff0-136">Returns 01/03/2003.</span></span> 
  

