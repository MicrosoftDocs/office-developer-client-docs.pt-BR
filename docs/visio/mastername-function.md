---
title: Função MASTERNAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Retorna o nome do mestre de uma planilha como uma cadeia de caracteres ou não retorna a cadeia de caracteres 'nenhum mestre' se a folha não tiver um mestre.
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772325"
---
# <a name="mastername-function"></a><span data-ttu-id="e6742-103">Função MASTERNAME</span><span class="sxs-lookup"><span data-stu-id="e6742-103">MASTERNAME Function</span></span>

<span data-ttu-id="e6742-104">Retorna o nome do mestre de uma planilha como uma cadeia de caracteres ou retorna a cadeia de caracteres "\<nenhum mestre\>" se a folha não tiver um mestre.</span><span class="sxs-lookup"><span data-stu-id="e6742-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e6742-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6742-105">Syntax</span></span>

<span data-ttu-id="e6742-106">MASTERNAME ([* * *langID_opt* * *])</span><span class="sxs-lookup"><span data-stu-id="e6742-106">MASTERNAME ([ ** *langID_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e6742-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6742-107">Parameters</span></span>

|<span data-ttu-id="e6742-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e6742-108">**Name**</span></span>|<span data-ttu-id="e6742-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e6742-109">**Required/Optional**</span></span>|<span data-ttu-id="e6742-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e6742-110">**Data Type**</span></span>|<span data-ttu-id="e6742-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e6742-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e6742-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="e6742-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="e6742-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="e6742-113">Optional</span></span>  <br/> |<span data-ttu-id="e6742-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="e6742-114">**Number**</span></span> <br/> |<span data-ttu-id="e6742-p101">Use para especificar uma linguagem para a cadeia de caracteres retornada pela função. Use 0 (valor padrão) para especificar a linguagem local. Use 750 para especificar a linguagem universal.</span><span class="sxs-lookup"><span data-stu-id="e6742-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e6742-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e6742-118">Return value</span></span>

<span data-ttu-id="e6742-119">String</span><span class="sxs-lookup"><span data-stu-id="e6742-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6742-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6742-120">Remarks</span></span>

<span data-ttu-id="e6742-121">Se você passar um código de linguagem inválido, a linguagem local será utilizada.</span><span class="sxs-lookup"><span data-stu-id="e6742-121">If you pass an illegal language code, the local language is used.</span></span> 
  

