---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432377"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="08a6e-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="08a6e-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="08a6e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08a6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08a6e-105">Define uma função de retorno de chamada invocada pelo Assistente de Perfil para permitir que um provedor de serviços reaja a eventos de usuário quando as páginas ou folhas de propriedades do provedor estão sendo mostradas.</span><span class="sxs-lookup"><span data-stu-id="08a6e-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08a6e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="08a6e-106">Header file:</span></span>  <br/> |<span data-ttu-id="08a6e-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="08a6e-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="08a6e-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="08a6e-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="08a6e-109">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="08a6e-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="08a6e-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="08a6e-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="08a6e-111">Assistente de Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="08a6e-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="08a6e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08a6e-112">Parameters</span></span>

<span data-ttu-id="08a6e-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="08a6e-113">_hDlg_</span></span>
  
> <span data-ttu-id="08a6e-114">[in] Alça de janela para a caixa de diálogo Assistente de Perfil.</span><span class="sxs-lookup"><span data-stu-id="08a6e-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="08a6e-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="08a6e-115">_wMsgID_</span></span>
  
> <span data-ttu-id="08a6e-116">[in] A mensagem da janela a ser processada.</span><span class="sxs-lookup"><span data-stu-id="08a6e-116">[in] The window message to be processed.</span></span> <span data-ttu-id="08a6e-117">Além das mensagens de janela regular esperadas por uma caixa de diálogo modal, as seguintes mensagens podem ser recebidas:</span><span class="sxs-lookup"><span data-stu-id="08a6e-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="08a6e-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="08a6e-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="08a6e-119">O Assistente de Perfil foi concluído.</span><span class="sxs-lookup"><span data-stu-id="08a6e-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="08a6e-120">O provedor de serviços deve fazer toda a limpeza necessária, como desalocar qualquer memória alocada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="08a6e-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="08a6e-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="08a6e-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="08a6e-122">Um dos controles do provedor foi  selecionado  ou o botão Próximo ou Voltar foi clicado.</span><span class="sxs-lookup"><span data-stu-id="08a6e-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="08a6e-123">O valor no  _parâmetro wParam_ indica quais desses eventos de usuário ocorreram.</span><span class="sxs-lookup"><span data-stu-id="08a6e-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="08a6e-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="08a6e-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="08a6e-125">O usuário foi movido para outra página de propriedades, para a qual a caixa de diálogo deve ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="08a6e-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="08a6e-126">O provedor deve inicializar os controles que o Assistente de Perfil adicionou à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="08a6e-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="08a6e-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="08a6e-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="08a6e-128">O Assistente de Perfil está solicitando o número de páginas que o provedor precisa exibir.</span><span class="sxs-lookup"><span data-stu-id="08a6e-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="08a6e-129">O provedor deve retornar o número de páginas em vez de VERDADEIRO ou FALSO.</span><span class="sxs-lookup"><span data-stu-id="08a6e-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="08a6e-130">Por exemplo, use a seguinte instrução de retorno para indicar que três páginas devem ser exibidas:</span><span class="sxs-lookup"><span data-stu-id="08a6e-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="08a6e-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="08a6e-131">_wParam_</span></span>
  
> <span data-ttu-id="08a6e-132">[in] Um parâmetro de 32 bits associado a mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="08a6e-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="08a6e-133">Os valores possíveis dependem da mensagem especificada no _parâmetro wMsgID._</span><span class="sxs-lookup"><span data-stu-id="08a6e-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="08a6e-134">Além dos valores esperados com as mensagens de janela regular para uma caixa de diálogo modal, os seguintes valores podem ser recebidos:</span><span class="sxs-lookup"><span data-stu-id="08a6e-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="08a6e-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="08a6e-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="08a6e-136">Quando  _wMsgID_ contém WM_COMMAND, o usuário clicou no **botão** Próximo.</span><span class="sxs-lookup"><span data-stu-id="08a6e-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="08a6e-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="08a6e-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="08a6e-138">Quando  _wMsgID_ contém WM_COMMAND, o usuário clicou no **botão** Voltar.</span><span class="sxs-lookup"><span data-stu-id="08a6e-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="08a6e-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="08a6e-139">_lParam_</span></span>
  
> <span data-ttu-id="08a6e-140">[in] Um parâmetro de 32 bits associado a mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="08a6e-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="08a6e-141">Os valores possíveis dependem da mensagem especificada no _parâmetro wMsgID._</span><span class="sxs-lookup"><span data-stu-id="08a6e-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="08a6e-142">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="08a6e-142">Return value</span></span>

<span data-ttu-id="08a6e-143">O valor retornado por **uma função baseada em SERVICEWIZARDDLGPROC** depende da mensagem de janela recebida.</span><span class="sxs-lookup"><span data-stu-id="08a6e-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="08a6e-144">Observe, em particular, o valor de retorno excepcional da WIZ_QUERYNUMPAGES mensagem.</span><span class="sxs-lookup"><span data-stu-id="08a6e-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="08a6e-145">Os valores de retorno normais são:</span><span class="sxs-lookup"><span data-stu-id="08a6e-145">The normal return values are:</span></span> 
  
