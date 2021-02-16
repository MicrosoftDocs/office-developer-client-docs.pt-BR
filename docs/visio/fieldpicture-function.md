---
title: Função FIELDPICTURE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Retorna uma cadeia de caracteres de formatação que corresponde ao código de formato de campo de texto interno do Microsoft Visio.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431453"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="fb27f-103">Função FIELDPICTURE</span><span class="sxs-lookup"><span data-stu-id="fb27f-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="fb27f-104">Retorna uma cadeia de caracteres de formatação que corresponde ao código de formato de campo de texto interno do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="fb27f-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fb27f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb27f-105">Syntax</span></span>

<span data-ttu-id="fb27f-106">FIELDPICTURE(\*\* *code* \*\* )</span><span class="sxs-lookup"><span data-stu-id="fb27f-106">FIELDPICTURE(\*\* *code* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fb27f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb27f-107">Parameters</span></span>

|<span data-ttu-id="fb27f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fb27f-108">**Name**</span></span>|<span data-ttu-id="fb27f-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="fb27f-109">**Required/Optional**</span></span>|<span data-ttu-id="fb27f-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="fb27f-110">**Data Type**</span></span>|<span data-ttu-id="fb27f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fb27f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fb27f-112">_code_</span><span class="sxs-lookup"><span data-stu-id="fb27f-112">_code_</span></span> <br/> |<span data-ttu-id="fb27f-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fb27f-113">Required</span></span>  <br/> |<span data-ttu-id="fb27f-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="fb27f-114">**Number**</span></span> <br/> | <span data-ttu-id="fb27f-115">Um código de formato de campo de texto.</span><span class="sxs-lookup"><span data-stu-id="fb27f-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fb27f-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fb27f-116">Return value</span></span>

<span data-ttu-id="fb27f-117">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="fb27f-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb27f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb27f-118">Remarks</span></span>

<span data-ttu-id="fb27f-119">As sequências de caracteres de figura de formatação são utilizadas na função FORMAT para definir a expansão de valores para datas, horas, números e rótulos de unidade.</span><span class="sxs-lookup"><span data-stu-id="fb27f-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="fb27f-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fb27f-120">Example</span></span>

<span data-ttu-id="fb27f-121">FIELDPICTURE(0)</span><span class="sxs-lookup"><span data-stu-id="fb27f-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="fb27f-122">Retorna a cadeia de caracteres de figura de formatação "esc(0)", a qual especifica um número com uma posição decimal e uma descrição de unidade em minúsculas quando utilizada na função FORMAT.</span><span class="sxs-lookup"><span data-stu-id="fb27f-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

