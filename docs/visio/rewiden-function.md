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
description: Converte uma fórmula que produz códigos de caracteres de 16 bits que são códigos de conjunto de caracteres de um ou vários byte ampliados em uma cadeia de caracteres Unicode de 16 bits, usando os conjuntos de caracteres especificados.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405209"
---
# <a name="rewiden-function"></a><span data-ttu-id="ab2ab-103">Função REWIDEN</span><span class="sxs-lookup"><span data-stu-id="ab2ab-103">REWIDEN Function</span></span>

<span data-ttu-id="ab2ab-104">Converte uma fórmula que produz códigos de caracteres de 16 bits que são códigos de conjunto de caracteres de um ou vários byte ampliados em uma cadeia de caracteres Unicode de 16 bits, usando os conjuntos de caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="ab2ab-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ab2ab-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab2ab-105">Syntax</span></span>

<span data-ttu-id="ab2ab-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ab2ab-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ab2ab-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab2ab-107">Parameters</span></span>

|<span data-ttu-id="ab2ab-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ab2ab-108">**Name**</span></span>|<span data-ttu-id="ab2ab-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="ab2ab-109">**Required/Optional**</span></span>|<span data-ttu-id="ab2ab-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="ab2ab-110">**Data Type**</span></span>|<span data-ttu-id="ab2ab-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ab2ab-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ab2ab-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="ab2ab-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="ab2ab-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ab2ab-113">Required</span></span>  <br/> |<span data-ttu-id="ab2ab-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ab2ab-114">**String**</span></span> <br/> |<span data-ttu-id="ab2ab-115">O conjunto de caracteres no documento de origem.</span><span class="sxs-lookup"><span data-stu-id="ab2ab-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="ab2ab-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="ab2ab-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="ab2ab-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ab2ab-117">Required</span></span>  <br/> |<span data-ttu-id="ab2ab-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ab2ab-118">**String**</span></span> <br/> | <span data-ttu-id="ab2ab-119">O conjunto de caracteres no documento de destino.</span><span class="sxs-lookup"><span data-stu-id="ab2ab-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="ab2ab-120">_text_</span><span class="sxs-lookup"><span data-stu-id="ab2ab-120">_text_</span></span> <br/> |<span data-ttu-id="ab2ab-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ab2ab-121">Required</span></span>  <br/> |<span data-ttu-id="ab2ab-122">**String**</span><span class="sxs-lookup"><span data-stu-id="ab2ab-122">**String**</span></span> <br/> |<span data-ttu-id="ab2ab-123">O texto a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="ab2ab-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab2ab-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab2ab-124">Remarks</span></span>

<span data-ttu-id="ab2ab-p101">A função REWIDEN é usada na conversão automática de documentos do Visio 2002 em documentos do Visio 2003. A utilização para outros fins não é recomendada.</span><span class="sxs-lookup"><span data-stu-id="ab2ab-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

