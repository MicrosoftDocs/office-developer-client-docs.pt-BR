---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cb4f38615ac6cacb3acbaa456f0992bf55c3653d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568620"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="10719-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="10719-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="10719-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10719-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10719-105">Garante que o método **OpenEntry** for aberto, o provedor de catálogo de endereços do Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="10719-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="10719-106">Essa função funciona da mesma forma para [IAddrBook::Details](iaddrbook-details.md) , mas abre **entryID** usando o catálogo de endereços do Exchange identificado pela _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="10719-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10719-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="10719-107">Header file:</span></span>  <br/> |<span data-ttu-id="10719-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="10719-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="10719-109">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="10719-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="10719-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="10719-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="10719-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="10719-111">Called by:</span></span>  <br/> |<span data-ttu-id="10719-112">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="10719-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="10719-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10719-113">Parameters</span></span>

 <span data-ttu-id="10719-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="10719-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="10719-115">[in] Um ponteiro para uma _emsabpUID_ que identifica o provedor de catálogo de endereços do Exchange essa função deve usar para exibir detalhes sobre o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="10719-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="10719-116">Se o identificador de entrada de entrada não é um identificador de entrada do Exchange endereço livro provedor, esse parâmetro será ignorado e a age de chamada de função exatamente como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="10719-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="10719-117">Se esse parâmetro for NULL ou um zero MAPIUID, essa função também funciona exatamente como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="10719-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="10719-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="10719-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="10719-119">[in] O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="10719-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="10719-120">Ele não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="10719-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="10719-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="10719-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="10719-122">[out] Uma alça para a janela pai para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="10719-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="10719-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="10719-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="10719-124">[in] Um ponteiro para uma função com base no **DISMISSMODELESS** protótipo ou nulo.</span><span class="sxs-lookup"><span data-stu-id="10719-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="10719-125">Este membro só se aplica a versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI sendo definido.</span><span class="sxs-lookup"><span data-stu-id="10719-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="10719-126">MAPI chama a função **DISMISSMODELESS** quando o usuário descarte a caixa de diálogo sem janela restrita endereço informando um cliente que está chamando que a caixa de diálogo não está mais ativa de detalhes.</span><span class="sxs-lookup"><span data-stu-id="10719-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="10719-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="10719-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="10719-128">[in] Um ponteiro para informações de contexto para passar para a função **DISMISSMODELESS** apontado pelo parâmetro _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="10719-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="10719-129">Esse parâmetro se aplica somente à versão da caixa de diálogo sem janela restrita, incluindo o sinalizador **DIALOG_SDI** no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="10719-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="10719-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="10719-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="10719-131">[in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="10719-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="10719-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="10719-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="10719-133">[in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir.</span><span class="sxs-lookup"><span data-stu-id="10719-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="10719-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="10719-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="10719-135">[in] Um ponteiro para uma função com base no protótipo de função **LPFNBUTTON** .</span><span class="sxs-lookup"><span data-stu-id="10719-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="10719-136">Uma função **LPFNBUTTON** adiciona um botão para a caixa de diálogo detalhes.</span><span class="sxs-lookup"><span data-stu-id="10719-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="10719-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="10719-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="10719-138">[in] Um ponteiro para os dados que foi usados como um parâmetro para a função especificada pelo parâmetro _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="10719-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="10719-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="10719-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="10719-140">[in] Um ponteiro para uma cadeia de caracteres que contém o texto a ser aplicado ao botão adicionado, se esse botão é extensível.</span><span class="sxs-lookup"><span data-stu-id="10719-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="10719-141">O parâmetro _lpszButtonText_ deve ser NULL quando um botão extensível não é necessário.</span><span class="sxs-lookup"><span data-stu-id="10719-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="10719-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="10719-142">_ulFlags_</span></span>
  
> <span data-ttu-id="10719-143">[in] Uma bitmask dos sinalizadores que controla o tipo do texto para o parâmetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="10719-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="10719-144">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="10719-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="10719-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="10719-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="10719-146">Indica que detalhes retorna TRUE se as alterações são feitas na verdade, o endereço; Caso contrário, detalhes retorna FALSE.</span><span class="sxs-lookup"><span data-stu-id="10719-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="10719-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="10719-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="10719-148">Exibe a versão modal da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="10719-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="10719-149">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="10719-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="10719-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="10719-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="10719-151">Exibe a versão sem janela restrita da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="10719-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="10719-152">Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="10719-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="10719-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="10719-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="10719-154">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="10719-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="10719-155">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="10719-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

