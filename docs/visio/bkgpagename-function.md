---
title: Função BKGPAGENAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Retorna um nome de página de plano de fundo como uma cadeia de caracteres.
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410312"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="8c76b-103">Função BKGPAGENAME</span><span class="sxs-lookup"><span data-stu-id="8c76b-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="8c76b-104">Retorna um nome de página de plano de fundo como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8c76b-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8c76b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c76b-105">Syntax</span></span>

<span data-ttu-id="8c76b-106">BKGPAGENAME (\*\* *langID_opt* \*\* )</span><span class="sxs-lookup"><span data-stu-id="8c76b-106">BKGPAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8c76b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c76b-107">Parameters</span></span>

|<span data-ttu-id="8c76b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8c76b-108">**Name**</span></span>|<span data-ttu-id="8c76b-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="8c76b-109">**Required/Optional**</span></span>|<span data-ttu-id="8c76b-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="8c76b-110">**Data Type**</span></span>|<span data-ttu-id="8c76b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8c76b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8c76b-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="8c76b-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="8c76b-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="8c76b-113">Optional</span></span>  <br/> |<span data-ttu-id="8c76b-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="8c76b-114">**Numeric**</span></span> <br/> |<span data-ttu-id="8c76b-p101">Use para especificar uma linguagem para a cadeia de caracteres retornada pela função. Use 0 (valor padrão) para especificar a linguagem local. Use 750 para especificar a linguagem universal.</span><span class="sxs-lookup"><span data-stu-id="8c76b-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8c76b-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8c76b-118">Return value</span></span>

<span data-ttu-id="8c76b-119">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="8c76b-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8c76b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c76b-120">Remarks</span></span>

<span data-ttu-id="8c76b-121">Se a página para a qual você está usando a função não tiver uma página de plano de fundo, a cadeia de caracteres "\<sem plano de fundo\>" é retornada.</span><span class="sxs-lookup"><span data-stu-id="8c76b-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="8c76b-122">Se você passar um código de linguagem inválido, a linguagem local será utilizada.</span><span class="sxs-lookup"><span data-stu-id="8c76b-122">If you pass an illegal language code, the local language is used.</span></span> 
  

