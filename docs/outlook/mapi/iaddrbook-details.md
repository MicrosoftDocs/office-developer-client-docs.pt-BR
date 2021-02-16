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
# <a name="iaddrbookdetails"></a><span data-ttu-id="0af11-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="0af11-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="0af11-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0af11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0af11-105">Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada específica do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="0af11-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0af11-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0af11-106">Parameters</span></span>

 <span data-ttu-id="0af11-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0af11-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="0af11-108">[in] Um ponteiro para uma alça da janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0af11-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="0af11-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="0af11-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="0af11-110">[in] Um ponteiro para uma função baseada no protótipo [DISMISSMODELESS](dismissmodeless.md) ou NULL.</span><span class="sxs-lookup"><span data-stu-id="0af11-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="0af11-111">Este membro aplica-se somente à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="0af11-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="0af11-112">MAPI calls the **DISMISSMODELESS function** when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span><span class="sxs-lookup"><span data-stu-id="0af11-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="0af11-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="0af11-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="0af11-114">[in] Um ponteiro para informações de contexto a ser passado para a **função DISMISSMODELESS** apontado pelo _parâmetro lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="0af11-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="0af11-115">Esse parâmetro se aplica somente à versão sem modo da caixa de diálogo, incluindo o sinalizador DIALOG_SDI no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="0af11-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="0af11-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0af11-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="0af11-117">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="0af11-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0af11-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0af11-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="0af11-119">[in] Um ponteiro para o identificador de entrada para a entrada para a qual os detalhes são exibidos.</span><span class="sxs-lookup"><span data-stu-id="0af11-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="0af11-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="0af11-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="0af11-121">[in] Um ponteiro para uma função baseada no protótipo da função [LPFNBUTTON.](lpfnbutton.md)</span><span class="sxs-lookup"><span data-stu-id="0af11-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="0af11-122">Uma **função LPFNBUTTON** adiciona um botão à caixa de diálogo de detalhes.</span><span class="sxs-lookup"><span data-stu-id="0af11-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="0af11-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="0af11-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="0af11-124">[in] Um ponteiro para dados que foi usado como um parâmetro para a função especificada pelo _parâmetro lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="0af11-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="0af11-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="0af11-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="0af11-126">[in] Um ponteiro para uma cadeia de caracteres que contém texto a ser aplicado ao botão adicionado, se esse botão for extensível.</span><span class="sxs-lookup"><span data-stu-id="0af11-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="0af11-127">O  _parâmetro lpszButtonText_ deve ser NULL se você não precisar de um botão extensível.</span><span class="sxs-lookup"><span data-stu-id="0af11-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="0af11-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0af11-128">_ulFlags_</span></span>
  
> <span data-ttu-id="0af11-129">[in] Uma bitmask de sinalizadores que controla o tipo de texto para o _parâmetro lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="0af11-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="0af11-130">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="0af11-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="0af11-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="0af11-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="0af11-132">Indica que **Details retornará** S_OK se realmente foram feitas alterações no endereço; caso contrário, **Details** retornará S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="0af11-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="0af11-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="0af11-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="0af11-134">Exibe a versão modal da caixa de diálogo de endereço comum, que é sempre mostrada em clientes que não são do Outlook.</span><span class="sxs-lookup"><span data-stu-id="0af11-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="0af11-135">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="0af11-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="0af11-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="0af11-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="0af11-137">Exibe a versão sem modo da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="0af11-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="0af11-138">Esse sinalizador é ignorado para clientes que não são do Outlook.</span><span class="sxs-lookup"><span data-stu-id="0af11-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="0af11-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0af11-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0af11-140">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0af11-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="0af11-141">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="0af11-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0af11-142">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0af11-142">Return value</span></span>

<span data-ttu-id="0af11-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="0af11-143">S_OK</span></span> 
  
> <span data-ttu-id="0af11-144">A caixa de diálogo de detalhes foi exibida com êxito para a entrada do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="0af11-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0af11-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="0af11-145">Remarks</span></span>

<span data-ttu-id="0af11-146">Os aplicativos cliente chamam **o método Details** para exibir uma caixa de diálogo que fornece detalhes sobre uma entrada específica no livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="0af11-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="0af11-147">Você pode usar os parâmetros  _lpfButtonCallback_,  _lpvButtonContext_ e  _lpszButtonText_ para adicionar um botão definido pelo cliente à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0af11-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="0af11-148">Quando o botão é clicado, MAPI chama a função de retorno de chamada apontada por  _lpfButtonCallback_, passando o identificador de entrada do botão e os dados em  _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="0af11-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="0af11-149">Se você não precisar de um botão extensível,  _lpszButtonText_ deverá ser NULL.</span><span class="sxs-lookup"><span data-stu-id="0af11-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="0af11-150">**Os detalhes** suportam cadeias de caracteres Unicode; As cadeias de caracteres Unicode são convertidas para o formato de cadeia de caracteres multibyte (MBCS) antes de serem exibidas na caixa de diálogo de detalhes.</span><span class="sxs-lookup"><span data-stu-id="0af11-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0af11-151">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0af11-151">MFCMAPI reference</span></span>

<span data-ttu-id="0af11-152">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0af11-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0af11-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="0af11-153">**File**</span></span>|<span data-ttu-id="0af11-154">**Função**</span><span class="sxs-lookup"><span data-stu-id="0af11-154">**Function**</span></span>|<span data-ttu-id="0af11-155">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="0af11-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0af11-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="0af11-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="0af11-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="0af11-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="0af11-158">MFCMAPI usa o **método Details** para exibir uma caixa de diálogo que mostra os detalhes de uma entrada do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="0af11-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0af11-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="0af11-159">See also</span></span>



[<span data-ttu-id="0af11-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="0af11-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="0af11-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="0af11-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="0af11-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="0af11-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="0af11-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0af11-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="0af11-164">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="0af11-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

