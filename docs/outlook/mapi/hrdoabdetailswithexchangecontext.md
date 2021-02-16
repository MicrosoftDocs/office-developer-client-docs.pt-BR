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
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="6c396-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="6c396-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="6c396-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c396-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c396-105">Garante que o método **OpenEntry** seja aberto pelo provedor de agenda do Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="6c396-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="6c396-106">Essa função funciona de forma semelhante a [IAddrBook::D etails](iaddrbook-details.md), mas abre a **entryID** usando o livro de endereços do Exchange identificado pelo parâmetro _pEmsmdbUID._</span><span class="sxs-lookup"><span data-stu-id="6c396-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c396-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6c396-107">Header file:</span></span>  <br/> |<span data-ttu-id="6c396-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="6c396-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="6c396-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6c396-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="6c396-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="6c396-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="6c396-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="6c396-111">Called by:</span></span>  <br/> |<span data-ttu-id="6c396-112">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="6c396-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="6c396-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c396-113">Parameters</span></span>

 <span data-ttu-id="6c396-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="6c396-114">_pmsess_</span></span>
  
> <span data-ttu-id="6c396-115">O **IMAPISession conectado.**</span><span class="sxs-lookup"><span data-stu-id="6c396-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="6c396-116">Não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="6c396-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="6c396-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="6c396-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="6c396-118">Um ponteiro para **um emsmdbUID** que identifica o Serviço do Exchange que contém o provedor de agenda do Exchange que é usado pela função para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="6c396-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="6c396-119">Se o identificador de entrada de entrada não for um identificador de entrada do provedor de endereços do Exchange, esse parâmetro será ignorado e a função se comportará como [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="6c396-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="6c396-120">Se esse parâmetro for NULL ou zero **MAPIUID,** essa função também atuará exatamente como [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="6c396-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="6c396-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="6c396-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="6c396-122">[in] O livro de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="6c396-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="6c396-123">Não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="6c396-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="6c396-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6c396-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="6c396-125">[out] Um alça para a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6c396-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="6c396-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="6c396-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="6c396-127">[in] Um ponteiro para uma função baseada no protótipo **DISMISSMODELESS** ou NULL.</span><span class="sxs-lookup"><span data-stu-id="6c396-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="6c396-128">Este membro aplica-se somente à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="6c396-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="6c396-129">MAPI calls the **DISMISSMODELESS function** when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span><span class="sxs-lookup"><span data-stu-id="6c396-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="6c396-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="6c396-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="6c396-131">[in] Um ponteiro para informações de contexto a ser passado para a **função DISMISSMODELESS** apontado pelo _parâmetro lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="6c396-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="6c396-132">Esse parâmetro só se aplica à versão sem modo da caixa de diálogo incluindo o sinalizador **DIALOG_SDI** no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="6c396-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="6c396-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6c396-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="6c396-134">[in] A contagem de byte do identificador de entrada especificado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="6c396-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6c396-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6c396-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="6c396-136">[in] Um ponteiro para o identificador de entrada que representa a entrada do livro de endereços a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="6c396-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="6c396-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="6c396-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="6c396-138">[in] Um ponteiro para uma função baseada no protótipo da função **LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="6c396-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="6c396-139">Uma **função LPFNBUTTON** adiciona um botão à caixa de diálogo de detalhes.</span><span class="sxs-lookup"><span data-stu-id="6c396-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="6c396-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="6c396-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="6c396-141">[in] Um ponteiro para dados que foi usado como um parâmetro para a função especificada pelo _parâmetro lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="6c396-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="6c396-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="6c396-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="6c396-143">[in] Um ponteiro para uma cadeia de caracteres que contém texto a ser aplicado ao botão adicionado, se esse botão for extensível.</span><span class="sxs-lookup"><span data-stu-id="6c396-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="6c396-144">O  _parâmetro lpszButtonText_ deve ser NULL quando não for necessário um botão extensível.</span><span class="sxs-lookup"><span data-stu-id="6c396-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="6c396-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c396-145">_ulFlags_</span></span>
  
> <span data-ttu-id="6c396-146">[in] Uma bitmask de sinalizadores que controla o tipo de texto para o _parâmetro lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="6c396-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="6c396-147">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="6c396-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="6c396-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="6c396-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="6c396-149">Indica que Details retornará TRUE se as alterações realmente foram feitas no endereço; Caso contrário, Details retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="6c396-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="6c396-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="6c396-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="6c396-151">Exibe a versão modal da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="6c396-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="6c396-152">Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="6c396-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="6c396-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="6c396-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="6c396-154">Exibe a versão sem modo da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="6c396-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="6c396-155">Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="6c396-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="6c396-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6c396-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="6c396-157">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6c396-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="6c396-158">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6c396-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

