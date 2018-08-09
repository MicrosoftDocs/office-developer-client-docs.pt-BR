---
title: Função REWIDEN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Converte uma fórmula que produz códigos de caracteres de 16 bits que são largo códigos de conjunto de caracteres de byte único ou vários bytes em uma cadeia de códigos de caracteres Unicode 16 bits, usando os conjuntos de caracteres especificado.
ms.openlocfilehash: 66dc3e801585077a9521cd93f8ae78c47f8a746b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772731"
---
# <a name="rewiden-function"></a><span data-ttu-id="72f9f-103">Função REWIDEN</span><span class="sxs-lookup"><span data-stu-id="72f9f-103">REWIDEN Function</span></span>

<span data-ttu-id="72f9f-104">Converte uma fórmula que produz códigos de caracteres de 16 bits que são largo códigos de conjunto de caracteres de byte único ou vários bytes em uma cadeia de códigos de caracteres Unicode 16 bits, usando os conjuntos de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="72f9f-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="72f9f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72f9f-105">Syntax</span></span>

<span data-ttu-id="72f9f-106">REWIDEN (* * *srcCharSet* * *, * * *dstCharSet* * *, * * *texto* * *)</span><span class="sxs-lookup"><span data-stu-id="72f9f-106">REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="72f9f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72f9f-107">Parameters</span></span>

|<span data-ttu-id="72f9f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="72f9f-108">**Name**</span></span>|<span data-ttu-id="72f9f-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="72f9f-109">**Required/Optional**</span></span>|<span data-ttu-id="72f9f-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="72f9f-110">**Data Type**</span></span>|<span data-ttu-id="72f9f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="72f9f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="72f9f-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="72f9f-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="72f9f-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="72f9f-113">Required</span></span>  <br/> |<span data-ttu-id="72f9f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="72f9f-114">**String**</span></span> <br/> |<span data-ttu-id="72f9f-115">O conjunto de caracteres no documento de origem.</span><span class="sxs-lookup"><span data-stu-id="72f9f-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="72f9f-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="72f9f-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="72f9f-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="72f9f-117">Required</span></span>  <br/> |<span data-ttu-id="72f9f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="72f9f-118">**String**</span></span> <br/> | <span data-ttu-id="72f9f-119">O conjunto de caracteres no documento de destino.</span><span class="sxs-lookup"><span data-stu-id="72f9f-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="72f9f-120">_text_</span><span class="sxs-lookup"><span data-stu-id="72f9f-120">_text_</span></span> <br/> |<span data-ttu-id="72f9f-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="72f9f-121">Required</span></span>  <br/> |<span data-ttu-id="72f9f-122">**String**</span><span class="sxs-lookup"><span data-stu-id="72f9f-122">**String**</span></span> <br/> |<span data-ttu-id="72f9f-123">O texto a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="72f9f-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72f9f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="72f9f-124">Remarks</span></span>

<span data-ttu-id="72f9f-p101">A função REWIDEN é usada na conversão automática de documentos do Visio 2002 em documentos do Visio 2003. A utilização para outros fins não é recomendada.</span><span class="sxs-lookup"><span data-stu-id="72f9f-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

