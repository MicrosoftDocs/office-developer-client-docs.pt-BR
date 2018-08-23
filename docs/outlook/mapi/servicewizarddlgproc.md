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
ms.openlocfilehash: fdd5d01b96c9ea756ee64f113ccb5119a9693668
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594464"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="5a3c7-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="5a3c7-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="5a3c7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a3c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a3c7-105">Define uma função de retorno de chamada invocada pelo Assistente de perfil para permitir que um provedor de serviços reajam a eventos quando estão sendo mostradas folhas de propriedades ou a páginas do provedor do usuário.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a3c7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5a3c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a3c7-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="5a3c7-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="5a3c7-108">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="5a3c7-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="5a3c7-109">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="5a3c7-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="5a3c7-110">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="5a3c7-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="5a3c7-111">Assistente de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="5a3c7-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="5a3c7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a3c7-112">Parameters</span></span>

<span data-ttu-id="5a3c7-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="5a3c7-113">_hDlg_</span></span>
  
> <span data-ttu-id="5a3c7-114">[in] Identificador da janela para a caixa de diálogo Assistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="5a3c7-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="5a3c7-115">_wMsgID_</span></span>
  
> <span data-ttu-id="5a3c7-116">[in] A mensagem da janela a ser processado.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-116">[in] The window message to be processed.</span></span> <span data-ttu-id="5a3c7-117">Além das mensagens de janela regular esperadas por uma caixa de diálogo de janela restrita, as seguintes mensagens podem ser recebidas:</span><span class="sxs-lookup"><span data-stu-id="5a3c7-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="5a3c7-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="5a3c7-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="5a3c7-119">O Assistente de perfil for concluído.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="5a3c7-120">O provedor de serviços deve fazer todas as limpeza necessária como desalocar qualquer dinamicamente memória alocada.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="5a3c7-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="5a3c7-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="5a3c7-122">Um dos controles do provedor foi selecionado ou o botão **Avançar** ou **Voltar** foi clicado.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="5a3c7-123">O valor no parâmetro _wParam_ indica qual desses eventos de usuário tenha ocorrido.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="5a3c7-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="5a3c7-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="5a3c7-125">O usuário foi movido para outra página de propriedade, para o qual a caixa de diálogo deve ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="5a3c7-126">O provedor deve inicializar os controles que o Assistente de perfil adicionada à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="5a3c7-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="5a3c7-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="5a3c7-128">O Assistente de perfil está solicitando o número de páginas que o provedor precisa ser exibido.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="5a3c7-129">O provedor deve retornar o número de páginas em vez de TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="5a3c7-130">Por exemplo, use a seguinte instrução de retorno para indicar que três páginas devem para ser exibida:</span><span class="sxs-lookup"><span data-stu-id="5a3c7-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="5a3c7-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="5a3c7-131">_wParam_</span></span>
  
> <span data-ttu-id="5a3c7-132">[in] Um parâmetro de 32 bits associado a mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="5a3c7-133">Os valores possíveis dependem a mensagem especificada no parâmetro _wMsgID_ .</span><span class="sxs-lookup"><span data-stu-id="5a3c7-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="5a3c7-134">Além dos valores esperados com as mensagens de janela normal para uma caixa de diálogo modal, os seguintes valores podem ser recebidos:</span><span class="sxs-lookup"><span data-stu-id="5a3c7-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="5a3c7-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="5a3c7-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="5a3c7-136">Quando _wMsgID_ contém WM_COMMAND, o usuário clicou no botão **Avançar** .</span><span class="sxs-lookup"><span data-stu-id="5a3c7-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="5a3c7-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="5a3c7-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="5a3c7-138">Quando _wMsgID_ contém WM_COMMAND, o usuário clicou no botão **Voltar** .</span><span class="sxs-lookup"><span data-stu-id="5a3c7-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="5a3c7-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="5a3c7-139">_lParam_</span></span>
  
> <span data-ttu-id="5a3c7-140">[in] Um parâmetro de 32 bits associado a mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="5a3c7-141">Os valores possíveis dependem a mensagem especificada no parâmetro _wMsgID_ .</span><span class="sxs-lookup"><span data-stu-id="5a3c7-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5a3c7-142">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5a3c7-142">Return value</span></span>

