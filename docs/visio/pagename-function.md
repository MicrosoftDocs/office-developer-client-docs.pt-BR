---
title: Função PAGENAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
localization_priority: Normal
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: Retorna o nome da página como uma cadeia de caracteres.
ms.openlocfilehash: d5527bde58a68c96bd75773f3a0a8c30f64fa20d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438649"
---
# <a name="pagename-function"></a><span data-ttu-id="a5717-103">Função PAGENAME</span><span class="sxs-lookup"><span data-stu-id="a5717-103">PAGENAME Function</span></span>

<span data-ttu-id="a5717-104">Retorna o nome da página como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a5717-104">Returns the page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a5717-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5717-105">Syntax</span></span>

<span data-ttu-id="a5717-106">PAGEname (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a5717-106">PAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a5717-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5717-107">Parameters</span></span>

|<span data-ttu-id="a5717-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a5717-108">**Name**</span></span>|<span data-ttu-id="a5717-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="a5717-109">**Required/Optional**</span></span>|<span data-ttu-id="a5717-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a5717-110">**Data Type**</span></span>|<span data-ttu-id="a5717-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a5717-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a5717-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="a5717-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="a5717-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="a5717-113">Optional</span></span>  <br/> |<span data-ttu-id="a5717-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="a5717-114">**Number**</span></span> <br/> |<span data-ttu-id="a5717-p101">Use para especificar uma linguagem para a cadeia de caracteres retornada pela função. Use 0 (valor padrão) para especificar a linguagem local. Use 750 para especificar a linguagem universal.</span><span class="sxs-lookup"><span data-stu-id="a5717-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a5717-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a5717-118">Return value</span></span>

<span data-ttu-id="a5717-119">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a5717-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5717-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5717-120">Remarks</span></span>

<span data-ttu-id="a5717-121">Se você passar um código de linguagem inválido, a linguagem local será utilizada.</span><span class="sxs-lookup"><span data-stu-id="a5717-121">If you pass an illegal language code, the local language is used.</span></span>
  

