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
description: Remove todo o espaço do texto, exceto espaços individuais entre palavras.
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435716"
---
# <a name="trim-function"></a><span data-ttu-id="741a1-103">Função TRIM</span><span class="sxs-lookup"><span data-stu-id="741a1-103">TRIM Function</span></span>

<span data-ttu-id="741a1-104">Remove todo o espaço do texto, exceto espaços individuais entre palavras.</span><span class="sxs-lookup"><span data-stu-id="741a1-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="741a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="741a1-105">Syntax</span></span>

<span data-ttu-id="741a1-106">TRIM (\*\* *texto* \*\* )</span><span class="sxs-lookup"><span data-stu-id="741a1-106">TRIM (\*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="741a1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="741a1-107">Parameters</span></span>

|<span data-ttu-id="741a1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="741a1-108">**Name**</span></span>|<span data-ttu-id="741a1-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="741a1-109">**Required/Optional**</span></span>|<span data-ttu-id="741a1-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="741a1-110">**Data Type**</span></span>|<span data-ttu-id="741a1-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="741a1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="741a1-112">_text_</span><span class="sxs-lookup"><span data-stu-id="741a1-112">_text_</span></span> <br/> |<span data-ttu-id="741a1-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="741a1-113">Required</span></span>  <br/> |<span data-ttu-id="741a1-114">**String**</span><span class="sxs-lookup"><span data-stu-id="741a1-114">**String**</span></span> <br/> |<span data-ttu-id="741a1-115">O texto em que os espaços devem ser removidos.</span><span class="sxs-lookup"><span data-stu-id="741a1-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="741a1-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="741a1-116">Return value</span></span>

<span data-ttu-id="741a1-117">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="741a1-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="741a1-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="741a1-118">Remarks</span></span>

<span data-ttu-id="741a1-119">Você pode usar a função TRIM no texto recebido de outro aplicativo que tenha espaçamento irregular.</span><span class="sxs-lookup"><span data-stu-id="741a1-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="741a1-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="741a1-120">Example</span></span>

<span data-ttu-id="741a1-121">TRIM ("1º de janeiro de 2003 ")</span><span class="sxs-lookup"><span data-stu-id="741a1-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="741a1-122">Retornará "January 1, 2003".</span><span class="sxs-lookup"><span data-stu-id="741a1-122">Returns "January 1, 2003".</span></span> 
  

