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
description: Retorna o nome de uma página de plano de fundo como uma cadeia de caracteres.
ms.openlocfilehash: 290fa62242298b3c513bf2870df37204fab31bf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771397"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="98b09-103">Função BKGPAGENAME</span><span class="sxs-lookup"><span data-stu-id="98b09-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="98b09-104">Retorna o nome de uma página de plano de fundo como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="98b09-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="98b09-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98b09-105">Syntax</span></span>

<span data-ttu-id="98b09-106">BKGPAGENAME (* * *langID_opt* * *)</span><span class="sxs-lookup"><span data-stu-id="98b09-106">BKGPAGENAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="98b09-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98b09-107">Parameters</span></span>

|<span data-ttu-id="98b09-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="98b09-108">**Name**</span></span>|<span data-ttu-id="98b09-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="98b09-109">**Required/Optional**</span></span>|<span data-ttu-id="98b09-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="98b09-110">**Data Type**</span></span>|<span data-ttu-id="98b09-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="98b09-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="98b09-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="98b09-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="98b09-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="98b09-113">Optional</span></span>  <br/> |<span data-ttu-id="98b09-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="98b09-114">**Numeric**</span></span> <br/> |<span data-ttu-id="98b09-p101">Use para especificar uma linguagem para a cadeia de caracteres retornada pela função. Use 0 (valor padrão) para especificar a linguagem local. Use 750 para especificar a linguagem universal.</span><span class="sxs-lookup"><span data-stu-id="98b09-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="98b09-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="98b09-118">Return value</span></span>

<span data-ttu-id="98b09-119">String</span><span class="sxs-lookup"><span data-stu-id="98b09-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98b09-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="98b09-120">Remarks</span></span>

<span data-ttu-id="98b09-121">Se a página para o qual você estiver usando a função não tiver uma página de plano de fundo, a cadeia de caracteres "\<nenhum plano de fundo\>" é retornado.</span><span class="sxs-lookup"><span data-stu-id="98b09-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="98b09-122">Se você passar um código de linguagem inválido, a linguagem local será utilizada.</span><span class="sxs-lookup"><span data-stu-id="98b09-122">If you pass an illegal language code, the local language is used.</span></span> 
  

