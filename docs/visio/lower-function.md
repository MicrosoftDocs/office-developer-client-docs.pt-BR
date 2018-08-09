---
title: Função LOWER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
localization_priority: Normal
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: Retorna uma cadeia de caracteres convertida em minúsculas.
ms.openlocfilehash: da626ee0bb0474fceafcf93ed5c835aacd0034fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772300"
---
# <a name="lower-function"></a><span data-ttu-id="2235b-103">Função LOWER</span><span class="sxs-lookup"><span data-stu-id="2235b-103">LOWER Function</span></span>

<span data-ttu-id="2235b-104">Retorna uma cadeia de caracteres convertida em minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2235b-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2235b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2235b-105">Syntax</span></span>

<span data-ttu-id="2235b-106">INFERIOR (* * *expressão* * *)</span><span class="sxs-lookup"><span data-stu-id="2235b-106">LOWER(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2235b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2235b-107">Parameters</span></span>

|<span data-ttu-id="2235b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2235b-108">**Name**</span></span>|<span data-ttu-id="2235b-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="2235b-109">**Required/Optional**</span></span>|<span data-ttu-id="2235b-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="2235b-110">**Data Type**</span></span>|<span data-ttu-id="2235b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2235b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2235b-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="2235b-112">_expression_</span></span> <br/> |<span data-ttu-id="2235b-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2235b-113">Required</span></span>  <br/> |<span data-ttu-id="2235b-114">**Varia**</span><span class="sxs-lookup"><span data-stu-id="2235b-114">**Varies**</span></span> <br/> | <span data-ttu-id="2235b-115">Uma cadeia de caracteres, uma referência de célula ou uma expressão: o resultado é convertido em uma cadeia, que é depois convertida em minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2235b-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2235b-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2235b-116">Return value</span></span>

<span data-ttu-id="2235b-117">String</span><span class="sxs-lookup"><span data-stu-id="2235b-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2235b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2235b-118">Remarks</span></span>

<span data-ttu-id="2235b-119">A conversão de maiúsculas e minúsculas é específica a cada local, tendo por base as configurações de usuário atuais.</span><span class="sxs-lookup"><span data-stu-id="2235b-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2235b-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2235b-120">Example</span></span>

<span data-ttu-id="2235b-121">LOWER("MAiúsculas/minÚsculas")</span><span class="sxs-lookup"><span data-stu-id="2235b-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="2235b-122">Retornará "maiúsculas/minúsculas".</span><span class="sxs-lookup"><span data-stu-id="2235b-122">Returns "mixed case".</span></span> 
  

