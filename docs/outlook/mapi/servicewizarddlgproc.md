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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356410"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="1cbed-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="1cbed-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="1cbed-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cbed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cbed-105">Define uma função de retorno de chamada invocada pelo assistente de perfil para permitir que um provedor de serviços reagir a eventos do usuário quando as folhas de propriedades ou páginas do provedor estiverem sendo mostradas.</span><span class="sxs-lookup"><span data-stu-id="1cbed-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1cbed-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1cbed-106">Header file:</span></span>  <br/> |<span data-ttu-id="1cbed-107">Mapiwz. h</span><span class="sxs-lookup"><span data-stu-id="1cbed-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="1cbed-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="1cbed-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="1cbed-109">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="1cbed-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="1cbed-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="1cbed-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="1cbed-111">Assistente de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="1cbed-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="1cbed-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cbed-112">Parameters</span></span>

<span data-ttu-id="1cbed-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="1cbed-113">_hDlg_</span></span>
  
> <span data-ttu-id="1cbed-114">no Manipulador de janela para a caixa de diálogo Assistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="1cbed-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="1cbed-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="1cbed-115">_wMsgID_</span></span>
  
> <span data-ttu-id="1cbed-116">no A mensagem da janela a ser processada.</span><span class="sxs-lookup"><span data-stu-id="1cbed-116">[in] The window message to be processed.</span></span> <span data-ttu-id="1cbed-117">Além das mensagens de janela regulares esperadas por uma caixa de diálogo modal, as seguintes mensagens podem ser recebidas:</span><span class="sxs-lookup"><span data-stu-id="1cbed-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="1cbed-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="1cbed-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="1cbed-119">O assistente de perfil foi concluído.</span><span class="sxs-lookup"><span data-stu-id="1cbed-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="1cbed-120">O provedor de serviços deve fazer todas as limpezas necessárias, como desalocar qualquer memória alocada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="1cbed-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="1cbed-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="1cbed-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="1cbed-122">Um dos controles do provedor foi selecionado ou o botão **Avançar** ou **voltar** foi clicado.</span><span class="sxs-lookup"><span data-stu-id="1cbed-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="1cbed-123">O valor no parâmetro _wParam_ indica qual desses eventos de usuário ocorreu.</span><span class="sxs-lookup"><span data-stu-id="1cbed-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="1cbed-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="1cbed-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="1cbed-125">O usuário foi movido para outra página de propriedades, para a qual a caixa de diálogo deve ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="1cbed-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="1cbed-126">O provedor deve inicializar os controles que o assistente de perfil adicionou à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1cbed-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="1cbed-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="1cbed-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="1cbed-128">O assistente de perfil está solicitando o número de páginas que o provedor precisa exibir.</span><span class="sxs-lookup"><span data-stu-id="1cbed-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="1cbed-129">O provedor deve retornar o número de páginas em vez de TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="1cbed-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="1cbed-130">Por exemplo, use a seguinte instrução de retorno para indicar que três páginas devem ser exibidas:</span><span class="sxs-lookup"><span data-stu-id="1cbed-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="1cbed-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="1cbed-131">_wParam_</span></span>
  
> <span data-ttu-id="1cbed-132">no Um parâmetro de 32 bits associado a mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="1cbed-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="1cbed-133">Os valores possíveis dependem da mensagem especificada no parâmetro _wMsgID_ .</span><span class="sxs-lookup"><span data-stu-id="1cbed-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="1cbed-134">Além dos valores esperados com as mensagens de janela regulares de uma caixa de diálogo modal, os seguintes valores podem ser recebidos:</span><span class="sxs-lookup"><span data-stu-id="1cbed-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="1cbed-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="1cbed-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="1cbed-136">Quando _wMsgID_ contiver WM_COMMAND, o usuário clicou no botão **Avançar** .</span><span class="sxs-lookup"><span data-stu-id="1cbed-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="1cbed-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="1cbed-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="1cbed-138">Quando _wMsgID_ contiver WM_COMMAND, o usuário clicou no botão **voltar** .</span><span class="sxs-lookup"><span data-stu-id="1cbed-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="1cbed-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="1cbed-139">_lParam_</span></span>
  
> <span data-ttu-id="1cbed-140">no Um parâmetro de 32 bits associado a mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="1cbed-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="1cbed-141">Os valores possíveis dependem da mensagem especificada no parâmetro _wMsgID_ .</span><span class="sxs-lookup"><span data-stu-id="1cbed-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1cbed-142">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1cbed-142">Return value</span></span>

