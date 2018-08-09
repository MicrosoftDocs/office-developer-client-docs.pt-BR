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
description: Reproduz um arquivo de som ou som do sistema.
ms.openlocfilehash: ca54b749b764e9ea2c7db71d41268303542417f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772522"
---
# <a name="playsound-function"></a><span data-ttu-id="3eab5-103">Função PLAYSOUND</span><span class="sxs-lookup"><span data-stu-id="3eab5-103">PLAYSOUND Function</span></span>

<span data-ttu-id="3eab5-104">Reproduz um arquivo de som ou som do sistema.</span><span class="sxs-lookup"><span data-stu-id="3eab5-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3eab5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3eab5-105">Syntax</span></span>

<span data-ttu-id="3eab5-106">PLAYSOUND ("* * *filename* * *" | "* * *alias* * *", * * *isAlias* * *, * * *AlarmeSonoro* * *, * * *synch* * *)</span><span class="sxs-lookup"><span data-stu-id="3eab5-106">PLAYSOUND(" ** *filename* ** "|" ** *alias* ** ", ** *isAlias* **, ** *beep* **, ** *synch* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3eab5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3eab5-107">Parameters</span></span>

|<span data-ttu-id="3eab5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3eab5-108">**Name**</span></span>|<span data-ttu-id="3eab5-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="3eab5-109">**Required/Optional**</span></span>|<span data-ttu-id="3eab5-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="3eab5-110">**Data Type**</span></span>|<span data-ttu-id="3eab5-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3eab5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3eab5-112">_FileName_</span><span class="sxs-lookup"><span data-stu-id="3eab5-112">_filename_</span></span> <br/> |<span data-ttu-id="3eab5-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3eab5-113">Required</span></span>  <br/> |<span data-ttu-id="3eab5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="3eab5-114">**String**</span></span> <br/> |<span data-ttu-id="3eab5-115">O nome do arquivo de som a ser executado.</span><span class="sxs-lookup"><span data-stu-id="3eab5-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="3eab5-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="3eab5-116">_alias_</span></span> <br/> |<span data-ttu-id="3eab5-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3eab5-117">Required</span></span>  <br/> |<span data-ttu-id="3eab5-118">**String**</span><span class="sxs-lookup"><span data-stu-id="3eab5-118">**String**</span></span> <br/> | <span data-ttu-id="3eab5-119">Um som de sistema representado por um alias.</span><span class="sxs-lookup"><span data-stu-id="3eab5-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="3eab5-120">_isAlias_</span><span class="sxs-lookup"><span data-stu-id="3eab5-120">_isAlias_</span></span> <br/> |<span data-ttu-id="3eab5-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3eab5-121">Required</span></span>  <br/> |<span data-ttu-id="3eab5-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3eab5-122">**Boolean**</span></span> <br/> | <span data-ttu-id="3eab5-123">Especifica se a expressão precedente é um alias ou um nome de arquivo; utilize um valor diferente de zero para especificar um alias.</span><span class="sxs-lookup"><span data-stu-id="3eab5-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="3eab5-124">_alarme sonoro_</span><span class="sxs-lookup"><span data-stu-id="3eab5-124">_beep_</span></span> <br/> |<span data-ttu-id="3eab5-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3eab5-125">Required</span></span>  <br/> |<span data-ttu-id="3eab5-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3eab5-126">**Boolean**</span></span> <br/> |<span data-ttu-id="3eab5-127">Especifica se haverá um alarme sonoro do Microsoft Visio quando o som não puder ser reproduzido; utilize um número diferente de zero para o alarme sonoro.</span><span class="sxs-lookup"><span data-stu-id="3eab5-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="3eab5-128">_sincronização_</span><span class="sxs-lookup"><span data-stu-id="3eab5-128">_synch_</span></span> <br/> |<span data-ttu-id="3eab5-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3eab5-129">Required</span></span>  <br/> |<span data-ttu-id="3eab5-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3eab5-130">**Boolean**</span></span> <br/> |<span data-ttu-id="3eab5-131">Determina se o som será reproduzido de forma assíncrona (0) ou síncrona (1).</span><span class="sxs-lookup"><span data-stu-id="3eab5-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3eab5-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="3eab5-132">Remarks</span></span>

<span data-ttu-id="3eab5-p101">Geralmente, você deve tocar sons de forma assíncrona para que o Visio possa continuar a processar enquanto o som estiver sendo tocado. Para criar cadeias de caracteres de vários sons juntos, execute-os de forma síncrona ou alguns deles poderão falhar.
</span><span class="sxs-lookup"><span data-stu-id="3eab5-p101">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound. To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="3eab5-135">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3eab5-135">Example 1</span></span>

<span data-ttu-id="3eab5-136">PLAYSOUND("chord.wav", 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="3eab5-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="3eab5-137">Reproduz o arquivo de áudio wave chord.wav de forma assíncrona sem aviso sonoro.</span><span class="sxs-lookup"><span data-stu-id="3eab5-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3eab5-138">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3eab5-138">Example 2</span></span>

<span data-ttu-id="3eab5-139">PLAYSOUND("ExclamaçãodeSistema", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="3eab5-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="3eab5-140">Reproduz o som de exclamação de sistema de forma assíncrona sem aviso sonoro.</span><span class="sxs-lookup"><span data-stu-id="3eab5-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

