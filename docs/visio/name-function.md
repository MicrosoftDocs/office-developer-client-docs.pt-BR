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
description: Retorna o nome de uma planilha como uma cadeia de caracteres.
ms.openlocfilehash: 7d0a4e9f3c5f70be07e9cc5691f52afcbc7bea68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416794"
---
# <a name="name-function"></a><span data-ttu-id="759bf-103">Função NAME</span><span class="sxs-lookup"><span data-stu-id="759bf-103">NAME Function</span></span>

<span data-ttu-id="759bf-104">Retorna o nome de uma planilha como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="759bf-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="759bf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="759bf-105">Syntax</span></span>

<span data-ttu-id="759bf-106">NAME (\*\* *langID_opt* \*\* )</span><span class="sxs-lookup"><span data-stu-id="759bf-106">NAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="759bf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="759bf-107">Parameters</span></span>

|<span data-ttu-id="759bf-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="759bf-108">**Name**</span></span>|<span data-ttu-id="759bf-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="759bf-109">**Required/Optional**</span></span>|<span data-ttu-id="759bf-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="759bf-110">**Data Type**</span></span>|<span data-ttu-id="759bf-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="759bf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="759bf-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="759bf-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="759bf-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="759bf-113">Optional</span></span>  <br/> |<span data-ttu-id="759bf-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="759bf-114">**Number**</span></span> <br/> |<span data-ttu-id="759bf-p101">Use para especificar uma linguagem para a cadeia de caracteres retornada pela função. Use 0 (valor padrão) para especificar a linguagem local. Use 750 para especificar a linguagem universal.</span><span class="sxs-lookup"><span data-stu-id="759bf-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="759bf-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="759bf-118">Return value</span></span>

<span data-ttu-id="759bf-119">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="759bf-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="759bf-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="759bf-120">Remarks</span></span>

<span data-ttu-id="759bf-121">Se você passar um código de linguagem inválido, a linguagem local será utilizada.</span><span class="sxs-lookup"><span data-stu-id="759bf-121">If you pass an illegal language code, the local language is used.</span></span> 
  