<span data-ttu-id="08a6e-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="08a6e-146">TRUE</span></span> 
  
> <span data-ttu-id="08a6e-147">O provedor de serviços processou a mensagem de janela recebida.</span><span class="sxs-lookup"><span data-stu-id="08a6e-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="08a6e-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="08a6e-148">FALSE</span></span> 
  
> <span data-ttu-id="08a6e-149">O provedor de serviços não processou a mensagem de janela recebida.</span><span class="sxs-lookup"><span data-stu-id="08a6e-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08a6e-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="08a6e-150">Remarks</span></span>

<span data-ttu-id="08a6e-151">Quando o usuário se move de uma página de propriedades para outra, o provedor é responsável por ocultar os controles da página antiga e mostrar os controles da página seguinte ou anterior.</span><span class="sxs-lookup"><span data-stu-id="08a6e-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="08a6e-152">Quando o usuário  clica no botão Próximo, a função baseada **SERVICEWIZARDDLGPROC** é chamada com a mensagem WM_COMMAND e WIZ_NEXT no parâmetro _wParam._</span><span class="sxs-lookup"><span data-stu-id="08a6e-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="08a6e-153">As etapas a seguir descrevem o que ocorre entre o momento em que o usuário clica em **Next** e a hora em que as páginas de configuração do primeiro provedor são renderizadas.</span><span class="sxs-lookup"><span data-stu-id="08a6e-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="08a6e-154">O Assistente de Perfil oculta todos os controles que estão na janela.</span><span class="sxs-lookup"><span data-stu-id="08a6e-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="08a6e-155">O Assistente de Perfil adiciona os controles ocultos do provedor à página.</span><span class="sxs-lookup"><span data-stu-id="08a6e-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="08a6e-156">O Assistente de Perfil **chama SERVICEWIZARDDLGPROC**, enviando a WM_INITDIALOG, para que o provedor possa inicializar os controles.</span><span class="sxs-lookup"><span data-stu-id="08a6e-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="08a6e-157">O Assistente de Perfil **chama SERVICEWIZARDDLGPROC**, enviando a WIZ_QUERYNUMPAGES mensagem.</span><span class="sxs-lookup"><span data-stu-id="08a6e-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="08a6e-158">O provedor retorna o número de páginas a serem mostradas.</span><span class="sxs-lookup"><span data-stu-id="08a6e-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="08a6e-159">O Assistente de Perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WM_COMMAND com o parâmetro  _wParam_ definido como WIZ_NEXT ou WIZ_PREV.</span><span class="sxs-lookup"><span data-stu-id="08a6e-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="08a6e-160">Neste ponto, o provedor retorna FALSE {error} ou revela seus controles e retorna VERDADEIRO {success}.</span><span class="sxs-lookup"><span data-stu-id="08a6e-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="08a6e-161">Se o Assistente de Perfil passar ID_NEXT, a primeira página do provedor será exibida.</span><span class="sxs-lookup"><span data-stu-id="08a6e-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="08a6e-162">Se ID_PREV for passada, a última página será exibida.</span><span class="sxs-lookup"><span data-stu-id="08a6e-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="08a6e-163">O Assistente de Perfil chama a função **SERVICEWIZARDDLGPROC** do provedor, enviando WM_COMMAND mensagem com o parâmetro  _wParam_ definido como WIZ_NEXT ou WIZ_PREV (dependendo de qual botão o usuário clicou).</span><span class="sxs-lookup"><span data-stu-id="08a6e-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="08a6e-164">O provedor é responsável por mostrar ou ocultar seus controles e escrever seus dados para o **IMAPIProp** passado para o Assistente de Perfil para passar por sua sequência de páginas.</span><span class="sxs-lookup"><span data-stu-id="08a6e-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="08a6e-165">O provedor deverá retornar TRUE se a página seguinte ou anterior tiver sido exibida com êxito e FALSE se nem a página seguinte nem a anterior puderem ser mostradas.</span><span class="sxs-lookup"><span data-stu-id="08a6e-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="08a6e-166">O provedor precisa estar ciente de quando está saindo de sua sequência de páginas e responder adequadamente ocultando seus controles e escrevendo seus dados no perfil.</span><span class="sxs-lookup"><span data-stu-id="08a6e-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="08a6e-167">Se o usuário sair do intervalo de páginas do provedor, o Assistente de Perfil excluirá os controles ocultos do provedor da caixa de diálogo e chamará o próximo provedor ou exibirá sua próxima página se esse for o último provedor.</span><span class="sxs-lookup"><span data-stu-id="08a6e-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

