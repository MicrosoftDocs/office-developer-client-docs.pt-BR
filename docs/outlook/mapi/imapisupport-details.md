---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322355"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="63b39-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="63b39-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="63b39-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63b39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63b39-105">Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada de catálogo de endereços específica.</span><span class="sxs-lookup"><span data-stu-id="63b39-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="63b39-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63b39-106">Parameters</span></span>

 <span data-ttu-id="63b39-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="63b39-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="63b39-108">bota Um ponteiro para a alça da janela pai da caixa de diálogo retornada.</span><span class="sxs-lookup"><span data-stu-id="63b39-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="63b39-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="63b39-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="63b39-110">no Um ponteiro para uma função com base no protótipo [DISMISSMODELESS](dismissmodeless.md) ou nulo.</span><span class="sxs-lookup"><span data-stu-id="63b39-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="63b39-111">Este membro se aplica apenas à versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="63b39-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="63b39-112">MAPI chama a função **DISMISSMODELESS** quando o usuário ignora a caixa de diálogo de endereço sem restrições, informando um cliente que está chamando **IMAPISupport::D etails** que a caixa de diálogo não está mais ativa.</span><span class="sxs-lookup"><span data-stu-id="63b39-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="63b39-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="63b39-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="63b39-114">no Um ponteiro para informações de contexto a serem passadas para a função **DISMISSMODELESS** apontada pelo parâmetro _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="63b39-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="63b39-115">Esse parâmetro se aplica apenas à versão sem janela restrita da caixa de diálogo, incluindo o sinalizador DIALOG_SDI no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="63b39-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="63b39-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="63b39-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="63b39-117">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="63b39-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="63b39-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="63b39-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="63b39-119">no Um ponteiro para o identificador de entrada para o qual os detalhes são exibidos.</span><span class="sxs-lookup"><span data-stu-id="63b39-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="63b39-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="63b39-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="63b39-121">no Um ponteiro para uma função com base no protótipo de função [LPFNBUTTON](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="63b39-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="63b39-122">Uma função **LPFNBUTTON** adiciona um botão à caixa de diálogo detalhes.</span><span class="sxs-lookup"><span data-stu-id="63b39-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="63b39-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="63b39-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="63b39-124">no Um ponteiro para dados usados como um parâmetro para a função especificada pelo parâmetro _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="63b39-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="63b39-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="63b39-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="63b39-126">no Um ponteiro para uma cadeia de caracteres que contém o texto a ser aplicado ao botão adicionado se esse botão é extensível.</span><span class="sxs-lookup"><span data-stu-id="63b39-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="63b39-127">O parâmetro _lpszButtonText_ deve ser NULL se um botão extensível não for necessário.</span><span class="sxs-lookup"><span data-stu-id="63b39-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="63b39-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63b39-128">_ulFlags_</span></span>
  
> <span data-ttu-id="63b39-129">no Uma bitmask de sinalizadores que controla o tipo de texto para o parâmetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="63b39-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="63b39-130">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="63b39-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="63b39-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="63b39-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="63b39-132">Exibe a versão modal da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="63b39-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="63b39-133">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="63b39-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="63b39-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="63b39-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="63b39-135">Exibe a versão sem janela restrita da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="63b39-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="63b39-136">Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="63b39-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="63b39-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="63b39-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="63b39-138">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="63b39-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="63b39-139">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="63b39-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63b39-140">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="63b39-140">Return value</span></span>

<span data-ttu-id="63b39-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="63b39-141">S_OK</span></span> 
  
> <span data-ttu-id="63b39-142">A caixa de diálogo detalhes foi exibida com êxito para a entrada do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="63b39-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63b39-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="63b39-143">Remarks</span></span>

<span data-ttu-id="63b39-144">O método **IMAPISupport::D etails** é implementado para objetos de suporte do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="63b39-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="63b39-145">Os provedores de catálogo de endereços chamam **detalhes** para exibir uma caixa de diálogo que fornece detalhes sobre uma entrada específica no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="63b39-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="63b39-146">Os parâmetros _lpfButtonCallback_, _lpvButtonContext_e _lpszButtonText_ podem ser usados para adicionar um botão definido pelo cliente à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="63b39-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="63b39-147">Quando o botão é clicado, MAPI chama a função de retorno de chamada indicada por _lpfButtonCallback_, passando o identificador de entrada do botão e os dados no _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="63b39-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="63b39-148">Se um botão extensível não for necessário, _lpszButtonText_ deverá ser nulo.</span><span class="sxs-lookup"><span data-stu-id="63b39-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63b39-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="63b39-149">See also</span></span>



[<span data-ttu-id="63b39-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="63b39-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="63b39-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="63b39-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="63b39-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="63b39-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="63b39-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="63b39-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

