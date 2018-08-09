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
ms.openlocfilehash: c4e216f2204f4ee97d9eeac81f77ce6a82fff3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770691"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="4f20c-103">Usar macros para lidar com erros</span><span class="sxs-lookup"><span data-stu-id="4f20c-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="4f20c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f20c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f20c-105">Há várias macros para tornando mais fácil trabalhar com valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="4f20c-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="4f20c-106">Há dois conjuntos de macros que testam a falha ou sucesso: HR_SUCCEEDED e HR_FAILED e SUCCEEDED e FAILED.</span><span class="sxs-lookup"><span data-stu-id="4f20c-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="4f20c-107">SUCESSO é que o mesmo que HR_SUCCEEDED e FAILED é o mesmo HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="4f20c-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="4f20c-108">Nesse caso, use a macro **ResultFromScode** para definir a variável HRESULT com o valor HRESULT correspondente para S_OK.</span><span class="sxs-lookup"><span data-stu-id="4f20c-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="4f20c-109">Macros comumente usadas são descritas resumidamente na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4f20c-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="4f20c-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="4f20c-110">**Macro**</span></span>|<span data-ttu-id="4f20c-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4f20c-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f20c-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4f20c-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="4f20c-113">Constrói um HRESULT de seus componentes.</span><span class="sxs-lookup"><span data-stu-id="4f20c-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="4f20c-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="4f20c-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="4f20c-115">Testa um HRESULT para um sucesso ou condição de aviso.</span><span class="sxs-lookup"><span data-stu-id="4f20c-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="4f20c-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="4f20c-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="4f20c-117">Testa um HRESULT para uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="4f20c-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="4f20c-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="4f20c-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="4f20c-119">Extrai a parte do código de erro do HRESULT.</span><span class="sxs-lookup"><span data-stu-id="4f20c-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="4f20c-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="4f20c-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="4f20c-121">Extrai a facilidade do HRESULT.</span><span class="sxs-lookup"><span data-stu-id="4f20c-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="4f20c-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="4f20c-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="4f20c-123">Extrai estará definido o bit gravidade da GRAVIDADE.</span><span class="sxs-lookup"><span data-stu-id="4f20c-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="4f20c-124">**FOI BEM-SUCEDIDA**</span><span class="sxs-lookup"><span data-stu-id="4f20c-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="4f20c-125">Testa um HRESULT para um sucesso ou condição de aviso.</span><span class="sxs-lookup"><span data-stu-id="4f20c-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="4f20c-126">**FALHA**</span><span class="sxs-lookup"><span data-stu-id="4f20c-126">**FAILED**</span></span> <br/> |<span data-ttu-id="4f20c-127">Testa um HRESULT para uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="4f20c-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