<span data-ttu-id="1cbed-143">O valor retornado por uma função baseada em **SERVICEWIZARDDLGPROC** depende da mensagem de janela recebida.</span><span class="sxs-lookup"><span data-stu-id="1cbed-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="1cbed-144">Observe em particular o valor de retorno excepcional para a mensagem WIZ_QUERYNUMPAGES.</span><span class="sxs-lookup"><span data-stu-id="1cbed-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="1cbed-145">Os valores de retorno normais são:</span><span class="sxs-lookup"><span data-stu-id="1cbed-145">The normal return values are:</span></span> 
  
<span data-ttu-id="1cbed-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="1cbed-146">TRUE</span></span> 
  
> <span data-ttu-id="1cbed-147">O provedor de serviços processou a mensagem de janela recebida.</span><span class="sxs-lookup"><span data-stu-id="1cbed-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="1cbed-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="1cbed-148">FALSE</span></span> 
  
> <span data-ttu-id="1cbed-149">O provedor de serviços não processou a mensagem de janela recebida.</span><span class="sxs-lookup"><span data-stu-id="1cbed-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1cbed-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cbed-150">Remarks</span></span>

<span data-ttu-id="1cbed-151">Quando o usuário move de uma página de propriedades para outra, o provedor é responsável por ocultar os controles da página antiga e mostrar os controles da página seguinte ou anterior.</span><span class="sxs-lookup"><span data-stu-id="1cbed-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="1cbed-152">Quando o usuário clica no botão **Avançar** , a função baseada em **SERVICEWIZARDDLGPROC** é chamada com a mensagem WM_COMMAND e WIZ_NEXT no parâmetro _wParam_ .</span><span class="sxs-lookup"><span data-stu-id="1cbed-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="1cbed-153">As etapas a seguir descrevem o que ocorre entre o momento em que o usuário clica **em Avançar** e a hora em que as páginas de configuração do primeiro provedor são renderizadas.</span><span class="sxs-lookup"><span data-stu-id="1cbed-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="1cbed-154">O assistente de perfil oculta os controles que estão na janela.</span><span class="sxs-lookup"><span data-stu-id="1cbed-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="1cbed-155">O assistente de perfil adiciona os controles ocultos do provedor à página.</span><span class="sxs-lookup"><span data-stu-id="1cbed-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="1cbed-156">O assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WM_INITDIALOG, para que o provedor possa inicializar os controles.</span><span class="sxs-lookup"><span data-stu-id="1cbed-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="1cbed-157">O assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WIZ_QUERYNUMPAGES.</span><span class="sxs-lookup"><span data-stu-id="1cbed-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="1cbed-158">O provedor retorna o número de páginas que devem ser mostradas.</span><span class="sxs-lookup"><span data-stu-id="1cbed-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="1cbed-159">O assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WM_COMMAND com o parâmetro _wParam_ definido como WIZ_NEXT ou WIZ_PREV.</span><span class="sxs-lookup"><span data-stu-id="1cbed-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="1cbed-160">Neste ponto, o provedor retorna FALSE {erro} ou revela seus controles e retorna TRUE {Success}.</span><span class="sxs-lookup"><span data-stu-id="1cbed-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="1cbed-161">Se o assistente de perfil passar no ID_NEXT, a primeira página do provedor será exibida.</span><span class="sxs-lookup"><span data-stu-id="1cbed-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="1cbed-162">Se ID_PREV for passado, a última página é exibida.</span><span class="sxs-lookup"><span data-stu-id="1cbed-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="1cbed-163">O assistente de perfil chama a função **SERVICEWIZARDDLGPROC** do provedor, enviando a mensagem WM_COMMAND com o parâmetro _wParam_ definido como WIZ_NEXT ou WIZ_PREV (dependendo de qual botão o usuário clicou).</span><span class="sxs-lookup"><span data-stu-id="1cbed-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="1cbed-164">O provedor é responsável por mostrar ou ocultar seus controles e gravar seus dados no **IMAPIProp** passado para o assistente de perfil para percorrer sua sequência de páginas.</span><span class="sxs-lookup"><span data-stu-id="1cbed-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="1cbed-165">O provedor deve retornar TRUE se a página seguinte ou anterior for exibida com êxito e FALSE se nem a página seguinte ou anterior puder ser exibida.</span><span class="sxs-lookup"><span data-stu-id="1cbed-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="1cbed-166">O provedor precisa estar ciente de quando estiver Depurando fora de sua sequência de páginas e responder de forma adequada, ocultando seus controles e gravando seus dados no perfil.</span><span class="sxs-lookup"><span data-stu-id="1cbed-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="1cbed-167">Se o usuário seguir as etapas de fora do intervalo de páginas do provedor, o assistente de perfil excluirá os controles ocultos do provedor da caixa de diálogo e chamará o próximo provedor ou exibirá sua próxima página se esse for o último provedor.</span><span class="sxs-lookup"><span data-stu-id="1cbed-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

