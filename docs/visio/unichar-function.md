---
title: Função UNICHAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Retorna o caractere Unicode de um número.
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773219"
---
# <a name="unichar-function"></a><span data-ttu-id="e1087-103">Função UNICHAR</span><span class="sxs-lookup"><span data-stu-id="e1087-103">UNICHAR Function</span></span>

<span data-ttu-id="e1087-104">Retorna o caractere Unicode de um número.</span><span class="sxs-lookup"><span data-stu-id="e1087-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e1087-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1087-105">Syntax</span></span>

<span data-ttu-id="e1087-106">UNICHAR (* * *número* * *)</span><span class="sxs-lookup"><span data-stu-id="e1087-106">UNICHAR (** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e1087-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1087-107">Parameters</span></span>

|<span data-ttu-id="e1087-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e1087-108">**Name**</span></span>|<span data-ttu-id="e1087-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e1087-109">**Required/Optional**</span></span>|<span data-ttu-id="e1087-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e1087-110">**Data Type**</span></span>|<span data-ttu-id="e1087-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e1087-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e1087-112">_number_</span><span class="sxs-lookup"><span data-stu-id="e1087-112">_number_</span></span> <br/> |<span data-ttu-id="e1087-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e1087-113">Required</span></span>  <br/> |<span data-ttu-id="e1087-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="e1087-114">**Integer**</span></span> <br/> |<span data-ttu-id="e1087-115">Um número inteiro entre 1 e 65.535 (inclusive) ou a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="e1087-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1087-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1087-116">Remarks</span></span>

<span data-ttu-id="e1087-117">A cadeia de caracteres resultante é um caractere Unicode (dois caracteres).</span><span class="sxs-lookup"><span data-stu-id="e1087-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e1087-118">Example</span><span class="sxs-lookup"><span data-stu-id="e1087-118">Example</span></span>

<span data-ttu-id="e1087-119">UNICHAR(65)</span><span class="sxs-lookup"><span data-stu-id="e1087-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="e1087-120">Retorna um (letra latina A maiuscula)</span><span class="sxs-lookup"><span data-stu-id="e1087-120">Returns A (Latin Capital Letter A)</span></span> 
  

