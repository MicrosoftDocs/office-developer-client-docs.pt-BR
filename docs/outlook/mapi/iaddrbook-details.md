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
ms.openlocfilehash: fbe7f02555f76532896c951f50648c528c250a58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766882"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="42c3e-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="42c3e-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="42c3e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42c3e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42c3e-105">Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada de catálogo de endereço específica.</span><span class="sxs-lookup"><span data-stu-id="42c3e-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="42c3e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42c3e-106">Parameters</span></span>

 <span data-ttu-id="42c3e-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="42c3e-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="42c3e-108">[in] Um ponteiro para um identificador da janela pai para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="42c3e-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="42c3e-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="42c3e-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="42c3e-110">[in] Um ponteiro para uma função com base no [DISMISSMODELESS](dismissmodeless.md) protótipo ou nulo.</span><span class="sxs-lookup"><span data-stu-id="42c3e-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="42c3e-111">Este membro só se aplica a versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI sendo definido.</span><span class="sxs-lookup"><span data-stu-id="42c3e-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="42c3e-112">MAPI chama a função **DISMISSMODELESS** quando o usuário descarte a caixa de diálogo sem janela restrita endereço informando um cliente que está chamando **detalhes** que a caixa de diálogo não está mais ativa.</span><span class="sxs-lookup"><span data-stu-id="42c3e-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="42c3e-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="42c3e-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="42c3e-114">[in] Um ponteiro para informações de contexto para passar para a função **DISMISSMODELESS** apontado pelo parâmetro _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="42c3e-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="42c3e-115">Esse parâmetro se aplica somente à versão da caixa de diálogo sem janela restrita, incluindo o sinalizador DIALOG_SDI no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="42c3e-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="42c3e-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="42c3e-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="42c3e-117">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="42c3e-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="42c3e-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="42c3e-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="42c3e-119">[in] Um ponteiro para o identificador de entrada para a entrada para o qual os detalhes são exibidos.</span><span class="sxs-lookup"><span data-stu-id="42c3e-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="42c3e-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="42c3e-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="42c3e-121">[in] Um ponteiro para uma função com base no protótipo de função [LPFNBUTTON](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="42c3e-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="42c3e-122">Uma função **LPFNBUTTON** adiciona um botão para a caixa de diálogo detalhes.</span><span class="sxs-lookup"><span data-stu-id="42c3e-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="42c3e-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="42c3e-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="42c3e-124">[in] Um ponteiro para os dados que foi usados como um parâmetro para a função especificada pelo parâmetro _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="42c3e-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="42c3e-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="42c3e-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="42c3e-126">[in] Um ponteiro para uma cadeia de caracteres que contém o texto a ser aplicado ao botão adicionado, se esse botão é extensível.</span><span class="sxs-lookup"><span data-stu-id="42c3e-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="42c3e-127">O parâmetro _lpszButtonText_ deve ser NULL se não é necessário um botão extensível.</span><span class="sxs-lookup"><span data-stu-id="42c3e-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="42c3e-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="42c3e-128">_ulFlags_</span></span>
  
> <span data-ttu-id="42c3e-129">[in] Uma bitmask dos sinalizadores que controla o tipo do texto para o parâmetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="42c3e-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="42c3e-130">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="42c3e-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="42c3e-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="42c3e-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="42c3e-132">Indica que os **detalhes** Retorna S_OK se alterações forem feitas realmente o endereço; Caso contrário, **detalhes** retorna S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="42c3e-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="42c3e-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="42c3e-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="42c3e-134">Exiba a versão modal da caixa de diálogo endereço comuns, que sempre é mostrada nos clientes não do Outlook.</span><span class="sxs-lookup"><span data-stu-id="42c3e-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="42c3e-135">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="42c3e-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="42c3e-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="42c3e-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="42c3e-137">Exiba a versão sem janela restrita da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="42c3e-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="42c3e-138">Esse sinalizador é ignorada para clientes não do Outlook.</span><span class="sxs-lookup"><span data-stu-id="42c3e-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="42c3e-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="42c3e-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="42c3e-140">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="42c3e-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="42c3e-141">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="42c3e-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="42c3e-142">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="42c3e-142">Return value</span></span>

<span data-ttu-id="42c3e-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="42c3e-143">S_OK</span></span> 
  
> <span data-ttu-id="42c3e-144">A caixa de diálogo detalhes foi exibida com êxito para a entrada do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="42c3e-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42c3e-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="42c3e-145">Remarks</span></span>

<span data-ttu-id="42c3e-146">Aplicativos cliente chamam o método de **detalhes** para exibir uma caixa de diálogo que fornece detalhes sobre uma determinada entrada no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="42c3e-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="42c3e-147">Você pode usar os parâmetros _lpfButtonCallback_, _lpvButtonContext_e _lpszButtonText_ para adicionar um botão de cliente definido para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="42c3e-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="42c3e-148">Quando o botão é clicado, o MAPI chama a função de retorno de chamada apontada pela _lpfButtonCallback_, passando o identificador de entrada do botão e os dados em _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="42c3e-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="42c3e-149">Se você não é necessário um botão extensível, _lpszButtonText_ deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="42c3e-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="42c3e-150">**Detalhes** oferece suporte a cadeias de caracteres Unicode; Cadeias de caracteres Unicode são convertidas para o formato de cadeia de caracteres (MBCS) caracteres multibyte antes que eles sejam exibidos na caixa de diálogo detalhes.</span><span class="sxs-lookup"><span data-stu-id="42c3e-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="42c3e-151">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="42c3e-151">MFCMAPI reference</span></span>

<span data-ttu-id="42c3e-152">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="42c3e-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="42c3e-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="42c3e-153">**File**</span></span>|<span data-ttu-id="42c3e-154">**Function**</span><span class="sxs-lookup"><span data-stu-id="42c3e-154">**Function**</span></span>|<span data-ttu-id="42c3e-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="42c3e-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="42c3e-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="42c3e-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="42c3e-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="42c3e-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="42c3e-158">MFCMAPI usa o método **Details** para exibir uma caixa de diálogo que mostra os detalhes de uma entrada do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="42c3e-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42c3e-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="42c3e-159">See also</span></span>



[<span data-ttu-id="42c3e-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="42c3e-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="42c3e-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="42c3e-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="42c3e-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="42c3e-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="42c3e-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="42c3e-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="42c3e-164">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="42c3e-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

