---
title: Função LANGUAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permite operações de comparação entre diferentes representações de idioma. Ele é melhor usado para converter os valores de marcas de idioma (BCP 47) de engenharia da Internet para valores de ID de localidade (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424747"
---
# <a name="language-function"></a><span data-ttu-id="1080a-104">Função LANGUAGE</span><span class="sxs-lookup"><span data-stu-id="1080a-104">LANGUAGE Function</span></span>

<span data-ttu-id="1080a-105">Permite operações de comparação entre diferentes representações de idioma.</span><span class="sxs-lookup"><span data-stu-id="1080a-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="1080a-106">Ele é melhor usado para converter os valores de marcas de idioma (BCP 47) de engenharia da Internet para valores de ID de localidade (LCID).</span><span class="sxs-lookup"><span data-stu-id="1080a-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="1080a-107">Informações sobre a versão</span><span class="sxs-lookup"><span data-stu-id="1080a-107">Version Information</span></span>

<span data-ttu-id="1080a-108">Version Added: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="1080a-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1080a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1080a-109">Syntax</span></span>

 <span data-ttu-id="1080a-110">**Idioma** ( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="1080a-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="1080a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1080a-111">Parameters</span></span>

|<span data-ttu-id="1080a-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="1080a-112">**Name**</span></span>|<span data-ttu-id="1080a-113">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="1080a-113">**Required/Optional**</span></span>|<span data-ttu-id="1080a-114">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="1080a-114">**Data Type**</span></span>|<span data-ttu-id="1080a-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1080a-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1080a-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="1080a-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="1080a-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1080a-117">Required</span></span>  <br/> |<span data-ttu-id="1080a-118">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1080a-118">**String**</span></span> <br/> |<span data-ttu-id="1080a-119">O valor LCID ou BCP 47 para o idioma.</span><span class="sxs-lookup"><span data-stu-id="1080a-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="1080a-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1080a-120">Return value</span></span>

<span data-ttu-id="1080a-121">Inteiro</span><span class="sxs-lookup"><span data-stu-id="1080a-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="1080a-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1080a-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="1080a-123">Retorna um valor de ' 1033 '.</span><span class="sxs-lookup"><span data-stu-id="1080a-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="1080a-124">Retorna um valor de ' 3082 '.</span><span class="sxs-lookup"><span data-stu-id="1080a-124">Returns a value of '3082'.</span></span>
  

