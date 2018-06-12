---
title: Função TRIM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Remove todo o espaço do texto, com exceção de espaços simples entre palavras.
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773188"
---
# <a name="trim-function"></a><span data-ttu-id="938ed-103">Função TRIM</span><span class="sxs-lookup"><span data-stu-id="938ed-103">TRIM Function</span></span>

<span data-ttu-id="938ed-104">Remove todo o espaço do texto, com exceção de espaços simples entre palavras.</span><span class="sxs-lookup"><span data-stu-id="938ed-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="938ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="938ed-105">Syntax</span></span>

<span data-ttu-id="938ed-106">TRIM (* * *texto* * *)</span><span class="sxs-lookup"><span data-stu-id="938ed-106">TRIM (** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="938ed-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="938ed-107">Parameters</span></span>

|<span data-ttu-id="938ed-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="938ed-108">**Name**</span></span>|<span data-ttu-id="938ed-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="938ed-109">**Required/Optional**</span></span>|<span data-ttu-id="938ed-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="938ed-110">**Data Type**</span></span>|<span data-ttu-id="938ed-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="938ed-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="938ed-112">_text_</span><span class="sxs-lookup"><span data-stu-id="938ed-112">_text_</span></span> <br/> |<span data-ttu-id="938ed-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="938ed-113">Required</span></span>  <br/> |<span data-ttu-id="938ed-114">**String**</span><span class="sxs-lookup"><span data-stu-id="938ed-114">**String**</span></span> <br/> |<span data-ttu-id="938ed-115">O texto em que os espaços devem ser removidos.</span><span class="sxs-lookup"><span data-stu-id="938ed-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="938ed-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="938ed-116">Return value</span></span>

<span data-ttu-id="938ed-117">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="938ed-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="938ed-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="938ed-118">Remarks</span></span>

<span data-ttu-id="938ed-119">Você pode usar a função TRIM no texto recebido de outro aplicativo que tenha espaçamento irregular.</span><span class="sxs-lookup"><span data-stu-id="938ed-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="938ed-120">Example</span><span class="sxs-lookup"><span data-stu-id="938ed-120">Example</span></span>

<span data-ttu-id="938ed-121">TRIM ("1 de janeiro de 2003")</span><span class="sxs-lookup"><span data-stu-id="938ed-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="938ed-122">Retornará "January 1, 2003".</span><span class="sxs-lookup"><span data-stu-id="938ed-122">Returns "January 1, 2003".</span></span> 
  

