---
title: Usando macros para tratamento de erros
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435562"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="46169-103">Usando macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="46169-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="46169-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46169-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46169-105">Há várias macros para facilitar o trabalho com valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="46169-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="46169-106">Há dois conjuntos de macros que testam a falha ou o êxito: HR_SUCCEEDED e HR_FAILED e com êxito e falha.</span><span class="sxs-lookup"><span data-stu-id="46169-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="46169-107">SUCCEEDed é o mesmo que HR_SUCCEEDED e FAILED é o mesmo que HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="46169-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="46169-108">Nesse caso, use a macro **ResultFromScode** para definir a variável HRESULT para o valor HRESULT correspondente de S_OK.</span><span class="sxs-lookup"><span data-stu-id="46169-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="46169-109">As macros comumente usadas são descritas brevemente na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="46169-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="46169-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="46169-110">**Macro**</span></span>|<span data-ttu-id="46169-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="46169-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="46169-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="46169-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="46169-113">Constrói um HRESULT a partir de seus componentes.</span><span class="sxs-lookup"><span data-stu-id="46169-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="46169-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="46169-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="46169-115">Testa um HRESULT para uma condição de êxito ou de aviso.</span><span class="sxs-lookup"><span data-stu-id="46169-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="46169-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="46169-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="46169-117">Testa um HRESULT para uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="46169-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="46169-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="46169-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="46169-119">Extrai a parte do código de erro do HRESULT.</span><span class="sxs-lookup"><span data-stu-id="46169-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="46169-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="46169-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="46169-121">Extrai o recurso do HRESULT.</span><span class="sxs-lookup"><span data-stu-id="46169-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="46169-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="46169-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="46169-123">Extrai o bit de severidade da severidade.</span><span class="sxs-lookup"><span data-stu-id="46169-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="46169-124">**ADICIONADA**</span><span class="sxs-lookup"><span data-stu-id="46169-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="46169-125">Testa um HRESULT para uma condição de êxito ou de aviso.</span><span class="sxs-lookup"><span data-stu-id="46169-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="46169-126">**FALHOU**</span><span class="sxs-lookup"><span data-stu-id="46169-126">**FAILED**</span></span> <br/> |<span data-ttu-id="46169-127">Testa um HRESULT para uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="46169-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

