---
title: Função PLAYSOUND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
localization_priority: Normal
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: ReProduz um arquivo de som ou som do sistema.
ms.openlocfilehash: 752412aab6584d2b01235fe88644e3ec3fa5daee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435835"
---
# <a name="playsound-function"></a><span data-ttu-id="dc7a0-103">Função PLAYSOUND</span><span class="sxs-lookup"><span data-stu-id="dc7a0-103">PLAYSOUND Function</span></span>

<span data-ttu-id="dc7a0-104">ReProduz um arquivo de som ou som do sistema.</span><span class="sxs-lookup"><span data-stu-id="dc7a0-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dc7a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc7a0-105">Syntax</span></span>

<span data-ttu-id="dc7a0-106">PLAYSOUND ("\* \* *filename* \* *" | "* \* *alias* \* \*", \* \* *IsAlias* \* \*, \* \* *beep* \* \*, \* \* *Synch* \* \*)</span><span class="sxs-lookup"><span data-stu-id="dc7a0-106">PLAYSOUND(" \*\* *filename* \*\* "|" \*\* *alias* \*\* ", \*\* *isAlias* \*\*, \*\* *beep* \*\*, \*\* *synch* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dc7a0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc7a0-107">Parameters</span></span>

|<span data-ttu-id="dc7a0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="dc7a0-108">**Name**</span></span>|<span data-ttu-id="dc7a0-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="dc7a0-109">**Required/Optional**</span></span>|<span data-ttu-id="dc7a0-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="dc7a0-110">**Data Type**</span></span>|<span data-ttu-id="dc7a0-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dc7a0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dc7a0-112">_nomes_</span><span class="sxs-lookup"><span data-stu-id="dc7a0-112">_filename_</span></span> <br/> |<span data-ttu-id="dc7a0-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dc7a0-113">Required</span></span>  <br/> |<span data-ttu-id="dc7a0-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dc7a0-114">**String**</span></span> <br/> |<span data-ttu-id="dc7a0-115">O nome do arquivo de som a ser executado.</span><span class="sxs-lookup"><span data-stu-id="dc7a0-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="dc7a0-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="dc7a0-116">_alias_</span></span> <br/> |<span data-ttu-id="dc7a0-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dc7a0-117">Required</span></span>  <br/> |<span data-ttu-id="dc7a0-118">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dc7a0-118">**String**</span></span> <br/> | <span data-ttu-id="dc7a0-119">Um som de sistema representado por um alias.</span><span class="sxs-lookup"><span data-stu-id="dc7a0-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="dc7a0-120">_isAlias_</span><span class="sxs-lookup"><span data-stu-id="dc7a0-120">_isAlias_</span></span> <br/> |<span data-ttu-id="dc7a0-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dc7a0-121">Required</span></span>  <br/> |<span data-ttu-id="dc7a0-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc7a0-122">**Boolean**</span></span> <br/> | <span data-ttu-id="dc7a0-123">Especifica se a expressão precedente é um alias ou um nome de arquivo; utilize um valor diferente de zero para especificar um alias.</span><span class="sxs-lookup"><span data-stu-id="dc7a0-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="dc7a0-124">_sinais_</span><span class="sxs-lookup"><span data-stu-id="dc7a0-124">_beep_</span></span> <br/> |<span data-ttu-id="dc7a0-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dc7a0-125">Required</span></span>  <br/> |<span data-ttu-id="dc7a0-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc7a0-126">**Boolean**</span></span> <br/> |<span data-ttu-id="dc7a0-127">Especifica se haverá um alarme sonoro do Microsoft Visio quando o som não puder ser reproduzido; utilize um número diferente de zero para o alarme sonoro.</span><span class="sxs-lookup"><span data-stu-id="dc7a0-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="dc7a0-128">_sincroniza_</span><span class="sxs-lookup"><span data-stu-id="dc7a0-128">_synch_</span></span> <br/> |<span data-ttu-id="dc7a0-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dc7a0-129">Required</span></span>  <br/> |<span data-ttu-id="dc7a0-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc7a0-130">**Boolean**</span></span> <br/> |<span data-ttu-id="dc7a0-131">Determina se o som será reproduzido de forma assíncrona (0) ou síncrona (1).</span><span class="sxs-lookup"><span data-stu-id="dc7a0-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc7a0-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc7a0-132">Remarks</span></span>

<span data-ttu-id="dc7a0-133">Geralmente, você deve tocar sons de forma assíncrona para que o Visio possa continuar a processar enquanto o som estiver sendo tocado.</span><span class="sxs-lookup"><span data-stu-id="dc7a0-133">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound.</span></span> <span data-ttu-id="dc7a0-134">Para criar cadeias de caracteres de vários sons juntos, execute-os de forma síncrona ou alguns deles poderão falhar.</span><span class="sxs-lookup"><span data-stu-id="dc7a0-134">To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="dc7a0-135">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc7a0-135">Example 1</span></span>

<span data-ttu-id="dc7a0-136">PLAYSOUND("chord.wav", 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="dc7a0-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="dc7a0-137">Reproduz o arquivo de áudio wave chord.wav de forma assíncrona sem aviso sonoro.</span><span class="sxs-lookup"><span data-stu-id="dc7a0-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="dc7a0-138">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dc7a0-138">Example 2</span></span>

<span data-ttu-id="dc7a0-139">PLAYSOUND("ExclamaçãodeSistema", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="dc7a0-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="dc7a0-140">Reproduz o som de exclamação de sistema de forma assíncrona sem aviso sonoro.</span><span class="sxs-lookup"><span data-stu-id="dc7a0-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

