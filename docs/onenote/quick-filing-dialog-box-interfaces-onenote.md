---
title: Interfaces de caixa de diálogo de arquivamento rápidos (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: Este tópico descreve as interfaces que você pode usar para personalizar programaticamente a caixa de diálogo arquivamento rápido no OneNote 2013.
ms.openlocfilehash: d2647ed4d7b9f4487c033260eba8df1e4281c6ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765784"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a><span data-ttu-id="3c151-103">Interfaces de caixa de diálogo de arquivamento rápidos (OneNote)</span><span class="sxs-lookup"><span data-stu-id="3c151-103">Quick Filing dialog box interfaces (OneNote)</span></span>

<span data-ttu-id="3c151-104">Este tópico descreve as interfaces que você pode usar para personalizar programaticamente a caixa de diálogo arquivamento rápido no OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="3c151-104">This topic describes the interfaces that you can use to programmatically customize the Quick Filing dialog box in OneNote 2013.</span></span>
  
## <a name="quick-filing-dialog-box"></a><span data-ttu-id="3c151-105">Caixa de diálogo arquivamento rápida</span><span class="sxs-lookup"><span data-stu-id="3c151-105">Quick Filing dialog box</span></span>

<span data-ttu-id="3c151-106">A caixa de diálogo arquivamento rápido no OneNote 2013 é uma caixa de diálogo personalizável que permite que os usuários selecionem um local dentro da estrutura de hierarquia do OneNote.</span><span class="sxs-lookup"><span data-stu-id="3c151-106">The Quick Filing dialog box in OneNote 2013 is a customizable dialog box that allows users to select a location within the OneNote hierarchy structure.</span></span> <span data-ttu-id="3c151-107">Selecionáveis locais incluem os blocos de anotações, grupos de seção, seções, páginas e subpáginas.</span><span class="sxs-lookup"><span data-stu-id="3c151-107">Selectable locations include notebooks, section groups, sections, pages, and subpages.</span></span> <span data-ttu-id="3c151-108">A caixa de diálogo é usada dentro do aplicativo do OneNote e por aplicativos externos por meio da API do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="3c151-108">The dialog box is used both within the OneNote application and by external applications through the OneNote 2013 API.</span></span> <span data-ttu-id="3c151-109">A Figura 1 mostra a caixa de diálogo Preenchimento rápido em seu estado padrão.</span><span class="sxs-lookup"><span data-stu-id="3c151-109">Figure 1 shows the Quick Filing dialog box in its default state.</span></span>
  
<span data-ttu-id="3c151-110">**Figura 1. Caixa de diálogo arquivamento rápida sem personalizações**</span><span class="sxs-lookup"><span data-stu-id="3c151-110">**Figure 1. Quick Filing dialog box without customizations**</span></span>

<span data-ttu-id="3c151-111">![Caixa de diálogo Preenchimento rápido sem personalizações] (media/ON15Con_quick_filing_dialog.jpg "Caixa de diálogo Preenchimento rápido sem personalizações")</span><span class="sxs-lookup"><span data-stu-id="3c151-111">![Quick Filing dialog box without customizations](media/ON15Con_quick_filing_dialog.jpg "Quick Filing dialog box without customizations")</span></span>
  
<span data-ttu-id="3c151-112">Dentro da caixa de diálogo, os usuários podem navegar na hierarquia de todos os blocos de anotações para procurar locais específicos ou pesquise a estrutura de árvore do OneNote digitando na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="3c151-112">Within the dialog box, users can navigate the All Notebooks hierarchy to look for specific locations or search the OneNote tree structure by typing into the text box.</span></span> <span data-ttu-id="3c151-113">Aspectos da caixa de diálogo que podem ser personalizados incluem o título, descrição, recentes lista de resultados, caixa de seleção de texto e estado, profundidade de árvore, botões e tipos de localização selecionável.</span><span class="sxs-lookup"><span data-stu-id="3c151-113">Aspects of the dialog box that can be customized include the title, description, recent results list, check box text and state, tree depth, buttons, and selectable location types.</span></span>

<span data-ttu-id="3c151-114">Você pode acessar a funcionalidade de caixa de diálogo Preenchimento rápido por meio de duas interfaces do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="3c151-114">You can access the Quick Filing dialog box functionality through two OneNote 2013 interfaces.</span></span> <span data-ttu-id="3c151-115">A interface **IQuickFilingDialog** permite que os usuários criar uma instância, configurar e executar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3c151-115">The **IQuickFilingDialog** interface allows users to instantiate, set up, and run the dialog box.</span></span> <span data-ttu-id="3c151-116">A interface **IQuickFilingDialogCallback** é chamada depois que a caixa de diálogo é fechada.</span><span class="sxs-lookup"><span data-stu-id="3c151-116">The **IQuickFilingDialogCallback** interface is called after the dialog box is closed.</span></span> <span data-ttu-id="3c151-117">A caixa de diálogo é executada no processo do OneNote, portanto um mecanismo é necessário para manter um segmento da caixa de diálogo em execução e, em seguida, para capturar a seleção do usuário e o estado da caixa de diálogo quando ele for fechado.</span><span class="sxs-lookup"><span data-stu-id="3c151-117">The dialog box is run in the OneNote process, so a mechanism is needed to keep the dialog box's thread running and then to capture the user's selection and the state of the dialog box when it is closed.</span></span> 
  
## <a name="iquickfilingdialog-interface"></a><span data-ttu-id="3c151-118">Interface de IQuickFilingDialog</span><span class="sxs-lookup"><span data-stu-id="3c151-118">IQuickFilingDialog interface</span></span>
<span data-ttu-id="3c151-119"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="3c151-119"></span></span>

<span data-ttu-id="3c151-120">Essa interface permite ao usuário personalizar e executar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3c151-120">This interface allows the user to customize and run the dialog box.</span></span> <span data-ttu-id="3c151-121">O usuário pode instanciar uma caixa de diálogo por meio da classe de **aplicativo** usando o método **Application.QuickFilingDialog** .</span><span class="sxs-lookup"><span data-stu-id="3c151-121">The user can instantiate a dialog box through the **Application** class by using the **Application.QuickFilingDialog** method.</span></span> <span data-ttu-id="3c151-122">O método retorna uma instância da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3c151-122">The method returns an instance of the dialog box.</span></span> <span data-ttu-id="3c151-123">Depois que as propriedades da caixa de diálogo estiverem definidas, o método **IQuickFilingDialog.Run** é usado para a caixa de diálogo Executar.</span><span class="sxs-lookup"><span data-stu-id="3c151-123">Once the properties of the dialog box are set, the **IQuickFilingDialog.Run** method is used to run the dialog box.</span></span> <span data-ttu-id="3c151-124">Esse método executa a caixa de diálogo em um novo segmento.</span><span class="sxs-lookup"><span data-stu-id="3c151-124">This method runs the dialog box on a new thread.</span></span> 
  
<span data-ttu-id="3c151-125">**Properties**</span><span class="sxs-lookup"><span data-stu-id="3c151-125">**Properties**</span></span>

|<span data-ttu-id="3c151-126">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3c151-126">**Name**</span></span>|<span data-ttu-id="3c151-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="3c151-127">**Type**</span></span>|<span data-ttu-id="3c151-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3c151-129">**Title**</span><span class="sxs-lookup"><span data-stu-id="3c151-129">**Title**</span></span> <br/> |<span data-ttu-id="3c151-130">string</span><span class="sxs-lookup"><span data-stu-id="3c151-130">string</span></span>  <br/> |<span data-ttu-id="3c151-131">Obtém ou define o texto do título aparece na barra de título da janela de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3c151-131">Gets or sets the title text that appears in the title bar of the dialog box window.</span></span>  <br/> |
|<span data-ttu-id="3c151-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-132">**Description**</span></span> <br/> |<span data-ttu-id="3c151-133">string</span><span class="sxs-lookup"><span data-stu-id="3c151-133">string</span></span>  <br/> |<span data-ttu-id="3c151-134">Obtém ou define a descrição de texto para instruir o usuário sobre o que selecionar.</span><span class="sxs-lookup"><span data-stu-id="3c151-134">Gets or sets the text description to instruct the user about what to select.</span></span> <span data-ttu-id="3c151-135">Esse valor pode ser texto com várias linhas.</span><span class="sxs-lookup"><span data-stu-id="3c151-135">This value can be multiple-line text.</span></span>  <br/> |
|<span data-ttu-id="3c151-136">**CheckboxText**</span><span class="sxs-lookup"><span data-stu-id="3c151-136">**CheckboxText**</span></span> <br/> |<span data-ttu-id="3c151-137">string</span><span class="sxs-lookup"><span data-stu-id="3c151-137">string</span></span>  <br/> |<span data-ttu-id="3c151-138">Obtém ou define o texto que segue a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="3c151-138">Gets or sets the text that follows the check box.</span></span> <span data-ttu-id="3c151-139">Se esse valor é definido como uma cadeia de caracteres não-vazias, uma caixa de seleção é exibida na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3c151-139">If this value is set to a non-empty string, a check box appears in the dialog box.</span></span> <span data-ttu-id="3c151-140">Se o valor for uma sequência vazia, nenhuma caixa de seleção é exibida.</span><span class="sxs-lookup"><span data-stu-id="3c151-140">If the value is an empty string, no check box appears.</span></span>  <br/> |
|<span data-ttu-id="3c151-141">**CheckboxState**</span><span class="sxs-lookup"><span data-stu-id="3c151-141">**CheckboxState**</span></span> <br/> |<span data-ttu-id="3c151-142">bool</span><span class="sxs-lookup"><span data-stu-id="3c151-142">bool</span></span>  <br/> |<span data-ttu-id="3c151-143">Obtém ou define o estado da caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="3c151-143">Gets or sets the state of the check box.</span></span> <span data-ttu-id="3c151-144">Se o valor for definido como **false**, a caixa de seleção está desmarcada, quando a caixa de diálogo é iniciada.</span><span class="sxs-lookup"><span data-stu-id="3c151-144">If value is set to **false**, the check box is cleared when the dialog box is started.</span></span> <span data-ttu-id="3c151-145">Se o valor for definido como **true**, a caixa de seleção é selecionada quando a caixa de diálogo é iniciada desde que o **CheckboxText** é uma cadeia de caracteres não vazias.</span><span class="sxs-lookup"><span data-stu-id="3c151-145">If the value is set to **true**, the check box is selected when the dialog box is started as long as **CheckboxText** is a non-empty string.</span></span>  <br/> |
|<span data-ttu-id="3c151-146">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="3c151-146">**WindowHandle**</span></span> <br/> |<span data-ttu-id="3c151-147">ULong</span><span class="sxs-lookup"><span data-stu-id="3c151-147">ulong</span></span>  <br/> |<span data-ttu-id="3c151-148">Obtém a identificação da alça da janela de caixa de diálogo Preenchimento rápido.</span><span class="sxs-lookup"><span data-stu-id="3c151-148">Gets the handle ID of the Quick Filing dialog box window.</span></span>  <br/> |
|<span data-ttu-id="3c151-149">**TreeDepth**</span><span class="sxs-lookup"><span data-stu-id="3c151-149">**TreeDepth**</span></span> <br/> |<span data-ttu-id="3c151-150">**HierarchyElement**</span><span class="sxs-lookup"><span data-stu-id="3c151-150">**HierarchyElement**</span></span> <br/> |<span data-ttu-id="3c151-151">Obtém ou define a profundidade, a árvore do OneNote deve ser exibida na seção de todos os blocos de anotações.</span><span class="sxs-lookup"><span data-stu-id="3c151-151">Gets or sets how deep the OneNote tree should be displayed in the All Notebooks section.</span></span> <span data-ttu-id="3c151-152">Por padrão, a árvore é exibida até as seções.</span><span class="sxs-lookup"><span data-stu-id="3c151-152">By default, the tree is displayed up to the sections.</span></span> <span data-ttu-id="3c151-153">Essa propriedade não afeta a que tipo de elementos que pode ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="3c151-153">This property does not affect what type of elements can be selected.</span></span>  <br/> <span data-ttu-id="3c151-154">Se **TreeDepth** estiver definida como um elemento inferior na hierarquia do OneNote, que pode ser selecionado por qualquer um dos botões, a profundidade de árvore exibida será o menor elemento selecionável possível.</span><span class="sxs-lookup"><span data-stu-id="3c151-154">If **TreeDepth** is set to an element lower in the OneNote hierarchy than can be selected by any of the buttons, the displayed tree depth will be the lowest possible selectable element.</span></span> <span data-ttu-id="3c151-155">Ou seja, se profundidade da árvore está definida para exibir para baixo até páginas, mas o elemento selecionável mais baixa é uma seção, a árvore é exibida para baixo até seções.</span><span class="sxs-lookup"><span data-stu-id="3c151-155">That is, if tree depth is set to display down to pages, but the lowest selectable element is a section, the tree is displayed down to sections.</span></span>  <br/> |
|<span data-ttu-id="3c151-156">**ParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="3c151-156">**ParentWindowHandle**</span></span> <br/> |<span data-ttu-id="3c151-157">ULong</span><span class="sxs-lookup"><span data-stu-id="3c151-157">ulong</span></span>  <br/> |<span data-ttu-id="3c151-158">Obtém ou define a ID do identificador da janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3c151-158">Gets or sets the handle ID of the parent window of the dialog box.</span></span> <span data-ttu-id="3c151-159">Se essa propriedade estiver definida, a caixa de diálogo Preenchimento rápido será restrita para a janela pai atribuído quando a caixa de diálogo será aberta.</span><span class="sxs-lookup"><span data-stu-id="3c151-159">If this property is set, the Quick Filing dialog box will be modal to the assigned parent window when the dialog box opens.</span></span> <span data-ttu-id="3c151-160">Ou seja, um usuário não será capaz de acessar a janela pai até que a caixa de diálogo Preenchimento rápido seja fechada.</span><span class="sxs-lookup"><span data-stu-id="3c151-160">That is, a user will not be able to access the parent window until the Quick Filing dialog box is closed.</span></span>  <br/> |
|<span data-ttu-id="3c151-161">**Position**</span><span class="sxs-lookup"><span data-stu-id="3c151-161">**Position**</span></span> <br/> |<span data-ttu-id="3c151-162">tagPOINT</span><span class="sxs-lookup"><span data-stu-id="3c151-162">tagPOINT</span></span>  <br/> |<span data-ttu-id="3c151-163">Obtém ou define a posição da janela em relação à tela.</span><span class="sxs-lookup"><span data-stu-id="3c151-163">Gets or sets the position of the window in relation to the screen.</span></span> <span data-ttu-id="3c151-164">Por padrão, a caixa de diálogo aparece no meio da janela pai ou a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3c151-164">By default, the dialog box appears in the middle of the parent window or the desktop.</span></span>  <br/> |
|<span data-ttu-id="3c151-165">**SelectedItem**</span><span class="sxs-lookup"><span data-stu-id="3c151-165">**SelectedItem**</span></span> <br/> |<span data-ttu-id="3c151-166">string</span><span class="sxs-lookup"><span data-stu-id="3c151-166">string</span></span>  <br/> |<span data-ttu-id="3c151-167">Obtém a ID de objeto do OneNote local selecionado pelo usuário quando a caixa de diálogo é fechada.</span><span class="sxs-lookup"><span data-stu-id="3c151-167">Gets the object ID of the OneNote location selected by the user when the dialog box is closed.</span></span> <span data-ttu-id="3c151-168">Se o usuário clicar no botão **Cancelar** , o objeto é definido como null.</span><span class="sxs-lookup"><span data-stu-id="3c151-168">If the user clicks the **Cancel** button, the object is set to null.</span></span>  <br/> |
|<span data-ttu-id="3c151-169">**PressedButton**</span><span class="sxs-lookup"><span data-stu-id="3c151-169">**PressedButton**</span></span> <br/> |<span data-ttu-id="3c151-170">ULong</span><span class="sxs-lookup"><span data-stu-id="3c151-170">ulong</span></span>  <br/> |<span data-ttu-id="3c151-171">Obtém a qual botão foi clicado quando a caixa de diálogo foi fechada.</span><span class="sxs-lookup"><span data-stu-id="3c151-171">Gets which button was clicked when the dialog box was closed.</span></span> <span data-ttu-id="3c151-172">Se o botão **Cancelar** foi clicado, essa propriedade retorna um valor de -1.</span><span class="sxs-lookup"><span data-stu-id="3c151-172">If the **Cancel** button was clicked, this property returns a value of -1.</span></span> <span data-ttu-id="3c151-173">Todos os outros botões recebem valores inteiros de 0, incrementada em 1 para cada botão adicionado à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3c151-173">All other buttons are assigned integer values from 0, incremented by 1 for each button added to the dialog box.</span></span> <span data-ttu-id="3c151-174">O valor de inteiro do botão de **Okey** padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="3c151-174">The integer value of the default **OK** button is 0.</span></span>  <br/> |
   
### <a name="methods"></a><span data-ttu-id="3c151-175">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c151-175">Methods</span></span>

<span data-ttu-id="3c151-176">**SetRecentResults**</span><span class="sxs-lookup"><span data-stu-id="3c151-176">**SetRecentResults**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c151-177">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-177">**Description**</span></span> <br/> |<span data-ttu-id="3c151-178">Define a lista de resultados que recentes será exibida na caixa de diálogo Preenchimento rápido e indica se é necessário incluir alguns locais de arquivamento especiais na lista.</span><span class="sxs-lookup"><span data-stu-id="3c151-178">Sets what recent result list will be displayed in the Quick Filing dialog box, and indicates whether to include some special filing locations in the list.</span></span> <span data-ttu-id="3c151-179">Os usuários podem selecionar a lista de resultados recentes provenientes da enumeração [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) .</span><span class="sxs-lookup"><span data-stu-id="3c151-179">Users can select a recent result list from the [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) enumeration.</span></span> <span data-ttu-id="3c151-180">Os usuários também podem optar por adicionar as seguintes opções na lista: seção atual, a página atual ou anotações não arquivadas.</span><span class="sxs-lookup"><span data-stu-id="3c151-180">Users can also choose to add the following options to the list: Current Section, Current Page, or Unfiled Notes.</span></span> <span data-ttu-id="3c151-181">Se **RecentResultType.rrtNone** for selecionado, nenhuma lista de resultados recentes é mostrada.</span><span class="sxs-lookup"><span data-stu-id="3c151-181">If **RecentResultType.rrtNone** is selected, no recent result list is shown.</span></span>  <br/> |
|<span data-ttu-id="3c151-182">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="3c151-182">**Syntax**</span></span> <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|<span data-ttu-id="3c151-183">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="3c151-183">**Parameters**</span></span> <br/> | <span data-ttu-id="3c151-184">_recentResults_ &ndash; Um objeto do tipo **RecentResultType** que indica qual recentes lista de resultados, se houver, deve aparecer.</span><span class="sxs-lookup"><span data-stu-id="3c151-184">_recentResults_ &ndash; An object of type **RecentResultType** that indicates which recent result list, if any, should appear.</span></span> <span data-ttu-id="3c151-185">Se **rrtNone** for selecionado, nenhuma lista de resultados recentes aparece na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3c151-185">If **rrtNone** is selected, no recent result list appears in the dialog box.</span></span><br/><br/>  <span data-ttu-id="3c151-186">_fShowCurrentSection_ &ndash; Um valor Boolean que indica se a seção atual deve ser incluída na lista de resultados recentes.</span><span class="sxs-lookup"><span data-stu-id="3c151-186">_fShowCurrentSection_ &ndash; A Boolean value that indicates whether the current section should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="3c151-187">_fShowCurrentPage_ &ndash; Um valor Boolean que indica se a página atual deve ser incluída na lista de resultados recentes.</span><span class="sxs-lookup"><span data-stu-id="3c151-187">_fShowCurrentPage_ &ndash; A Boolean value that indicates whether the current page should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="3c151-188">_fShowUnfiledNotes_ &ndash; Um valor Boolean que indica se a seção anotações não arquivadas deve ser incluída na lista de resultados recentes.</span><span class="sxs-lookup"><span data-stu-id="3c151-188">_fShowUnfiledNotes_ &ndash; A Boolean value that indicates whether the Unfiled Notes section should be included in the recent result list.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3c151-189">Se um local de arquivamento especiais não pode ser selecionado usando qualquer um dos botões na caixa de diálogo, ele não será mostrado na lista.</span><span class="sxs-lookup"><span data-stu-id="3c151-189">If a special filing location cannot be selected by using any of the buttons in the dialog box, it is not shown in the list.</span></span> <span data-ttu-id="3c151-190">Se nenhum item selecionável na lista de resultados recentes for localizado, nenhuma recentes lista de resultados será exibida.</span><span class="sxs-lookup"><span data-stu-id="3c151-190">If no selectable item in the recent results list is found, no recent result list is displayed.</span></span> 
  
<span data-ttu-id="3c151-191">O exemplo a seguir usa o método **SetRecentResults** para exibir a seção atual, a página atual e a seção anotações não arquivadas na lista de resultados recentes.</span><span class="sxs-lookup"><span data-stu-id="3c151-191">The following example uses the **SetRecentResults** method to display the current section, current page, and the Unfiled Notes section in the recent result list.</span></span> 
  
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

<span data-ttu-id="3c151-192">**AddButton**</span><span class="sxs-lookup"><span data-stu-id="3c151-192">**AddButton**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c151-193">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-193">**Description**</span></span> <br/> |<span data-ttu-id="3c151-194">Permite aos usuários adicionar e personalizar os botões na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3c151-194">Allows users to add and customize buttons in the dialog box.</span></span> <span data-ttu-id="3c151-195">Os usuários podem especificar o texto sobre os botões e quais elementos da hierarquia do OneNote podem ser selecionados por cada botão.</span><span class="sxs-lookup"><span data-stu-id="3c151-195">Users can specify the text on the buttons and what elements of the OneNote hierarchy can be selected by each button.</span></span>  <br/> |
|<span data-ttu-id="3c151-196">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="3c151-196">**Syntax**</span></span> <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|<span data-ttu-id="3c151-197">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="3c151-197">**Parameters**</span></span> <br/> | <span data-ttu-id="3c151-198">_bstrText_ &ndash; Uma cadeia de caracteres que especifica o texto a ser exibido no botão.</span><span class="sxs-lookup"><span data-stu-id="3c151-198">_bstrText_ &ndash; A string that specifies the text to appear on the button.</span></span> <span data-ttu-id="3c151-199">Para personalizar o botão de **Okey** padrão, passe um valor nulo como **bstrText**.</span><span class="sxs-lookup"><span data-stu-id="3c151-199">To customize the default **OK** button, pass in a null value as **bstrText**.</span></span>  <br/><br/><span data-ttu-id="3c151-200">_allowedElements_ &ndash; **HierarchyElement** que indica quais elementos de hierarquia do OneNote não somente leitura que um usuário tem permissão para selecionar usando o botão.</span><span class="sxs-lookup"><span data-stu-id="3c151-200">_allowedElements_ &ndash; A **HierarchyElement** that indicates what non-read-only OneNote hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="3c151-201">Para selecionar vários itens, o usuário deve passar no operador **ou** para todos os valores equivalentes de uint dos tipos de **HierarchyElement** permitidos como um **HierarchyElement**.</span><span class="sxs-lookup"><span data-stu-id="3c151-201">For selecting multiple items, the user should pass in the **OR** operator for all the uint equivalent values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="3c151-202">_allowedReadOnlyElements_ &ndash; **HierarchyElement** que indica quais elementos de hierarquia de somente leitura do OneNote que um usuário tem permissão para selecionar usando o botão.</span><span class="sxs-lookup"><span data-stu-id="3c151-202">_allowedReadOnlyElements_ &ndash; A **HierarchyElement** that indicates what OneNote read-only hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="3c151-203">Para selecionar vários itens, o usuário deve passar no operador **ou** para todos os valores de equivalentes **uint** dos tipos de **HierarchyElement** permitidos como um **HierarchyElement**.</span><span class="sxs-lookup"><span data-stu-id="3c151-203">For selecting multiple items, the user should pass in the **OR** operator for all the **uint** equivalents values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="3c151-204">_fDefault_ &ndash; Um valor Boolean que especifica se este botão deve ser o botão padrão.</span><span class="sxs-lookup"><span data-stu-id="3c151-204">_fDefault_ &ndash; A Boolean value that specifies whether this button should be the default button.</span></span> <span data-ttu-id="3c151-205">Se vários botões estiverem definidos como padrão, o último botão especificado torna-se o botão padrão.</span><span class="sxs-lookup"><span data-stu-id="3c151-205">If multiple buttons are set as default, the last specified button becomes the default button.</span></span>  <br/> |
   
<span data-ttu-id="3c151-206">O exemplo a seguir adiciona três botões à caixa de diálogo arquivamento rápido.</span><span class="sxs-lookup"><span data-stu-id="3c151-206">The following example adds three buttons to the Quick Filing dialog box.</span></span> <span data-ttu-id="3c151-207">Uma primeira, **todos**, pode ser selecionada por todos os elementos na árvore de hierarquia do OneNote.</span><span class="sxs-lookup"><span data-stu-id="3c151-207">The first one, **All**, can be selected by all elements in the OneNote hierarchy tree.</span></span> <span data-ttu-id="3c151-208">Os outros, **blocos de anotações** e **páginas**, podem ser selecionados somente se seus elementos correspondentes, blocos de anotações e páginas, estão selecionados.</span><span class="sxs-lookup"><span data-stu-id="3c151-208">The others, **Notebooks** and **Pages**, can be selected only if their corresponding elements, Notebooks and Pages, are selected.</span></span>
  
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

<span data-ttu-id="3c151-209">**Run**</span><span class="sxs-lookup"><span data-stu-id="3c151-209">**Run**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c151-210">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-210">**Description**</span></span> <br/> |<span data-ttu-id="3c151-211">Exibe a caixa de diálogo Preenchimento rápido de um novo segmento.</span><span class="sxs-lookup"><span data-stu-id="3c151-211">Displays the Quick Filing dialog box from a new thread.</span></span> <span data-ttu-id="3c151-212">Ele utiliza uma referência para a interface **IQuickFilingDialogCallback** , cujo método **OnDialogClosed** será chamado depois que a caixa de diálogo é fechada.</span><span class="sxs-lookup"><span data-stu-id="3c151-212">It takes a reference to the **IQuickFilingDialogCallback** interface, whose **OnDialogClosed** method will be called once the dialog box closes.</span></span>  <br/> |
|<span data-ttu-id="3c151-213">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="3c151-213">**Syntax**</span></span> <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|<span data-ttu-id="3c151-214">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="3c151-214">**Parameters**</span></span> <br/> | <span data-ttu-id="3c151-215">_piCallback_ &ndash; Uma referência para a interface de **IQuickFilingDialogCallback** que será instanciada depois que a caixa de diálogo é fechada.</span><span class="sxs-lookup"><span data-stu-id="3c151-215">_piCallback_ &ndash; A reference to the **IQuickFilingDialogCallback** interface that will be instantiated once the dialog box closes.</span></span>  <br/> |
   
<span data-ttu-id="3c151-216">O exemplo a seguir usa o método **Run** para exibir a caixa de diálogo Preenchimento rápido de um novo segmento.</span><span class="sxs-lookup"><span data-stu-id="3c151-216">The following example uses the **Run** method to display the Quick Filing dialog box from a new thread.</span></span> 
  
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

<span data-ttu-id="3c151-217">**TreeCollapsedState**</span><span class="sxs-lookup"><span data-stu-id="3c151-217">**TreeCollapsedState**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c151-218">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-218">**Description**</span></span> <br/> |<span data-ttu-id="3c151-219">Indica se a árvore de hierarquia deve ser expandido ou recolhido.</span><span class="sxs-lookup"><span data-stu-id="3c151-219">Indicates whether the hierarchy tree should be expanded or collapsed.</span></span>  <br/> |
|<span data-ttu-id="3c151-220">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="3c151-220">**Syntax**</span></span> <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|<span data-ttu-id="3c151-221">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="3c151-221">**Parameters**</span></span> <br/> | <span data-ttu-id="3c151-222">_tcs_ - Especifica se a árvore é expandida ou recolhida.</span><span class="sxs-lookup"><span data-stu-id="3c151-222">_tcs_ - Specifies whether the tree is expanded or collapsed.</span></span>  <br/> |
   
<span data-ttu-id="3c151-223">**NotebookFilterOut**</span><span class="sxs-lookup"><span data-stu-id="3c151-223">**NotebookFilterOut**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c151-224">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-224">**Description**</span></span> <br/> |<span data-ttu-id="3c151-225">Filtra a lista de blocos de anotações mostrado por tipo.</span><span class="sxs-lookup"><span data-stu-id="3c151-225">Filters the list of notebooks shown by type.</span></span>  <br/> |
|<span data-ttu-id="3c151-226">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="3c151-226">**Syntax**</span></span> <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|<span data-ttu-id="3c151-227">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="3c151-227">**Parameters**</span></span> <br/> | <span data-ttu-id="3c151-228">_nfo_ - Especifica o conjunto de blocos de anotações que devem ser filtrados para fora da lista</span><span class="sxs-lookup"><span data-stu-id="3c151-228">_nfo_ - Specifies the set of notebooks that are to be filtered out of the list</span></span>  <br/> |
   
<span data-ttu-id="3c151-229">**ShowCreateNewNotebook**</span><span class="sxs-lookup"><span data-stu-id="3c151-229">**ShowCreateNewNotebook**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c151-230">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-230">**Description**</span></span> <br/> |<span data-ttu-id="3c151-231">Exibe a opção de criar novo bloco de anotações na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3c151-231">Displays the create new notebook option in the dialog.</span></span>  <br/> |
|<span data-ttu-id="3c151-232">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="3c151-232">**Syntax**</span></span> <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|<span data-ttu-id="3c151-233">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="3c151-233">**Parameters**</span></span> <br/> |<span data-ttu-id="3c151-234">None</span><span class="sxs-lookup"><span data-stu-id="3c151-234">None</span></span>  <br/> |
   
<span data-ttu-id="3c151-235">**AddInitialEditor**</span><span class="sxs-lookup"><span data-stu-id="3c151-235">**AddInitialEditor**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c151-236">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-236">**Description**</span></span> <br/> |<span data-ttu-id="3c151-237">Adiciona um usuário como um editor inicial a um bloco de anotações na caixa de diálogo arquivamento rápido.</span><span class="sxs-lookup"><span data-stu-id="3c151-237">Adds a user as an initial editor to a notebook in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="3c151-238">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="3c151-238">**Syntax**</span></span> <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|<span data-ttu-id="3c151-239">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="3c151-239">**Parameters**</span></span> <br/> | <span data-ttu-id="3c151-240">_initialEditor_ - o endereço de email do usuário que deseja adicionar como um editor como o bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="3c151-240">_initialEditor_ - The email address of the user you wish to add as an editor to the notebook.</span></span> <span data-ttu-id="3c151-241">Quando o bloco de anotações é criado por meio da caixa de diálogo Preenchimento rápido, ele é automaticamente compartilhado com todos os editores inicial.</span><span class="sxs-lookup"><span data-stu-id="3c151-241">When the notebook is created via the Quick Filing dialog box, it is automatically shared with all Initial Editors.</span></span>  <br/> |
   
<span data-ttu-id="3c151-242">**ClearInitialEditors**</span><span class="sxs-lookup"><span data-stu-id="3c151-242">**ClearInitialEditors**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c151-243">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-243">**Description**</span></span> <br/> |<span data-ttu-id="3c151-244">Remove todos os editores iniciais da caixa de diálogo arquivamento rápido.</span><span class="sxs-lookup"><span data-stu-id="3c151-244">Removes all initial editors from the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="3c151-245">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="3c151-245">**Syntax**</span></span> <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|<span data-ttu-id="3c151-246">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="3c151-246">**Parameters**</span></span> <br/> |<span data-ttu-id="3c151-247">None</span><span class="sxs-lookup"><span data-stu-id="3c151-247">None</span></span>  <br/> |
   
<span data-ttu-id="3c151-248">**ShowSharingHyperlink**</span><span class="sxs-lookup"><span data-stu-id="3c151-248">**ShowSharingHyperlink**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c151-249">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-249">**Description**</span></span> <br/> |<span data-ttu-id="3c151-250">Exibe o hiperlink de tópico da Ajuda do compartilhamento na caixa de diálogo arquivamento rápido.</span><span class="sxs-lookup"><span data-stu-id="3c151-250">Displays the Sharing Help Topic Hyperlink in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="3c151-251">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="3c151-251">**Syntax**</span></span> <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|<span data-ttu-id="3c151-252">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="3c151-252">**Parameters**</span></span> <br/> |<span data-ttu-id="3c151-253">None</span><span class="sxs-lookup"><span data-stu-id="3c151-253">None</span></span>  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a><span data-ttu-id="3c151-254">Interface de IQuickFilingDialogCallback</span><span class="sxs-lookup"><span data-stu-id="3c151-254">IQuickFilingDialogCallback interface</span></span>
<span data-ttu-id="3c151-255"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="3c151-255"></span></span>

<span data-ttu-id="3c151-256">Essa interface permite ao usuário acessar as propriedades de caixa de diálogo depois que a caixa de diálogo é fechada.</span><span class="sxs-lookup"><span data-stu-id="3c151-256">This interface allows the user to access the dialog box properties after the dialog box closes.</span></span> <span data-ttu-id="3c151-257">Depois que a caixa de diálogo é fechada, o OneNote 2013 chama o método **IQuickFilingDialogCallback.OnDialogClose** nesta interface.</span><span class="sxs-lookup"><span data-stu-id="3c151-257">Once the dialog box closes, OneNote 2013 calls the **IQuickFilingDialogCallback.OnDialogClose** method in this interface.</span></span> 
  
<span data-ttu-id="3c151-258">Uma classe que herda essa interface deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="3c151-258">A class that inherits this interface has to be defined.</span></span>
  
### <a name="methods"></a><span data-ttu-id="3c151-259">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c151-259">Methods</span></span>

<span data-ttu-id="3c151-260">A seção a seguir descreve os métodos associados com as interfaces detalhadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3c151-260">The following section describes the methods associated with the interfaces detailed previously.</span></span>
  
<span data-ttu-id="3c151-261">**OnDialogClosed**</span><span class="sxs-lookup"><span data-stu-id="3c151-261">**OnDialogClosed**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c151-262">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3c151-262">**Description**</span></span> <br/> |<span data-ttu-id="3c151-263">Permite que os usuários adicionam funcionalidade para capturar e usar a seleção de usuário da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3c151-263">Enables users to add functionality to capture and use the user selection from the dialog box.</span></span> <span data-ttu-id="3c151-264">Este método é chamado depois que a caixa de diálogo Preenchimento rápido é fechada.</span><span class="sxs-lookup"><span data-stu-id="3c151-264">This method is called after the Quick Filing dialog box is closed.</span></span> <span data-ttu-id="3c151-265">Esse método é uma função que **IQuickFilingDialogCallback** interfaces precisará definir.</span><span class="sxs-lookup"><span data-stu-id="3c151-265">This method is a function that **IQuickFilingDialogCallback** interfaces have to define.</span></span>  <br/> |
|<span data-ttu-id="3c151-266">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="3c151-266">**Syntax**</span></span> <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|<span data-ttu-id="3c151-267">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="3c151-267">**Parameters**</span></span> <br/> | <span data-ttu-id="3c151-268">_diálogo_ &ndash; o objeto de **IQuickFilingDialog** que chamou o método **OnDialogClose** .</span><span class="sxs-lookup"><span data-stu-id="3c151-268">_dialog_ &ndash; The **IQuickFilingDialog** object that called the **OnDialogClose** method.</span></span>  <br/> |
   
<span data-ttu-id="3c151-269">O exemplo a seguir é uma interface de **IQuickFilingDialogCallback** de amostra.</span><span class="sxs-lookup"><span data-stu-id="3c151-269">The following example is a sample **IQuickFilingDialogCallback** interface.</span></span> <span data-ttu-id="3c151-270">O método **OnDialogClose** imprime a seleção do usuário da caixa de diálogo arquivamento rápido no console.</span><span class="sxs-lookup"><span data-stu-id="3c151-270">The **OnDialogClose** method prints the user's selection from the Quick Filing dialog box to the console.</span></span> 
  
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

## <a name="example"></a><span data-ttu-id="3c151-271">Example</span><span class="sxs-lookup"><span data-stu-id="3c151-271">Example</span></span>
<span data-ttu-id="3c151-272"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="3c151-272"></span></span>

<span data-ttu-id="3c151-273">O exemplo de código a seguir abre uma caixa de diálogo Preenchimento rápido que tem um título personalizado, descrição, a lista de resultados recentes, profundidade de árvore, caixa de seleção e botões.</span><span class="sxs-lookup"><span data-stu-id="3c151-273">The following code example opens a Quick Filing dialog box that has a customized title, description, recent result list, tree depth, check box, and buttons.</span></span> <span data-ttu-id="3c151-274">O usuário selecionou o item, pressionado o botão e o estado da caixa de seleção será exibido em uma janela do console quando a caixa de diálogo é fechada.</span><span class="sxs-lookup"><span data-stu-id="3c151-274">The user's selected item, pressed button, and check-box state will be displayed in a console window when the dialog box is closed.</span></span> <span data-ttu-id="3c151-275">Para ver o botão página habilitado, o usuário terá que pesquisar uma página e selecioná-lo, porque a profundidade de árvore está definida para baixo às seções.</span><span class="sxs-lookup"><span data-stu-id="3c151-275">To see the page button enabled, the user will have to search for a page and select it, because the tree depth is set down to sections.</span></span> <span data-ttu-id="3c151-276">A caixa de diálogo não é um filho de qualquer janela.</span><span class="sxs-lookup"><span data-stu-id="3c151-276">The dialog box is not a child of any window.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="3c151-277">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c151-277">See also</span></span>

- [<span data-ttu-id="3c151-278">Referência para desenvolvedores do OneNote</span><span class="sxs-lookup"><span data-stu-id="3c151-278">OneNote developer reference</span></span>](onenote-developer-reference.md)