<span data-ttu-id="5a3c7-143">O valor retornado por uma função **SERVICEWIZARDDLGPROC** com base é dependente a janela mensagem recebida.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="5a3c7-144">Em particular, observe que o excepcionais para a mensagem WIZ_QUERYNUMPAGES o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="5a3c7-145">Os valores de retorno normais são:</span><span class="sxs-lookup"><span data-stu-id="5a3c7-145">The normal return values are:</span></span> 
  
<span data-ttu-id="5a3c7-146">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="5a3c7-146">TRUE</span></span> 
  
> <span data-ttu-id="5a3c7-147">O provedor de serviços tiver processado a mensagem recebida de janela.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="5a3c7-148">FALSO</span><span class="sxs-lookup"><span data-stu-id="5a3c7-148">FALSE</span></span> 
  
> <span data-ttu-id="5a3c7-149">O provedor de serviços não processado a mensagem recebida de janela.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5a3c7-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a3c7-150">Remarks</span></span>

<span data-ttu-id="5a3c7-151">Quando o usuário move na página de propriedades de um para outro, o provedor é responsável por ocultar os controles da página antiga e mostrando os controles da página anterior ou seguinte.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="5a3c7-152">Quando o usuário clica no botão **Avançar** , a função **SERVICEWIZARDDLGPROC** com base é chamada com a mensagem WM_COMMAND e WIZ_NEXT no parâmetro _wParam_ .</span><span class="sxs-lookup"><span data-stu-id="5a3c7-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="5a3c7-153">As seguintes etapas descrevem o que ocorre entre o momento em que o usuário clica em **Avançar** e o tempo de que páginas de configuração do provedor a primeira são processadas.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="5a3c7-154">O Assistente de perfil oculta todos os controles que estão na janela.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="5a3c7-155">O Assistente de perfil adiciona controles de ocultos do provedor à página.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="5a3c7-156">O Assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WM_INITDIALOG, para que o provedor pode inicializar os controles.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="5a3c7-157">O Assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WIZ_QUERYNUMPAGES.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="5a3c7-158">O provedor retorna o número de páginas que devem ser mostrados.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="5a3c7-159">O Assistente de perfil chama **SERVICEWIZARDDLGPROC**, enviando a mensagem WM_COMMAND com o parâmetro _wParam_ definido como WIZ_NEXT ou WIZ_PREV.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="5a3c7-160">Neste ponto, o provedor tanto retorna FALSE {erro} ou revela seus controles e retorna verdadeiro {sucesso}.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="5a3c7-161">Se o Assistente de perfil passa no ID_NEXT, a página do provedor primeira é exibida.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="5a3c7-162">Se ID_PREV for passado, a última página é exibida.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="5a3c7-163">O Assistente de perfil chama a função **SERVICEWIZARDDLGPROC** do provedor, enviando a mensagem WM_COMMAND com o parâmetro _wParam_ definido como WIZ_NEXT ou WIZ_PREV (dependendo de qual botão o usuário clicou).</span><span class="sxs-lookup"><span data-stu-id="5a3c7-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="5a3c7-164">O provedor é responsável por mostrar ou ocultar seus controles e gravando seus dados para o **IMAPIProp** passados para o Assistente de perfil para percorrer sua sequência de páginas.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="5a3c7-165">O provedor deve retornar TRUE se a página anterior ou seguinte foi exibida com êxito, e FALSE se nem a página próxima nem anterior puderam ser mostrada.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="5a3c7-166">O provedor precisa estar ciente quando ele está se preparando fora de sua sequência de páginas e responder apropriadamente ocultando seus controles e gravando seus dados para o perfil.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="5a3c7-167">Se o usuário etapas fora do intervalo do provedor de páginas, o Assistente de perfil e exclui a controles de ocultos do provedor de caixa de diálogo chama o provedor próximo ou exibe sua próxima página se que foi o último provedor.</span><span class="sxs-lookup"><span data-stu-id="5a3c7-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

