---
title: Função de idioma
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permite que operações de comparação entre as representações de idioma diferente. Melhor, ele é usado para conversão de valores de marcas (47 BCP) de idiomas do Internet Engineering Task Force para valores de id (LCID) da localidade.
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772167"
---
# <a name="language-function"></a><span data-ttu-id="28044-104">Função de idioma</span><span class="sxs-lookup"><span data-stu-id="28044-104">LANGUAGE Function</span></span>

<span data-ttu-id="28044-105">Permite que operações de comparação entre as representações de idioma diferente.</span><span class="sxs-lookup"><span data-stu-id="28044-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="28044-106">Melhor, ele é usado para conversão de valores de marcas (47 BCP) de idiomas do Internet Engineering Task Force para valores de id (LCID) da localidade.</span><span class="sxs-lookup"><span data-stu-id="28044-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="28044-107">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="28044-107">Version Information</span></span>

<span data-ttu-id="28044-108">Version Added: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="28044-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="28044-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28044-109">Syntax</span></span>

 <span data-ttu-id="28044-110">**Idioma** ( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="28044-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="28044-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28044-111">Parameters</span></span>

|<span data-ttu-id="28044-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="28044-112">**Name**</span></span>|<span data-ttu-id="28044-113">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="28044-113">**Required/Optional**</span></span>|<span data-ttu-id="28044-114">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="28044-114">**Data Type**</span></span>|<span data-ttu-id="28044-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="28044-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="28044-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="28044-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="28044-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="28044-117">Required</span></span>  <br/> |<span data-ttu-id="28044-118">**String**</span><span class="sxs-lookup"><span data-stu-id="28044-118">**String**</span></span> <br/> |<span data-ttu-id="28044-119">O valor para o idioma LCID ou 47 BCP.</span><span class="sxs-lookup"><span data-stu-id="28044-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="28044-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="28044-120">Return value</span></span>

<span data-ttu-id="28044-121">Inteiro</span><span class="sxs-lookup"><span data-stu-id="28044-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="28044-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="28044-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="28044-123">Retorna um valor de '1033'.</span><span class="sxs-lookup"><span data-stu-id="28044-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="28044-124">Retorna um valor de '3082'.</span><span class="sxs-lookup"><span data-stu-id="28044-124">Returns a value of '3082'.</span></span>
  

