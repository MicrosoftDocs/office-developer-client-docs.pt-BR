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
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431509"
---
# <a name="lpfnbutton"></a><span data-ttu-id="a125f-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="a125f-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="a125f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a125f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a125f-105">Define uma função de retorno de chamada que MAPI chama para ativar um controle de botão opcional em uma caixa de diálogo do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="a125f-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="a125f-106">Normalmente, esse botão é um **botão** Detalhes.</span><span class="sxs-lookup"><span data-stu-id="a125f-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a125f-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a125f-107">Header file:</span></span>  <br/> |<span data-ttu-id="a125f-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a125f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a125f-109">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="a125f-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a125f-110">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="a125f-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="a125f-111">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="a125f-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a125f-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="a125f-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a125f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a125f-113">Parameters</span></span>

 <span data-ttu-id="a125f-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a125f-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="a125f-115">[in] Alça das janelas pai para quaisquer caixas de diálogo ou janelas que essa função exibe.</span><span class="sxs-lookup"><span data-stu-id="a125f-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="a125f-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="a125f-116">_lpvContext_</span></span>
  
> <span data-ttu-id="a125f-117">[in] Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando MAPI o chama.</span><span class="sxs-lookup"><span data-stu-id="a125f-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="a125f-118">Esse valor pode representar um endereço significativo para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="a125f-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="a125f-119">Normalmente, para código C++,  _lpvContext_ representa um ponteiro para um objeto C++.</span><span class="sxs-lookup"><span data-stu-id="a125f-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="a125f-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a125f-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="a125f-121">[in] Tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpSelection._</span><span class="sxs-lookup"><span data-stu-id="a125f-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="a125f-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="a125f-122">_lpSelection_</span></span>
  
> <span data-ttu-id="a125f-123">[in] Ponteiro para o identificador de entrada definindo a seleção na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a125f-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="a125f-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a125f-124">_ulFlags_</span></span>
  
> <span data-ttu-id="a125f-125">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a125f-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a125f-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a125f-126">Return value</span></span>

<span data-ttu-id="a125f-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="a125f-127">S_OK</span></span> 
  
> <span data-ttu-id="a125f-128">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="a125f-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a125f-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="a125f-129">Remarks</span></span>

<span data-ttu-id="a125f-130">Os aplicativos cliente chamam uma função de retorno de chamada com base no protótipo **LPFNBUTTON** para definir um botão em uma caixa de diálogo de detalhes.</span><span class="sxs-lookup"><span data-stu-id="a125f-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="a125f-131">O cliente passa um ponteiro para a função de retorno de chamada em chamadas para o [método IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="a125f-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="a125f-132">Os provedores de serviços chamam uma função de gancho com base no protótipo **LPFNBUTTON** para definir um botão em uma caixa de diálogo de detalhes.</span><span class="sxs-lookup"><span data-stu-id="a125f-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="a125f-133">O provedor passa um ponteiro para essa função de gancho em chamadas para o [método IMAPISupport::D etails.](imapisupport-details.md)</span><span class="sxs-lookup"><span data-stu-id="a125f-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="a125f-134">Em ambos os casos, quando a caixa de diálogo é exibida e o usuário escolhe o botão definido, MAPI chama **LPFNBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="a125f-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a125f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a125f-135">See also</span></span>



[<span data-ttu-id="a125f-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="a125f-136">BuildDisplayTable</span></span>](builddisplaytable.md)

