---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424676"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="061c4-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="061c4-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="061c4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="061c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="061c4-105">Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada de catálogo de endereços específica.</span><span class="sxs-lookup"><span data-stu-id="061c4-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="061c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="061c4-106">Parameters</span></span>

 <span data-ttu-id="061c4-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="061c4-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="061c4-108">no Um ponteiro para um identificador da janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="061c4-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="061c4-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="061c4-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="061c4-110">no Um ponteiro para uma função com base no protótipo [DISMISSMODELESS](dismissmodeless.md) ou nulo.</span><span class="sxs-lookup"><span data-stu-id="061c4-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="061c4-111">Este membro se aplica apenas à versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="061c4-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="061c4-112">MAPI chama a função **DISMISSMODELESS** quando o usuário ignora a caixa de diálogo de endereço sem restrições, informando um cliente que está chamando os **detalhes** de que a caixa de diálogo não está mais ativa.</span><span class="sxs-lookup"><span data-stu-id="061c4-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="061c4-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="061c4-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="061c4-114">no Um ponteiro para informações de contexto a serem passadas para a função **DISMISSMODELESS** apontada pelo parâmetro _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="061c4-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="061c4-115">Esse parâmetro se aplica apenas à versão sem janela restrita da caixa de diálogo, incluindo o sinalizador DIALOG_SDI no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="061c4-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="061c4-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="061c4-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="061c4-117">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="061c4-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="061c4-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="061c4-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="061c4-119">no Um ponteiro para o identificador de entrada para a entrada para a qual os detalhes são exibidos.</span><span class="sxs-lookup"><span data-stu-id="061c4-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="061c4-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="061c4-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="061c4-121">no Um ponteiro para uma função com base no protótipo de função [LPFNBUTTON](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="061c4-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="061c4-122">Uma função **LPFNBUTTON** adiciona um botão à caixa de diálogo detalhes.</span><span class="sxs-lookup"><span data-stu-id="061c4-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="061c4-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="061c4-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="061c4-124">no Um ponteiro para dados que foram usados como um parâmetro para a função especificada pelo parâmetro _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="061c4-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="061c4-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="061c4-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="061c4-126">no Um ponteiro para uma cadeia de caracteres que contém o texto a ser aplicado ao botão adicionado, se esse botão é extensível.</span><span class="sxs-lookup"><span data-stu-id="061c4-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="061c4-127">O parâmetro _lpszButtonText_ deve ser NULL se você não precisar de um botão extensível.</span><span class="sxs-lookup"><span data-stu-id="061c4-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="061c4-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="061c4-128">_ulFlags_</span></span>
  
> <span data-ttu-id="061c4-129">no Uma bitmask de sinalizadores que controla o tipo de texto para o parâmetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="061c4-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="061c4-130">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="061c4-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="061c4-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="061c4-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="061c4-132">Indica que os **detalhes** retornam S_OK se as alterações forem realmente feitas no endereço; caso contrário, os **detalhes** retornarão S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="061c4-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="061c4-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="061c4-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="061c4-134">Exibe a versão modal da caixa de diálogo endereço comum, que sempre é mostrada em clientes não-Outlook.</span><span class="sxs-lookup"><span data-stu-id="061c4-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="061c4-135">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="061c4-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="061c4-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="061c4-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="061c4-137">Exibe a versão sem janela restrita da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="061c4-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="061c4-138">Este sinalizador é ignorado para clientes que não são do Outlook.</span><span class="sxs-lookup"><span data-stu-id="061c4-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="061c4-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="061c4-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="061c4-140">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="061c4-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="061c4-141">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="061c4-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="061c4-142">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="061c4-142">Return value</span></span>

<span data-ttu-id="061c4-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="061c4-143">S_OK</span></span> 
  
> <span data-ttu-id="061c4-144">A caixa de diálogo detalhes foi exibida com êxito para a entrada do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="061c4-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="061c4-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="061c4-145">Remarks</span></span>

<span data-ttu-id="061c4-146">Os aplicativos cliente chamam o método **Details** para exibir uma caixa de diálogo que fornece detalhes sobre uma entrada específica no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="061c4-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="061c4-147">Você pode usar os parâmetros _lpfButtonCallback_, _lpvButtonContext_e _lpszButtonText_ para adicionar um botão definido pelo cliente à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="061c4-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="061c4-148">Quando o botão é clicado, MAPI chama a função de retorno de chamada indicada por _lpfButtonCallback_, passando o identificador de entrada do botão e os dados no _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="061c4-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="061c4-149">Se você não precisar de um botão extensível, _lpszButtonText_ deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="061c4-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="061c4-150">Os **detalhes** dão suporte a cadeias de caracteres Unicode; As cadeias de caracteres Unicode são convertidas no formato MBCS (cadeia de caracteres multibyte) antes de serem exibidas na caixa de diálogo detalhes.</span><span class="sxs-lookup"><span data-stu-id="061c4-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="061c4-151">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="061c4-151">MFCMAPI reference</span></span>

<span data-ttu-id="061c4-152">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="061c4-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="061c4-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="061c4-153">**File**</span></span>|<span data-ttu-id="061c4-154">**Função**</span><span class="sxs-lookup"><span data-stu-id="061c4-154">**Function**</span></span>|<span data-ttu-id="061c4-155">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="061c4-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="061c4-156">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="061c4-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="061c4-157">CBaseDialog:: OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="061c4-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="061c4-158">MFCMAPI usa o método **Details** para exibir uma caixa de diálogo que mostra os detalhes de uma entrada do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="061c4-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="061c4-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="061c4-159">See also</span></span>



[<span data-ttu-id="061c4-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="061c4-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="061c4-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="061c4-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="061c4-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="061c4-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="061c4-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="061c4-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="061c4-164">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="061c4-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

