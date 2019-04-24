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
description: Converte uma fórmula que produz códigos de caracteres de 16 bits que são códigos de conjunto de caracteres de byte único ou multibyte ampliados em uma cadeia de caracteres de códigos Unicode de 16 bits, usando os conjuntos de caracteres especificados.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326765"
---
# <a name="rewiden-function"></a><span data-ttu-id="7526a-103">Função REWIDEN</span><span class="sxs-lookup"><span data-stu-id="7526a-103">REWIDEN Function</span></span>

<span data-ttu-id="7526a-104">Converte uma fórmula que produz códigos de caracteres de 16 bits que são códigos de conjunto de caracteres de byte único ou multibyte ampliados em uma cadeia de caracteres de códigos Unicode de 16 bits, usando os conjuntos de caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="7526a-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7526a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7526a-105">Syntax</span></span>

<span data-ttu-id="7526a-106">ReWIDEn (\* \* *srcCharSet* \* \*, \* \* *dstCharSet* \* \*, \* \* *Text* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7526a-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7526a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7526a-107">Parameters</span></span>

|<span data-ttu-id="7526a-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7526a-108">**Name**</span></span>|<span data-ttu-id="7526a-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="7526a-109">**Required/Optional**</span></span>|<span data-ttu-id="7526a-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="7526a-110">**Data Type**</span></span>|<span data-ttu-id="7526a-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7526a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7526a-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="7526a-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="7526a-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7526a-113">Required</span></span>  <br/> |<span data-ttu-id="7526a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="7526a-114">**String**</span></span> <br/> |<span data-ttu-id="7526a-115">O conjunto de caracteres no documento de origem.</span><span class="sxs-lookup"><span data-stu-id="7526a-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="7526a-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="7526a-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="7526a-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7526a-117">Required</span></span>  <br/> |<span data-ttu-id="7526a-118">**String**</span><span class="sxs-lookup"><span data-stu-id="7526a-118">**String**</span></span> <br/> | <span data-ttu-id="7526a-119">O conjunto de caracteres no documento de destino.</span><span class="sxs-lookup"><span data-stu-id="7526a-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="7526a-120">_text_</span><span class="sxs-lookup"><span data-stu-id="7526a-120">_text_</span></span> <br/> |<span data-ttu-id="7526a-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7526a-121">Required</span></span>  <br/> |<span data-ttu-id="7526a-122">**String**</span><span class="sxs-lookup"><span data-stu-id="7526a-122">**String**</span></span> <br/> |<span data-ttu-id="7526a-123">O texto a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="7526a-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7526a-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7526a-124">Remarks</span></span>

<span data-ttu-id="7526a-p101">A função REWIDEN é usada na conversão automática de documentos do Visio 2002 em documentos do Visio 2003. A utilização para outros fins não é recomendada.</span><span class="sxs-lookup"><span data-stu-id="7526a-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

