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
ms.openlocfilehash: 47cf87fce0af3b866018bf03a34a05ea42cef82c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426678"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="57c8b-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="57c8b-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="57c8b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57c8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57c8b-105">Garante que o método **OpenEntry** seja aberto pelo provedor de agenda do Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="57c8b-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="57c8b-106">Esta função funciona de forma semelhante a [IAddrBook::D etails,](iaddrbook-details.md) mas abre **entryID** usando o livro de endereços do Exchange identificado por  _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="57c8b-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="57c8b-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="57c8b-107">Header file:</span></span>  <br/> |<span data-ttu-id="57c8b-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="57c8b-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="57c8b-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="57c8b-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="57c8b-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="57c8b-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="57c8b-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="57c8b-111">Called by:</span></span>  <br/> |<span data-ttu-id="57c8b-112">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="57c8b-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="57c8b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57c8b-113">Parameters</span></span>

 <span data-ttu-id="57c8b-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="57c8b-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="57c8b-115">[in] Um ponteiro para um  _emsabpUID_ que identifica o provedor de agendamento de endereços do Exchange que essa função deve usar para exibir detalhes sobre o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="57c8b-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="57c8b-116">Se o identificador de entrada de entrada não for um identificador de entrada do provedor de endereços do Exchange, esse parâmetro será ignorado e a chamada de função agirá exatamente como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="57c8b-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="57c8b-117">Se esse parâmetro for NULL ou zero MAPIUID, essa função também atuará exatamente como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="57c8b-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="57c8b-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="57c8b-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="57c8b-119">[in] O livro de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="57c8b-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="57c8b-120">Não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="57c8b-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="57c8b-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="57c8b-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="57c8b-122">[out] Um alça para a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="57c8b-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="57c8b-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="57c8b-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="57c8b-124">[in] Um ponteiro para uma função baseada no protótipo **DISMISSMODELESS** ou NULL.</span><span class="sxs-lookup"><span data-stu-id="57c8b-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="57c8b-125">Este membro aplica-se somente à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="57c8b-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="57c8b-126">MAPI calls the **DISMISSMODELESS function** when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span><span class="sxs-lookup"><span data-stu-id="57c8b-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="57c8b-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="57c8b-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="57c8b-128">[in] Um ponteiro para informações de contexto a ser passado para a **função DISMISSMODELESS** apontado pelo _parâmetro lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="57c8b-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="57c8b-129">Esse parâmetro só se aplica à versão sem modo da caixa de diálogo incluindo o sinalizador **DIALOG_SDI** no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="57c8b-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="57c8b-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="57c8b-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="57c8b-131">[in] A contagem de byte do identificador de entrada especificado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="57c8b-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="57c8b-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="57c8b-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="57c8b-133">[in] Um ponteiro para o identificador de entrada que representa a entrada do livro de endereços a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="57c8b-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="57c8b-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="57c8b-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="57c8b-135">[in] Um ponteiro para uma função baseada no protótipo da função **LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="57c8b-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="57c8b-136">Uma **função LPFNBUTTON** adiciona um botão à caixa de diálogo de detalhes.</span><span class="sxs-lookup"><span data-stu-id="57c8b-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="57c8b-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="57c8b-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="57c8b-138">[in] Um ponteiro para dados que foi usado como um parâmetro para a função especificada pelo _parâmetro lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="57c8b-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="57c8b-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="57c8b-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="57c8b-140">[in] Um ponteiro para uma cadeia de caracteres que contém texto a ser aplicado ao botão adicionado, se esse botão for extensível.</span><span class="sxs-lookup"><span data-stu-id="57c8b-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="57c8b-141">O  _parâmetro lpszButtonText_ deve ser NULL quando não for necessário um botão extensível.</span><span class="sxs-lookup"><span data-stu-id="57c8b-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="57c8b-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57c8b-142">_ulFlags_</span></span>
  
> <span data-ttu-id="57c8b-143">[in] Uma bitmask de sinalizadores que controla o tipo de texto para o _parâmetro lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="57c8b-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="57c8b-144">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="57c8b-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="57c8b-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="57c8b-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="57c8b-146">Indica que Details retornará TRUE se as alterações realmente foram feitas no endereço; Caso contrário, Details retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="57c8b-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="57c8b-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="57c8b-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="57c8b-148">Exibe a versão modal da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="57c8b-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="57c8b-149">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="57c8b-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="57c8b-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="57c8b-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="57c8b-151">Exibe a versão sem modo da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="57c8b-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="57c8b-152">Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="57c8b-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="57c8b-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="57c8b-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="57c8b-154">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="57c8b-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="57c8b-155">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="57c8b-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

