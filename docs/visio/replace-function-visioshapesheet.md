---
title: Substituir função (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Substitui parte de uma cadeia de texto, baseada no número de caracteres especificado, por uma cadeia de texto diferente.
ms.openlocfilehash: 4112339d772248ac033674808d97c3f9c55b6f0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772684"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="8fbe4-103">Substituir função (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="8fbe4-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="8fbe4-104">Substitui parte de uma sequência de caracteres de texto, baseada no número de caracteres especificado, por uma sequência de caracteres de texto diferente.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8fbe4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fbe4-105">Syntax</span></span>

<span data-ttu-id="8fbe4-106">Substituir (* * *old_text* * *, * * *Núm_inicial* * *, * * *Núm_caract* * *, * * *Novo_texto* * *)</span><span class="sxs-lookup"><span data-stu-id="8fbe4-106">REPLACE (** *old_text* **, ** *start_num* **, ** *num_chars* **, ** *new_text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8fbe4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fbe4-107">Parameters</span></span>

|<span data-ttu-id="8fbe4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8fbe4-108">**Name**</span></span>|<span data-ttu-id="8fbe4-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="8fbe4-109">**Required/Optional**</span></span>|<span data-ttu-id="8fbe4-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="8fbe4-110">**Data Type**</span></span>|<span data-ttu-id="8fbe4-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8fbe4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8fbe4-112">_Texto_antigo_</span><span class="sxs-lookup"><span data-stu-id="8fbe4-112">_old_text_</span></span> <br/> |<span data-ttu-id="8fbe4-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8fbe4-113">Required</span></span>  <br/> |<span data-ttu-id="8fbe4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="8fbe4-114">**String**</span></span> <br/> |<span data-ttu-id="8fbe4-115">O texto no qual você deseja substituir alguns caracteres.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="8fbe4-116">_Núm_inicial_</span><span class="sxs-lookup"><span data-stu-id="8fbe4-116">_start_num_</span></span> <br/> |<span data-ttu-id="8fbe4-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8fbe4-117">Required</span></span>  <br/> |<span data-ttu-id="8fbe4-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="8fbe4-118">**Number**</span></span> <br/> |<span data-ttu-id="8fbe4-119">A posição do caractere em _texto_antigo_ que você deseja substituir por _Novo_texto_.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="8fbe4-120">O primeiro caractere na cadeia de caracteres é a posição 1.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="8fbe4-121">_Núm_caract_</span><span class="sxs-lookup"><span data-stu-id="8fbe4-121">_num_chars_</span></span> <br/> |<span data-ttu-id="8fbe4-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8fbe4-122">Required</span></span>  <br/> |<span data-ttu-id="8fbe4-123">**Número**</span><span class="sxs-lookup"><span data-stu-id="8fbe4-123">**Number**</span></span> <br/> |<span data-ttu-id="8fbe4-124">O número de caracteres em _texto_antigo_ que você deseja substituir</span><span class="sxs-lookup"><span data-stu-id="8fbe4-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="8fbe4-125">_Novo_texto_</span><span class="sxs-lookup"><span data-stu-id="8fbe4-125">_new_text_</span></span> <br/> |<span data-ttu-id="8fbe4-126">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8fbe4-126">Required</span></span>  <br/> |<span data-ttu-id="8fbe4-127">**String**</span><span class="sxs-lookup"><span data-stu-id="8fbe4-127">**String**</span></span> <br/> |<span data-ttu-id="8fbe4-128">O texto que substituirá os caracteres em _texto_antigo_.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8fbe4-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8fbe4-129">Return value</span></span>

<span data-ttu-id="8fbe4-130">String</span><span class="sxs-lookup"><span data-stu-id="8fbe4-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8fbe4-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fbe4-131">Remarks</span></span>

<span data-ttu-id="8fbe4-p102">Use a função REPLACE para substituir o texto que ocorre em um determinado local da sequência de texto. Para substituir um texto específico na sequência de texto, use a função SUBSTITUTE.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-p102">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string. If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="8fbe4-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8fbe4-134">Example</span></span>

<span data-ttu-id="8fbe4-135">REPLACE ("01/03/2002",9,2,"03")</span><span class="sxs-lookup"><span data-stu-id="8fbe4-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="8fbe4-136">Retornará 01/03/2003.</span><span class="sxs-lookup"><span data-stu-id="8fbe4-136">Returns 01/03/2003.</span></span> 
  

