---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421365"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="c844e-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="c844e-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="c844e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c844e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c844e-105">Garante que o método **OpenEntry** seja aberto pelo provedor de catálogo de endereços do Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="c844e-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="c844e-106">Essa função funciona de forma semelhante a [IAddrBook::D etails](iaddrbook-details.md), mas \*\*\*\* abre a EntryID usando o catálogo de endereços do Exchange identificado pelo parâmetro _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="c844e-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c844e-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c844e-107">Header file:</span></span>  <br/> |<span data-ttu-id="c844e-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="c844e-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="c844e-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c844e-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="c844e-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="c844e-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="c844e-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="c844e-111">Called by:</span></span>  <br/> |<span data-ttu-id="c844e-112">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="c844e-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a><span data-ttu-id="c844e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c844e-113">Parameters</span></span>

 <span data-ttu-id="c844e-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="c844e-114">_pmsess_</span></span>
  
> <span data-ttu-id="c844e-115">O **IMAPISession**conectado.</span><span class="sxs-lookup"><span data-stu-id="c844e-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="c844e-116">Ele não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="c844e-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c844e-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="c844e-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="c844e-118">Um ponteiro para um **emsmdbUID** que identifica o serviço do Exchange que contém o provedor de catálogo de endereços do Exchange usado pela função para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c844e-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="c844e-119">Se o identificador de entrada de entrada não for um identificador de entrada do provedor de catálogo de endereços do Exchange, esse parâmetro será ignorado e a função se comformará como [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="c844e-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="c844e-120">Se esse parâmetro for nulo ou um **MAPIUID**zero, essa função também funcionará exatamente como [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="c844e-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="c844e-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="c844e-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="c844e-122">no O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c844e-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="c844e-123">Ele não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="c844e-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c844e-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c844e-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="c844e-125">bota Uma alça para a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c844e-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="c844e-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="c844e-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="c844e-127">no Um ponteiro para uma função com base no protótipo **DISMISSMODELESS** ou nulo.</span><span class="sxs-lookup"><span data-stu-id="c844e-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="c844e-128">Este membro se aplica apenas à versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c844e-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="c844e-129">MAPI chama a função **DISMISSMODELESS** quando o usuário ignora a caixa de diálogo de endereço sem restrições, informando um cliente que está chamando os detalhes de que a caixa de diálogo não está mais ativa.</span><span class="sxs-lookup"><span data-stu-id="c844e-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="c844e-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="c844e-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="c844e-131">no Um ponteiro para informações de contexto a serem passadas para a função **DISMISSMODELESS** apontada pelo parâmetro _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="c844e-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="c844e-132">Esse parâmetro se aplica apenas à versão sem janela restrita da caixa de diálogo, incluindo o sinalizador **DIALOG_SDI** no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="c844e-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c844e-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c844e-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="c844e-134">no A contagem de bytes do identificador de entrada especificado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="c844e-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c844e-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c844e-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="c844e-136">no Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="c844e-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="c844e-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="c844e-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="c844e-138">no Um ponteiro para uma função com base no protótipo de função **LPFNBUTTON** .</span><span class="sxs-lookup"><span data-stu-id="c844e-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="c844e-139">Uma função **LPFNBUTTON** adiciona um botão à caixa de diálogo detalhes.</span><span class="sxs-lookup"><span data-stu-id="c844e-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="c844e-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="c844e-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="c844e-141">no Um ponteiro para dados que foram usados como um parâmetro para a função especificada pelo parâmetro _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="c844e-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="c844e-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="c844e-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="c844e-143">no Um ponteiro para uma cadeia de caracteres que contém o texto a ser aplicado ao botão adicionado, se esse botão é extensível.</span><span class="sxs-lookup"><span data-stu-id="c844e-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="c844e-144">O parâmetro _lpszButtonText_ deve ser NULL quando um botão extensível não é necessário.</span><span class="sxs-lookup"><span data-stu-id="c844e-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="c844e-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c844e-145">_ulFlags_</span></span>
  
> <span data-ttu-id="c844e-146">no Uma bitmask de sinalizadores que controla o tipo de texto para o parâmetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="c844e-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="c844e-147">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c844e-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="c844e-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="c844e-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="c844e-149">Indica que os detalhes retorna TRUE se as alterações forem realmente feitas no endereço; caso contrário, Details retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="c844e-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="c844e-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="c844e-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="c844e-151">Exibe a versão modal da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="c844e-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="c844e-152">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="c844e-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="c844e-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="c844e-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="c844e-154">Exibe a versão sem janela restrita da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="c844e-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="c844e-155">Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="c844e-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="c844e-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c844e-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="c844e-157">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="c844e-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c844e-158">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="c844e-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

