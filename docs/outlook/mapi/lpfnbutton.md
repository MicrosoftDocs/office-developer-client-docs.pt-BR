---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3b302de68f27e85c67430f82bd3e2c33009600e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591349"
---
# <a name="lpfnbutton"></a><span data-ttu-id="75372-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="75372-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="75372-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75372-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75372-105">Define uma função de retorno de chamada que chamadas MAPI para ativar um controle de botão opcional em uma caixa de diálogo Catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="75372-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="75372-106">Normalmente, esse botão é um botão de **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="75372-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75372-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="75372-107">Header file:</span></span>  <br/> |<span data-ttu-id="75372-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75372-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="75372-109">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="75372-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="75372-110">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="75372-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="75372-111">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="75372-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="75372-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="75372-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="75372-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75372-113">Parameters</span></span>

 <span data-ttu-id="75372-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="75372-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="75372-115">[in] Alça das janelas de pai para todas as caixas de diálogo ou windows que exibe essa função.</span><span class="sxs-lookup"><span data-stu-id="75372-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="75372-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="75372-116">_lpvContext_</span></span>
  
> <span data-ttu-id="75372-117">[in] Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando chamadas de MAPI-lo.</span><span class="sxs-lookup"><span data-stu-id="75372-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="75372-118">Esse valor pode representar um endereço de significância ao aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="75372-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="75372-119">Geralmente, para código C++, _lpvContext_ representa um ponteiro para um objeto C++.</span><span class="sxs-lookup"><span data-stu-id="75372-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="75372-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="75372-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="75372-121">[in] Tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpSelection_ .</span><span class="sxs-lookup"><span data-stu-id="75372-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="75372-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="75372-122">_lpSelection_</span></span>
  
> <span data-ttu-id="75372-123">[in] Ponteiro para o identificador de entrada definindo a seleção na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="75372-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="75372-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="75372-124">_ulFlags_</span></span>
  
> <span data-ttu-id="75372-125">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="75372-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="75372-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="75372-126">Return value</span></span>

<span data-ttu-id="75372-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="75372-127">S_OK</span></span> 
  
> <span data-ttu-id="75372-128">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="75372-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="75372-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="75372-129">Remarks</span></span>

<span data-ttu-id="75372-130">Aplicativos cliente chamam uma função de retorno de chamada com base em protótipo **LPFNBUTTON** para definir um botão em uma caixa de diálogo detalhes.</span><span class="sxs-lookup"><span data-stu-id="75372-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="75372-131">O cliente passa um ponteiro para a função de retorno de chamada em chamadas para o método [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="75372-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="75372-132">Provedores de serviços de chamarem uma função de fora do gancho, com base em protótipo **LPFNBUTTON** para definir um botão em uma caixa de diálogo detalhes.</span><span class="sxs-lookup"><span data-stu-id="75372-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="75372-133">O provedor passa um ponteiro para essa função gancho em chamadas para o método [IMAPISupport::Details](imapisupport-details.md) .</span><span class="sxs-lookup"><span data-stu-id="75372-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="75372-134">Em ambos os casos, quando a caixa de diálogo é exibida e o usuário escolhe o botão definido, MAPI chama **LPFNBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="75372-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="75372-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="75372-135">See also</span></span>



[<span data-ttu-id="75372-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="75372-136">BuildDisplayTable</span></span>](builddisplaytable.md)

