---
title: Interfaces da caixa de diálogo Arquivamento Rápido (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: Este tópico descreve as interfaces que você pode usar para personalizar programaticamente a caixa de diálogo Arquivamento Rápido no OneNote 2013.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425334"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a><span data-ttu-id="b713a-103">Interfaces da caixa de diálogo Arquivamento Rápido (OneNote)</span><span class="sxs-lookup"><span data-stu-id="b713a-103">Quick Filing dialog box interfaces (OneNote)</span></span>

<span data-ttu-id="b713a-104">Este tópico descreve as interfaces que você pode usar para personalizar programaticamente a caixa de diálogo Arquivamento Rápido no OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="b713a-104">This topic describes the interfaces that you can use to programmatically customize the Quick Filing dialog box in OneNote 2013.</span></span>
  
## <a name="quick-filing-dialog-box"></a><span data-ttu-id="b713a-105">Caixa de diálogo Arquivamento Rápido</span><span class="sxs-lookup"><span data-stu-id="b713a-105">Quick Filing dialog box</span></span>

<span data-ttu-id="b713a-106">A caixa de diálogo Arquivamento Rápido no OneNote 2013 é uma caixa de diálogo personalizável que permite aos usuários selecionar um local dentro da estrutura de hierarquia do OneNote.</span><span class="sxs-lookup"><span data-stu-id="b713a-106">The Quick Filing dialog box in OneNote 2013 is a customizable dialog box that allows users to select a location within the OneNote hierarchy structure.</span></span> <span data-ttu-id="b713a-107">Os locais selecionáveis incluem blocos de anotações, grupos de seções, seções, páginas e subpages.</span><span class="sxs-lookup"><span data-stu-id="b713a-107">Selectable locations include notebooks, section groups, sections, pages, and subpages.</span></span> <span data-ttu-id="b713a-108">A caixa de diálogo é usada dentro do aplicativo OneNote e por aplicativos externos por meio da API do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="b713a-108">The dialog box is used both within the OneNote application and by external applications through the OneNote 2013 API.</span></span> <span data-ttu-id="b713a-109">A Figura 1 mostra a caixa de diálogo Arquivamento Rápido em seu estado padrão.</span><span class="sxs-lookup"><span data-stu-id="b713a-109">Figure 1 shows the Quick Filing dialog box in its default state.</span></span>
  
<span data-ttu-id="b713a-110">**Figura 1. Caixa de diálogo Arquivamento Rápido sem personalizações**</span><span class="sxs-lookup"><span data-stu-id="b713a-110">**Figure 1. Quick Filing dialog box without customizations**</span></span>

<span data-ttu-id="b713a-111">![Caixa de diálogo Arquivamento Rápido sem personalizações]caixa de diálogo Arquivamento(media/ON15Con_quick_filing_dialog.jpg "Rápido sem personalizações")</span><span class="sxs-lookup"><span data-stu-id="b713a-111">![Quick Filing dialog box without customizations](media/ON15Con_quick_filing_dialog.jpg "Quick Filing dialog box without customizations")</span></span>
  
<span data-ttu-id="b713a-112">Na caixa de diálogo, os usuários podem navegar na hierarquia Todos os Blocos de Anotações para procurar locais específicos ou pesquisar a estrutura da árvore do OneNote digitando na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="b713a-112">Within the dialog box, users can navigate the All Notebooks hierarchy to look for specific locations or search the OneNote tree structure by typing into the text box.</span></span> <span data-ttu-id="b713a-113">Os aspectos da caixa de diálogo que podem ser personalizados incluem título, descrição, lista de resultados recentes, texto e estado da caixa de seleção, profundidade da árvore, botões e tipos de local selecionáveis.</span><span class="sxs-lookup"><span data-stu-id="b713a-113">Aspects of the dialog box that can be customized include the title, description, recent results list, check box text and state, tree depth, buttons, and selectable location types.</span></span>

<span data-ttu-id="b713a-114">Você pode acessar a funcionalidade da caixa de diálogo Arquivamento Rápido por meio de duas interfaces do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="b713a-114">You can access the Quick Filing dialog box functionality through two OneNote 2013 interfaces.</span></span> <span data-ttu-id="b713a-115">A interface **IQuickFilingDialog** permite que os usuários inciar, configurar e executar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-115">The **IQuickFilingDialog** interface allows users to instantiate, set up, and run the dialog box.</span></span> <span data-ttu-id="b713a-116">A interface **IQuickFilingDialogCallback** é chamada depois que a caixa de diálogo é fechada.</span><span class="sxs-lookup"><span data-stu-id="b713a-116">The **IQuickFilingDialogCallback** interface is called after the dialog box is closed.</span></span> <span data-ttu-id="b713a-117">A caixa de diálogo é executado no processo do OneNote, portanto, é necessário um mecanismo para manter o thread da caixa de diálogo em execução e, em seguida, capturar a seleção do usuário e o estado da caixa de diálogo quando ela for fechada.</span><span class="sxs-lookup"><span data-stu-id="b713a-117">The dialog box is run in the OneNote process, so a mechanism is needed to keep the dialog box's thread running and then to capture the user's selection and the state of the dialog box when it is closed.</span></span> 
  
## <a name="iquickfilingdialog-interface"></a><span data-ttu-id="b713a-118">Interface IQuickFilingDialog</span><span class="sxs-lookup"><span data-stu-id="b713a-118">IQuickFilingDialog interface</span></span>
<span data-ttu-id="b713a-119"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="b713a-119"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="b713a-120">Essa interface permite que o usuário personalize e execute a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-120">This interface allows the user to customize and run the dialog box.</span></span> <span data-ttu-id="b713a-121">O usuário pode inciar uma caixa de diálogo por meio da classe **Application** usando o **método Application.QuickFilingDialog.**</span><span class="sxs-lookup"><span data-stu-id="b713a-121">The user can instantiate a dialog box through the **Application** class by using the **Application.QuickFilingDialog** method.</span></span> <span data-ttu-id="b713a-122">O método retorna uma instância da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-122">The method returns an instance of the dialog box.</span></span> <span data-ttu-id="b713a-123">Depois que as propriedades da caixa de diálogo são definidas, o método **IQuickFilingDialog.Run** é usado para executar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-123">Once the properties of the dialog box are set, the **IQuickFilingDialog.Run** method is used to run the dialog box.</span></span> <span data-ttu-id="b713a-124">Esse método executa a caixa de diálogo em um novo thread.</span><span class="sxs-lookup"><span data-stu-id="b713a-124">This method runs the dialog box on a new thread.</span></span> 
  
<span data-ttu-id="b713a-125">**Propriedades**</span><span class="sxs-lookup"><span data-stu-id="b713a-125">**Properties**</span></span>

|<span data-ttu-id="b713a-126">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b713a-126">**Name**</span></span>|<span data-ttu-id="b713a-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b713a-127">**Type**</span></span>|<span data-ttu-id="b713a-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b713a-129">**Title**</span><span class="sxs-lookup"><span data-stu-id="b713a-129">**Title**</span></span> <br/> |<span data-ttu-id="b713a-130">string</span><span class="sxs-lookup"><span data-stu-id="b713a-130">string</span></span>  <br/> |<span data-ttu-id="b713a-131">Obtém ou define o texto do título que aparece na barra de título da janela da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-131">Gets or sets the title text that appears in the title bar of the dialog box window.</span></span>  <br/> |
|<span data-ttu-id="b713a-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-132">**Description**</span></span> <br/> |<span data-ttu-id="b713a-133">string</span><span class="sxs-lookup"><span data-stu-id="b713a-133">string</span></span>  <br/> |<span data-ttu-id="b713a-134">Obtém ou define a descrição do texto para instruir o usuário sobre o que selecionar.</span><span class="sxs-lookup"><span data-stu-id="b713a-134">Gets or sets the text description to instruct the user about what to select.</span></span> <span data-ttu-id="b713a-135">Esse valor pode ser texto de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="b713a-135">This value can be multiple-line text.</span></span>  <br/> |
|<span data-ttu-id="b713a-136">**CheckboxText**</span><span class="sxs-lookup"><span data-stu-id="b713a-136">**CheckboxText**</span></span> <br/> |<span data-ttu-id="b713a-137">string</span><span class="sxs-lookup"><span data-stu-id="b713a-137">string</span></span>  <br/> |<span data-ttu-id="b713a-138">Obtém ou define o texto que segue a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="b713a-138">Gets or sets the text that follows the check box.</span></span> <span data-ttu-id="b713a-139">Se esse valor for definido como uma cadeia de caracteres não vazia, uma caixa de seleção será exibida na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-139">If this value is set to a non-empty string, a check box appears in the dialog box.</span></span> <span data-ttu-id="b713a-140">Se o valor for uma cadeia de caracteres vazia, nenhuma caixa de seleção será exibida.</span><span class="sxs-lookup"><span data-stu-id="b713a-140">If the value is an empty string, no check box appears.</span></span>  <br/> |
|<span data-ttu-id="b713a-141">**CheckboxState**</span><span class="sxs-lookup"><span data-stu-id="b713a-141">**CheckboxState**</span></span> <br/> |<span data-ttu-id="b713a-142">bool</span><span class="sxs-lookup"><span data-stu-id="b713a-142">bool</span></span>  <br/> |<span data-ttu-id="b713a-143">Obtém ou define o estado da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="b713a-143">Gets or sets the state of the check box.</span></span> <span data-ttu-id="b713a-144">Se o valor for definido como **false,** a caixa de seleção será des limpa quando a caixa de diálogo for iniciada.</span><span class="sxs-lookup"><span data-stu-id="b713a-144">If value is set to **false**, the check box is cleared when the dialog box is started.</span></span> <span data-ttu-id="b713a-145">Se o valor for definido como **true**, a caixa de seleção será marcada quando a caixa de diálogo for iniciada, desde que **CheckboxText** seja uma cadeia de caracteres não vazia.</span><span class="sxs-lookup"><span data-stu-id="b713a-145">If the value is set to **true**, the check box is selected when the dialog box is started as long as **CheckboxText** is a non-empty string.</span></span>  <br/> |
|<span data-ttu-id="b713a-146">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="b713a-146">**WindowHandle**</span></span> <br/> |<span data-ttu-id="b713a-147">ULong</span><span class="sxs-lookup"><span data-stu-id="b713a-147">ulong</span></span>  <br/> |<span data-ttu-id="b713a-148">Obtém a ID de alça da janela da caixa de diálogo Arquivamento Rápido.</span><span class="sxs-lookup"><span data-stu-id="b713a-148">Gets the handle ID of the Quick Filing dialog box window.</span></span>  <br/> |
|<span data-ttu-id="b713a-149">**TreeDepth**</span><span class="sxs-lookup"><span data-stu-id="b713a-149">**TreeDepth**</span></span> <br/> |<span data-ttu-id="b713a-150">**HierarchyElement**</span><span class="sxs-lookup"><span data-stu-id="b713a-150">**HierarchyElement**</span></span> <br/> |<span data-ttu-id="b713a-151">Obtém ou define a profundidade em que a árvore do OneNote deve ser exibida na seção Todos os Blocos de Anotações.</span><span class="sxs-lookup"><span data-stu-id="b713a-151">Gets or sets how deep the OneNote tree should be displayed in the All Notebooks section.</span></span> <span data-ttu-id="b713a-152">Por padrão, a árvore é exibida até as seções.</span><span class="sxs-lookup"><span data-stu-id="b713a-152">By default, the tree is displayed up to the sections.</span></span> <span data-ttu-id="b713a-153">Essa propriedade não afeta que tipo de elementos podem ser selecionados.</span><span class="sxs-lookup"><span data-stu-id="b713a-153">This property does not affect what type of elements can be selected.</span></span>  <br/> <span data-ttu-id="b713a-154">Se **TreeDepth** for definido como um elemento inferior na hierarquia do OneNote do que pode ser selecionado por qualquer um dos botões, a profundidade da árvore exibida será o elemento selecionável mais baixo possível.</span><span class="sxs-lookup"><span data-stu-id="b713a-154">If **TreeDepth** is set to an element lower in the OneNote hierarchy than can be selected by any of the buttons, the displayed tree depth will be the lowest possible selectable element.</span></span> <span data-ttu-id="b713a-155">Ou seja, se a profundidade da árvore estiver definida para ser exibida para baixo nas páginas, mas o elemento selecionável mais baixo for uma seção, a árvore será exibida para baixo até as seções.</span><span class="sxs-lookup"><span data-stu-id="b713a-155">That is, if tree depth is set to display down to pages, but the lowest selectable element is a section, the tree is displayed down to sections.</span></span>  <br/> |
|<span data-ttu-id="b713a-156">**ParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="b713a-156">**ParentWindowHandle**</span></span> <br/> |<span data-ttu-id="b713a-157">ULong</span><span class="sxs-lookup"><span data-stu-id="b713a-157">ulong</span></span>  <br/> |<span data-ttu-id="b713a-158">Obtém ou define a ID de alça da janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-158">Gets or sets the handle ID of the parent window of the dialog box.</span></span> <span data-ttu-id="b713a-159">Se essa propriedade for definida, a caixa de diálogo Arquivamento Rápido será modal para a janela pai atribuída quando a caixa de diálogo for aberta.</span><span class="sxs-lookup"><span data-stu-id="b713a-159">If this property is set, the Quick Filing dialog box will be modal to the assigned parent window when the dialog box opens.</span></span> <span data-ttu-id="b713a-160">Ou seja, um usuário não poderá acessar a janela pai até que a caixa de diálogo Arquivamento Rápido seja fechada.</span><span class="sxs-lookup"><span data-stu-id="b713a-160">That is, a user will not be able to access the parent window until the Quick Filing dialog box is closed.</span></span>  <br/> |
|<span data-ttu-id="b713a-161">**Posição**</span><span class="sxs-lookup"><span data-stu-id="b713a-161">**Position**</span></span> <br/> |<span data-ttu-id="b713a-162">tagPOINT</span><span class="sxs-lookup"><span data-stu-id="b713a-162">tagPOINT</span></span>  <br/> |<span data-ttu-id="b713a-163">Obtém ou define a posição da janela em relação à tela.</span><span class="sxs-lookup"><span data-stu-id="b713a-163">Gets or sets the position of the window in relation to the screen.</span></span> <span data-ttu-id="b713a-164">Por padrão, a caixa de diálogo aparece no meio da janela pai ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b713a-164">By default, the dialog box appears in the middle of the parent window or the desktop.</span></span>  <br/> |
|<span data-ttu-id="b713a-165">**SelectedItem**</span><span class="sxs-lookup"><span data-stu-id="b713a-165">**SelectedItem**</span></span> <br/> |<span data-ttu-id="b713a-166">string</span><span class="sxs-lookup"><span data-stu-id="b713a-166">string</span></span>  <br/> |<span data-ttu-id="b713a-167">Obtém a ID do objeto do local do OneNote selecionado pelo usuário quando a caixa de diálogo é fechada.</span><span class="sxs-lookup"><span data-stu-id="b713a-167">Gets the object ID of the OneNote location selected by the user when the dialog box is closed.</span></span> <span data-ttu-id="b713a-168">Se o usuário clicar no **botão Cancelar,** o objeto será definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="b713a-168">If the user clicks the **Cancel** button, the object is set to null.</span></span>  <br/> |
|<span data-ttu-id="b713a-169">**PressedButton**</span><span class="sxs-lookup"><span data-stu-id="b713a-169">**PressedButton**</span></span> <br/> |<span data-ttu-id="b713a-170">ULong</span><span class="sxs-lookup"><span data-stu-id="b713a-170">ulong</span></span>  <br/> |<span data-ttu-id="b713a-171">Obtém qual botão foi clicado quando a caixa de diálogo foi fechada.</span><span class="sxs-lookup"><span data-stu-id="b713a-171">Gets which button was clicked when the dialog box was closed.</span></span> <span data-ttu-id="b713a-172">Se o **botão Cancelar** tiver sido clicado, essa propriedade retornará um valor de -1.</span><span class="sxs-lookup"><span data-stu-id="b713a-172">If the **Cancel** button was clicked, this property returns a value of -1.</span></span> <span data-ttu-id="b713a-173">Todos os outros botões são atribuídos valores inteiros de 0, incrementados em 1 para cada botão adicionado à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-173">All other buttons are assigned integer values from 0, incremented by 1 for each button added to the dialog box.</span></span> <span data-ttu-id="b713a-174">O valor inteiro do botão **OK** padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="b713a-174">The integer value of the default **OK** button is 0.</span></span>  <br/> |
   
### <a name="methods"></a><span data-ttu-id="b713a-175">Methods</span><span class="sxs-lookup"><span data-stu-id="b713a-175">Methods</span></span>

<span data-ttu-id="b713a-176">**SetRecentResults**</span><span class="sxs-lookup"><span data-stu-id="b713a-176">**SetRecentResults**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b713a-177">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-177">**Description**</span></span> <br/> |<span data-ttu-id="b713a-178">Define qual lista de resultados recentes será exibida na caixa de diálogo Arquivamento Rápido e indica se deve incluir alguns locais de arquivamento especiais na lista.</span><span class="sxs-lookup"><span data-stu-id="b713a-178">Sets what recent result list will be displayed in the Quick Filing dialog box, and indicates whether to include some special filing locations in the list.</span></span> <span data-ttu-id="b713a-179">Os usuários podem selecionar uma lista de resultados recentes na [enumeração RecentResultType.](enumerations-onenote-developer-reference.md#odc_RecentResultType)</span><span class="sxs-lookup"><span data-stu-id="b713a-179">Users can select a recent result list from the [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) enumeration.</span></span> <span data-ttu-id="b713a-180">Os usuários também podem optar por adicionar as seguintes opções à lista: Seção Atual, Página Atual ou Anotações Não-Preenchedas.</span><span class="sxs-lookup"><span data-stu-id="b713a-180">Users can also choose to add the following options to the list: Current Section, Current Page, or Unfiled Notes.</span></span> <span data-ttu-id="b713a-181">Se **RecentResultType.rrtNone** estiver selecionado, nenhuma lista de resultados recentes será exibida.</span><span class="sxs-lookup"><span data-stu-id="b713a-181">If **RecentResultType.rrtNone** is selected, no recent result list is shown.</span></span>  <br/> |
|<span data-ttu-id="b713a-182">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b713a-182">**Syntax**</span></span> <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|<span data-ttu-id="b713a-183">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="b713a-183">**Parameters**</span></span> <br/> | <span data-ttu-id="b713a-184">_recentResults_ &ndash; Um objeto do tipo **RecentResultType** que indica qual lista de resultados recentes, se alguma, deve aparecer.</span><span class="sxs-lookup"><span data-stu-id="b713a-184">_recentResults_ &ndash; An object of type **RecentResultType** that indicates which recent result list, if any, should appear.</span></span> <span data-ttu-id="b713a-185">Se **rrtNone** estiver selecionado, nenhuma lista de resultados recentes será exibida na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-185">If **rrtNone** is selected, no recent result list appears in the dialog box.</span></span><br/><br/>  <span data-ttu-id="b713a-186">_fShowCurrentSection_ &ndash; Um valor Boolean que indica se a seção atual deve ser incluída na lista de resultados recentes.</span><span class="sxs-lookup"><span data-stu-id="b713a-186">_fShowCurrentSection_ &ndash; A Boolean value that indicates whether the current section should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="b713a-187">_fShowCurrentPage_ &ndash; Um valor Boolean que indica se a página atual deve ser incluída na lista de resultados recentes.</span><span class="sxs-lookup"><span data-stu-id="b713a-187">_fShowCurrentPage_ &ndash; A Boolean value that indicates whether the current page should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="b713a-188">_fShowUnfiledNotes_ &ndash; Um valor booliana que indica se a seção Anotações Não Explicadas deve ser incluída na lista de resultados recentes.</span><span class="sxs-lookup"><span data-stu-id="b713a-188">_fShowUnfiledNotes_ &ndash; A Boolean value that indicates whether the Unfiled Notes section should be included in the recent result list.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b713a-189">Se um local de arquivamento especial não puder ser selecionado usando qualquer um dos botões na caixa de diálogo, ele não será mostrado na lista.</span><span class="sxs-lookup"><span data-stu-id="b713a-189">If a special filing location cannot be selected by using any of the buttons in the dialog box, it is not shown in the list.</span></span> <span data-ttu-id="b713a-190">Se nenhum item selecionável na lista de resultados recentes for encontrado, nenhuma lista de resultados recentes será exibida.</span><span class="sxs-lookup"><span data-stu-id="b713a-190">If no selectable item in the recent results list is found, no recent result list is displayed.</span></span> 
  
<span data-ttu-id="b713a-191">O exemplo a seguir usa o **método SetRecentResults** para exibir a seção atual, a página atual e a seção Anotações NãoFiladas na lista de resultados recentes.</span><span class="sxs-lookup"><span data-stu-id="b713a-191">The following example uses the **SetRecentResults** method to display the current section, current page, and the Unfiled Notes section in the recent result list.</span></span> 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

<span data-ttu-id="b713a-192">**AddButton**</span><span class="sxs-lookup"><span data-stu-id="b713a-192">**AddButton**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b713a-193">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-193">**Description**</span></span> <br/> |<span data-ttu-id="b713a-194">Permite que os usuários adicionem e personalizem botões na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-194">Allows users to add and customize buttons in the dialog box.</span></span> <span data-ttu-id="b713a-195">Os usuários podem especificar o texto nos botões e quais elementos da hierarquia do OneNote podem ser selecionados por cada botão.</span><span class="sxs-lookup"><span data-stu-id="b713a-195">Users can specify the text on the buttons and what elements of the OneNote hierarchy can be selected by each button.</span></span>  <br/> |
|<span data-ttu-id="b713a-196">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b713a-196">**Syntax**</span></span> <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|<span data-ttu-id="b713a-197">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="b713a-197">**Parameters**</span></span> <br/> | <span data-ttu-id="b713a-198">_bstrText_ &ndash; Uma cadeia de caracteres que especifica o texto a ser exibido no botão.</span><span class="sxs-lookup"><span data-stu-id="b713a-198">_bstrText_ &ndash; A string that specifies the text to appear on the button.</span></span> <span data-ttu-id="b713a-199">Para personalizar o botão **OK** padrão, passe um valor nulo como **bstrText**.</span><span class="sxs-lookup"><span data-stu-id="b713a-199">To customize the default **OK** button, pass in a null value as **bstrText**.</span></span>  <br/><br/><span data-ttu-id="b713a-200">_allowedElements_ &ndash; Um **HierarchyElement** que indica quais elementos de hierarquia do OneNote não somente leitura um usuário tem permissão para selecionar usando o botão.</span><span class="sxs-lookup"><span data-stu-id="b713a-200">_allowedElements_ &ndash; A **HierarchyElement** that indicates what non-read-only OneNote hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="b713a-201">Para selecionar vários itens, o usuário deve passar o operador **OR** para todos os valores equivalentes uint dos tipos **HierarchyElement** permitidos como **um HierarchyElement**.</span><span class="sxs-lookup"><span data-stu-id="b713a-201">For selecting multiple items, the user should pass in the **OR** operator for all the uint equivalent values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="b713a-202">_allowedReadOnlyElements_ &ndash; Um **HierarchyElement** que indica quais elementos de hierarquia somente leitura do OneNote um usuário tem permissão para selecionar usando o botão.</span><span class="sxs-lookup"><span data-stu-id="b713a-202">_allowedReadOnlyElements_ &ndash; A **HierarchyElement** that indicates what OneNote read-only hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="b713a-203">Para selecionar vários itens, o usuário deve passar o operador **OR** para todos os **valores equivalentes uint** dos tipos **HierarchyElement** permitidos como **um HierarchyElement**.</span><span class="sxs-lookup"><span data-stu-id="b713a-203">For selecting multiple items, the user should pass in the **OR** operator for all the **uint** equivalents values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="b713a-204">_fDefault_ &ndash; Um valor Boolean que especifica se esse botão deve ser o botão padrão.</span><span class="sxs-lookup"><span data-stu-id="b713a-204">_fDefault_ &ndash; A Boolean value that specifies whether this button should be the default button.</span></span> <span data-ttu-id="b713a-205">Se vários botões são definidos como padrão, o último botão especificado se torna o botão padrão.</span><span class="sxs-lookup"><span data-stu-id="b713a-205">If multiple buttons are set as default, the last specified button becomes the default button.</span></span>  <br/> |
   
<span data-ttu-id="b713a-206">O exemplo a seguir adiciona três botões à caixa de diálogo Arquivamento Rápido.</span><span class="sxs-lookup"><span data-stu-id="b713a-206">The following example adds three buttons to the Quick Filing dialog box.</span></span> <span data-ttu-id="b713a-207">O primeiro, **All**, pode ser selecionado por todos os elementos na árvore de hierarquia do OneNote.</span><span class="sxs-lookup"><span data-stu-id="b713a-207">The first one, **All**, can be selected by all elements in the OneNote hierarchy tree.</span></span> <span data-ttu-id="b713a-208">Os outros, **Blocos de** Anotações e **Páginas**, só poderão ser selecionados se seus elementos correspondentes, Blocos de Anotações e Páginas, forem selecionados.</span><span class="sxs-lookup"><span data-stu-id="b713a-208">The others, **Notebooks** and **Pages**, can be selected only if their corresponding elements, Notebooks and Pages, are selected.</span></span>
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

<span data-ttu-id="b713a-209">**Run**</span><span class="sxs-lookup"><span data-stu-id="b713a-209">**Run**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b713a-210">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-210">**Description**</span></span> <br/> |<span data-ttu-id="b713a-211">Exibe a caixa de diálogo Arquivamento Rápido de um novo thread.</span><span class="sxs-lookup"><span data-stu-id="b713a-211">Displays the Quick Filing dialog box from a new thread.</span></span> <span data-ttu-id="b713a-212">Ele faz referência à interface **IQuickFilingDialogCallback,** cujo método **OnDialogClosed** será chamado assim que a caixa de diálogo for fechado.</span><span class="sxs-lookup"><span data-stu-id="b713a-212">It takes a reference to the **IQuickFilingDialogCallback** interface, whose **OnDialogClosed** method will be called once the dialog box closes.</span></span>  <br/> |
|<span data-ttu-id="b713a-213">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b713a-213">**Syntax**</span></span> <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|<span data-ttu-id="b713a-214">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="b713a-214">**Parameters**</span></span> <br/> | <span data-ttu-id="b713a-215">_piCallback_ &ndash; Uma referência à interface **IQuickFilingDialogCallback** que será instariada depois que a caixa de diálogo fechar.</span><span class="sxs-lookup"><span data-stu-id="b713a-215">_piCallback_ &ndash; A reference to the **IQuickFilingDialogCallback** interface that will be instantiated once the dialog box closes.</span></span>  <br/> |
   
<span data-ttu-id="b713a-216">O exemplo a seguir usa o **método Run** para exibir a caixa de diálogo Arquivamento Rápido de um novo thread.</span><span class="sxs-lookup"><span data-stu-id="b713a-216">The following example uses the **Run** method to display the Quick Filing dialog box from a new thread.</span></span> 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

<span data-ttu-id="b713a-217">**TreeCollapsedState**</span><span class="sxs-lookup"><span data-stu-id="b713a-217">**TreeCollapsedState**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b713a-218">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-218">**Description**</span></span> <br/> |<span data-ttu-id="b713a-219">Indica se a árvore hierárquica deve ser expandida ou recolhido.</span><span class="sxs-lookup"><span data-stu-id="b713a-219">Indicates whether the hierarchy tree should be expanded or collapsed.</span></span>  <br/> |
|<span data-ttu-id="b713a-220">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b713a-220">**Syntax**</span></span> <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|<span data-ttu-id="b713a-221">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="b713a-221">**Parameters**</span></span> <br/> | <span data-ttu-id="b713a-222">_tcs_ - Especifica se a árvore está expandida ou recolhido.</span><span class="sxs-lookup"><span data-stu-id="b713a-222">_tcs_ - Specifies whether the tree is expanded or collapsed.</span></span>  <br/> |
   
<span data-ttu-id="b713a-223">**NotebookFilterOut**</span><span class="sxs-lookup"><span data-stu-id="b713a-223">**NotebookFilterOut**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b713a-224">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-224">**Description**</span></span> <br/> |<span data-ttu-id="b713a-225">Filtra a lista de blocos de anotações mostrados por tipo.</span><span class="sxs-lookup"><span data-stu-id="b713a-225">Filters the list of notebooks shown by type.</span></span>  <br/> |
|<span data-ttu-id="b713a-226">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b713a-226">**Syntax**</span></span> <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|<span data-ttu-id="b713a-227">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="b713a-227">**Parameters**</span></span> <br/> | <span data-ttu-id="b713a-228">_nfo_ - Especifica o conjunto de blocos de anotações que devem ser filtrados para fora da lista</span><span class="sxs-lookup"><span data-stu-id="b713a-228">_nfo_ - Specifies the set of notebooks that are to be filtered out of the list</span></span>  <br/> |
   
<span data-ttu-id="b713a-229">**ShowCreateNewNotebook**</span><span class="sxs-lookup"><span data-stu-id="b713a-229">**ShowCreateNewNotebook**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b713a-230">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-230">**Description**</span></span> <br/> |<span data-ttu-id="b713a-231">Exibe a opção criar novo bloco de anotações na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-231">Displays the create new notebook option in the dialog.</span></span>  <br/> |
|<span data-ttu-id="b713a-232">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b713a-232">**Syntax**</span></span> <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|<span data-ttu-id="b713a-233">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="b713a-233">**Parameters**</span></span> <br/> |<span data-ttu-id="b713a-234">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b713a-234">None</span></span>  <br/> |
   
<span data-ttu-id="b713a-235">**AddInitialEditor**</span><span class="sxs-lookup"><span data-stu-id="b713a-235">**AddInitialEditor**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b713a-236">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-236">**Description**</span></span> <br/> |<span data-ttu-id="b713a-237">Adiciona um usuário como editor inicial a um bloco de anotações na caixa de diálogo Arquivamento Rápido.</span><span class="sxs-lookup"><span data-stu-id="b713a-237">Adds a user as an initial editor to a notebook in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="b713a-238">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b713a-238">**Syntax**</span></span> <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|<span data-ttu-id="b713a-239">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="b713a-239">**Parameters**</span></span> <br/> | <span data-ttu-id="b713a-240">_initialEditor_ - O endereço de email do usuário que você deseja adicionar como editor ao bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="b713a-240">_initialEditor_ - The email address of the user you wish to add as an editor to the notebook.</span></span> <span data-ttu-id="b713a-241">Quando o bloco de anotações é criado por meio da caixa de diálogo Arquivamento Rápido, ele é compartilhado automaticamente com todos os Editores Iniciais.</span><span class="sxs-lookup"><span data-stu-id="b713a-241">When the notebook is created via the Quick Filing dialog box, it is automatically shared with all Initial Editors.</span></span>  <br/> |
   
<span data-ttu-id="b713a-242">**ClearInitialEditors**</span><span class="sxs-lookup"><span data-stu-id="b713a-242">**ClearInitialEditors**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b713a-243">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-243">**Description**</span></span> <br/> |<span data-ttu-id="b713a-244">Remove todos os editores iniciais da caixa de diálogo Arquivamento Rápido.</span><span class="sxs-lookup"><span data-stu-id="b713a-244">Removes all initial editors from the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="b713a-245">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b713a-245">**Syntax**</span></span> <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|<span data-ttu-id="b713a-246">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="b713a-246">**Parameters**</span></span> <br/> |<span data-ttu-id="b713a-247">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b713a-247">None</span></span>  <br/> |
   
<span data-ttu-id="b713a-248">**ShowSharingHyperlink**</span><span class="sxs-lookup"><span data-stu-id="b713a-248">**ShowSharingHyperlink**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b713a-249">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-249">**Description**</span></span> <br/> |<span data-ttu-id="b713a-250">Exibe o Hiperlink do Tópico da Ajuda de Compartilhamento na caixa de diálogo Arquivamento Rápido.</span><span class="sxs-lookup"><span data-stu-id="b713a-250">Displays the Sharing Help Topic Hyperlink in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="b713a-251">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b713a-251">**Syntax**</span></span> <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|<span data-ttu-id="b713a-252">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="b713a-252">**Parameters**</span></span> <br/> |<span data-ttu-id="b713a-253">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b713a-253">None</span></span>  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a><span data-ttu-id="b713a-254">Interface IQuickFilingDialogCallback</span><span class="sxs-lookup"><span data-stu-id="b713a-254">IQuickFilingDialogCallback interface</span></span>
<span data-ttu-id="b713a-255"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="b713a-255"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="b713a-256">Essa interface permite que o usuário acesse as propriedades da caixa de diálogo após o fechamento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-256">This interface allows the user to access the dialog box properties after the dialog box closes.</span></span> <span data-ttu-id="b713a-257">Depois que a caixa de diálogo é fechado, o OneNote 2013 chama o método **IQuickFilingDialogCallback.OnDialogClose** nesta interface.</span><span class="sxs-lookup"><span data-stu-id="b713a-257">Once the dialog box closes, OneNote 2013 calls the **IQuickFilingDialogCallback.OnDialogClose** method in this interface.</span></span> 
  
<span data-ttu-id="b713a-258">Uma classe que herda essa interface deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="b713a-258">A class that inherits this interface has to be defined.</span></span>
  
### <a name="methods"></a><span data-ttu-id="b713a-259">Methods</span><span class="sxs-lookup"><span data-stu-id="b713a-259">Methods</span></span>

<span data-ttu-id="b713a-260">A seção a seguir descreve os métodos associados às interfaces detalhadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b713a-260">The following section describes the methods associated with the interfaces detailed previously.</span></span>
  
<span data-ttu-id="b713a-261">**OnDialogClosed**</span><span class="sxs-lookup"><span data-stu-id="b713a-261">**OnDialogClosed**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b713a-262">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b713a-262">**Description**</span></span> <br/> |<span data-ttu-id="b713a-263">Permite que os usuários adicionem funcionalidade para capturar e usar a seleção do usuário na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b713a-263">Enables users to add functionality to capture and use the user selection from the dialog box.</span></span> <span data-ttu-id="b713a-264">Esse método é chamado depois que a caixa de diálogo Arquivamento Rápido é fechada.</span><span class="sxs-lookup"><span data-stu-id="b713a-264">This method is called after the Quick Filing dialog box is closed.</span></span> <span data-ttu-id="b713a-265">Esse método é uma função que as interfaces **IQuickFilingDialogCallback** têm que definir.</span><span class="sxs-lookup"><span data-stu-id="b713a-265">This method is a function that **IQuickFilingDialogCallback** interfaces have to define.</span></span>  <br/> |
|<span data-ttu-id="b713a-266">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b713a-266">**Syntax**</span></span> <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|<span data-ttu-id="b713a-267">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="b713a-267">**Parameters**</span></span> <br/> | <span data-ttu-id="b713a-268">_dialog_ &ndash; O **objeto IQuickFilingDialog** que chamou o **método OnDialogClose.**</span><span class="sxs-lookup"><span data-stu-id="b713a-268">_dialog_ &ndash; The **IQuickFilingDialog** object that called the **OnDialogClose** method.</span></span>  <br/> |
   
<span data-ttu-id="b713a-269">O exemplo a seguir é uma interface **IQuickFilingDialogCallback de** exemplo.</span><span class="sxs-lookup"><span data-stu-id="b713a-269">The following example is a sample **IQuickFilingDialogCallback** interface.</span></span> <span data-ttu-id="b713a-270">O **método OnDialogClose** imprime a seleção do usuário da caixa de diálogo Arquivamento Rápido no console.</span><span class="sxs-lookup"><span data-stu-id="b713a-270">The **OnDialogClose** method prints the user's selection from the Quick Filing dialog box to the console.</span></span> 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a><span data-ttu-id="b713a-271">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b713a-271">Example</span></span>
<span data-ttu-id="b713a-272"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="b713a-272"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="b713a-273">O exemplo de código a seguir abre uma caixa de diálogo arquivamento rápido que tem um título personalizado, descrição, lista de resultados recentes, profundidade da árvore, caixa de seleção e botões.</span><span class="sxs-lookup"><span data-stu-id="b713a-273">The following code example opens a Quick Filing dialog box that has a customized title, description, recent result list, tree depth, check box, and buttons.</span></span> <span data-ttu-id="b713a-274">O item selecionado do usuário, o botão pressionado e o estado da caixa de seleção serão exibidos em uma janela do console quando a caixa de diálogo for fechada.</span><span class="sxs-lookup"><span data-stu-id="b713a-274">The user's selected item, pressed button, and check-box state will be displayed in a console window when the dialog box is closed.</span></span> <span data-ttu-id="b713a-275">Para ver o botão de página habilitado, o usuário terá que pesquisar uma página e selecioná-la, porque a profundidade da árvore é definida para seções.</span><span class="sxs-lookup"><span data-stu-id="b713a-275">To see the page button enabled, the user will have to search for a page and select it, because the tree depth is set down to sections.</span></span> <span data-ttu-id="b713a-276">A caixa de diálogo não é um filho de nenhuma janela.</span><span class="sxs-lookup"><span data-stu-id="b713a-276">The dialog box is not a child of any window.</span></span>
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a><span data-ttu-id="b713a-277">Confira também</span><span class="sxs-lookup"><span data-stu-id="b713a-277">See also</span></span>

- [<span data-ttu-id="b713a-278">Referência do desenvolvedor do OneNote</span><span class="sxs-lookup"><span data-stu-id="b713a-278">OneNote developer reference</span></span>](onenote-developer-reference.md)

