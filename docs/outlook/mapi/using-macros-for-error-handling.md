---
title: Usar macros para lidar com erros
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 715cd001c5eab89f40c31200a12deaf6981b9a61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567122"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="06d51-103">Usar macros para lidar com erros</span><span class="sxs-lookup"><span data-stu-id="06d51-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="06d51-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06d51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06d51-105">Há várias macros para tornando mais fácil trabalhar com valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="06d51-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="06d51-106">Há dois conjuntos de macros que testam a falha ou sucesso: HR_SUCCEEDED e HR_FAILED e SUCCEEDED e FAILED.</span><span class="sxs-lookup"><span data-stu-id="06d51-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="06d51-107">SUCESSO é que o mesmo que HR_SUCCEEDED e FAILED é o mesmo HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="06d51-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="06d51-108">Nesse caso, use a macro **ResultFromScode** para definir a variável HRESULT com o valor HRESULT correspondente para S_OK.</span><span class="sxs-lookup"><span data-stu-id="06d51-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="06d51-109">Macros comumente usadas são descritas resumidamente na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="06d51-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="06d51-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="06d51-110">**Macro**</span></span>|<span data-ttu-id="06d51-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="06d51-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06d51-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="06d51-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="06d51-113">Constrói um HRESULT de seus componentes.</span><span class="sxs-lookup"><span data-stu-id="06d51-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="06d51-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="06d51-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="06d51-115">Testa um HRESULT para um sucesso ou condição de aviso.</span><span class="sxs-lookup"><span data-stu-id="06d51-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="06d51-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="06d51-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="06d51-117">Testa um HRESULT para uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="06d51-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="06d51-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="06d51-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="06d51-119">Extrai a parte do código de erro do HRESULT.</span><span class="sxs-lookup"><span data-stu-id="06d51-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="06d51-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="06d51-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="06d51-121">Extrai a facilidade do HRESULT.</span><span class="sxs-lookup"><span data-stu-id="06d51-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="06d51-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="06d51-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="06d51-123">Extrai estará definido o bit gravidade da GRAVIDADE.</span><span class="sxs-lookup"><span data-stu-id="06d51-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="06d51-124">**FOI BEM-SUCEDIDA**</span><span class="sxs-lookup"><span data-stu-id="06d51-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="06d51-125">Testa um HRESULT para um sucesso ou condição de aviso.</span><span class="sxs-lookup"><span data-stu-id="06d51-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="06d51-126">**FALHA**</span><span class="sxs-lookup"><span data-stu-id="06d51-126">**FAILED**</span></span> <br/> |<span data-ttu-id="06d51-127">Testa um HRESULT para uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="06d51-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

