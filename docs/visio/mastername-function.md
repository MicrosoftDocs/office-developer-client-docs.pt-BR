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
description: Retorna o nome mestre de uma planilha como uma cadeia de caracteres ou retorna a cadeia de caracteres ' sem mestre ' se a planilha não tiver um mestre.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414750"
---
# <a name="mastername-function"></a><span data-ttu-id="b16ee-103">Função MASTERNAME</span><span class="sxs-lookup"><span data-stu-id="b16ee-103">MASTERNAME Function</span></span>

<span data-ttu-id="b16ee-104">Retorna o nome mestre de uma planilha como uma cadeia de caracteres ou retorna a\<cadeia de\>caracteres "sem mestre" se a planilha não tiver um mestre.</span><span class="sxs-lookup"><span data-stu-id="b16ee-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b16ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b16ee-105">Syntax</span></span>

<span data-ttu-id="b16ee-106">MASTERname ([\* \* *langID_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="b16ee-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b16ee-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b16ee-107">Parameters</span></span>

|<span data-ttu-id="b16ee-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b16ee-108">**Name**</span></span>|<span data-ttu-id="b16ee-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="b16ee-109">**Required/Optional**</span></span>|<span data-ttu-id="b16ee-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="b16ee-110">**Data Type**</span></span>|<span data-ttu-id="b16ee-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b16ee-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b16ee-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="b16ee-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="b16ee-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="b16ee-113">Optional</span></span>  <br/> |<span data-ttu-id="b16ee-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="b16ee-114">**Number**</span></span> <br/> |<span data-ttu-id="b16ee-p101">Use para especificar uma linguagem para a cadeia de caracteres retornada pela função. Use 0 (valor padrão) para especificar a linguagem local. Use 750 para especificar a linguagem universal.</span><span class="sxs-lookup"><span data-stu-id="b16ee-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b16ee-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b16ee-118">Return value</span></span>

<span data-ttu-id="b16ee-119">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="b16ee-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b16ee-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b16ee-120">Remarks</span></span>

<span data-ttu-id="b16ee-121">Se você passar um código de linguagem inválido, a linguagem local será utilizada.</span><span class="sxs-lookup"><span data-stu-id="b16ee-121">If you pass an illegal language code, the local language is used.</span></span> 
  

