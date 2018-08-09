---
title: Função NAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
localization_priority: Normal
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: Retorna o nome de uma folha como uma cadeia de caracteres.
ms.openlocfilehash: 0d3a70573177d8e16a16972d0a08245381b209dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772406"
---
# <a name="name-function"></a><span data-ttu-id="f4589-103">Função NAME</span><span class="sxs-lookup"><span data-stu-id="f4589-103">NAME Function</span></span>

<span data-ttu-id="f4589-104">Retorna o nome de uma folha como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4589-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f4589-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4589-105">Syntax</span></span>

<span data-ttu-id="f4589-106">NOME (* * *langID_opt* * *)</span><span class="sxs-lookup"><span data-stu-id="f4589-106">NAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f4589-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4589-107">Parameters</span></span>

|<span data-ttu-id="f4589-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f4589-108">**Name**</span></span>|<span data-ttu-id="f4589-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f4589-109">**Required/Optional**</span></span>|<span data-ttu-id="f4589-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="f4589-110">**Data Type**</span></span>|<span data-ttu-id="f4589-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f4589-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f4589-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="f4589-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="f4589-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="f4589-113">Optional</span></span>  <br/> |<span data-ttu-id="f4589-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="f4589-114">**Number**</span></span> <br/> |<span data-ttu-id="f4589-p101">Use para especificar uma linguagem para a cadeia de caracteres retornada pela função. Use 0 (valor padrão) para especificar a linguagem local. Use 750 para especificar a linguagem universal.</span><span class="sxs-lookup"><span data-stu-id="f4589-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f4589-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f4589-118">Return value</span></span>

<span data-ttu-id="f4589-119">String</span><span class="sxs-lookup"><span data-stu-id="f4589-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f4589-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4589-120">Remarks</span></span>

<span data-ttu-id="f4589-121">Se você passar um código de linguagem inválido, a linguagem local será utilizada.</span><span class="sxs-lookup"><span data-stu-id="f4589-121">If you pass an illegal language code, the local language is used.</span></span> 
  

