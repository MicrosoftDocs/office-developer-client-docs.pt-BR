---
title: Interfaces das janelas (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: As interfaces Window e Windows são que objetos de API do OneNote 2013 que permitem que os usuários trabalhem com as janelas do OneNote. Esses objetos permitem que os usuários enumerem o conjunto das janelas do OneNote e modifiquem certas propriedades da janela.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317029"
---
# <a name="window-interfaces-onenote"></a><span data-ttu-id="e5b48-104">Interfaces das janelas (OneNote)</span><span class="sxs-lookup"><span data-stu-id="e5b48-104">Window interfaces (OneNote)</span></span>

<span data-ttu-id="e5b48-105">As interfaces**Window** e **Windows** são objetos de API do OneNote 2013 que permitem que os usuários trabalhem com as janelas do OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-105">The **Window** and **Windows** interfaces are OneNote 2013 API objects that enables users to work with OneNote windows.</span></span> <span data-ttu-id="e5b48-106">Esses objetos permitem que os usuários enumerem o conjunto das janelas do OneNote e modifiquem certas propriedades da janela.</span><span class="sxs-lookup"><span data-stu-id="e5b48-106">These objects allow users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
  
## <a name="onenote-window-views"></a><span data-ttu-id="e5b48-107">OneNote window views</span><span class="sxs-lookup"><span data-stu-id="e5b48-107">OneNote window views</span></span>

<span data-ttu-id="e5b48-108">A lista a seguir mostra os quatro modos de exibição que estão disponíveis para janelas do OneNote:</span><span class="sxs-lookup"><span data-stu-id="e5b48-108">The following list shows the four view modes that you can use for OneNote windows:</span></span> 
  
- <span data-ttu-id="e5b48-109">Modo de exibição normal, exibe a janela padrão do OneNote onde os painéis de navegação do bloco de anotações e da página estiverem visível.</span><span class="sxs-lookup"><span data-stu-id="e5b48-109">Normal view—Displays the default OneNote window in which the Notebook and Page navigation panes are visible.</span></span>
    
- <span data-ttu-id="e5b48-110">Total de exibição de página, exibe uma interface de usuário mínima (UI) onde os painéis de página e bloco de anotações não são exibidos.</span><span class="sxs-lookup"><span data-stu-id="e5b48-110">Full Page view—Displays a minimal user-interface (UI) view in which the Notebook and Page panes are not displayed.</span></span>
    
- <span data-ttu-id="e5b48-111">Anotação rápida, exibe uma pequena janela que permite aos usuários fazer anotações curtas.</span><span class="sxs-lookup"><span data-stu-id="e5b48-111">Quick note—Displays a small window that allows users to take short notes.</span></span> <span data-ttu-id="e5b48-112">Anotações rápidas normalmente podem ser acessadas por meio do ícone do OneNote na área de notificação do Windows, mas você também pode acessá-los por meio do guia**modo de exibição**no OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-112">You would usually access quick notes through the OneNote icon in the Windows notification area, but you can also access them through the **View** tab in OneNote.</span></span> 
    
- <span data-ttu-id="e5b48-113">Encaixar na área de trabalho, exibe uma janela do OneNote que você pode encaixar a qualquer lado da área de trabalho (semelhante à barra de tarefas).</span><span class="sxs-lookup"><span data-stu-id="e5b48-113">Dock to Desktop—Displays a OneNote window that you can dock to any side of the desktop (similar to the taskbar).</span></span> <span data-ttu-id="e5b48-114">Esse modo de exibição reduz o tamanho da área de trabalho para ajustá-la a janela.</span><span class="sxs-lookup"><span data-stu-id="e5b48-114">This view reduces the size of the desktop to fit the window.</span></span> <span data-ttu-id="e5b48-115">Você pode encaixar apenas uma janela a qualquer momento e janela fica sempre visível sem bloquear a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e5b48-115">You can dock only one window at any time, and the window is always visible without blocking the desktop.</span></span> 
    
<span data-ttu-id="e5b48-116">A figura a seguir mostra como os itens modo de página inteira, encaixar na área de trabalho modo de exibição, e anotações rápidas são exibidos na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e5b48-116">The following figure shows what the Full Page view, Dock to Desktop view, and quick notes look like on your desktop.</span></span>
  
<span data-ttu-id="e5b48-117">\*\*exibição do OneNote \*\*</span><span class="sxs-lookup"><span data-stu-id="e5b48-117">**OneNote views**</span></span>

<span data-ttu-id="e5b48-118">![Modos de exibição da janela OneNote](media/ON15Con_views.jpg "exibições de janela do OneNote")</span><span class="sxs-lookup"><span data-stu-id="e5b48-118">![OneNote window views](media/ON15Con_views.jpg "OneNote window views")</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="e5b48-119">Interfaces</span><span class="sxs-lookup"><span data-stu-id="e5b48-119">Interfaces</span></span>

<span data-ttu-id="e5b48-120">Esta seção lista as interfaces e membros que você pode usar para modificar as janelas do OneNote por programação.</span><span class="sxs-lookup"><span data-stu-id="e5b48-120">This section lists the interfaces and members that you can use to modify OneNote windows programmatically.</span></span>
  
### <a name="windows-interface"></a><span data-ttu-id="e5b48-121">Interface do Windows</span><span class="sxs-lookup"><span data-stu-id="e5b48-121">Windows interface</span></span>

<span data-ttu-id="e5b48-122">A interface **Windows** também permite ao usuário acessar o conjunto de janelas abertas do OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-122">The **Windows** interface allows the user to access the set of opened OneNote windows.</span></span> <span data-ttu-id="e5b48-123">É uma propriedade do OneNote da classe **aplicativo** acessado por meio de**Application.Windows**.</span><span class="sxs-lookup"><span data-stu-id="e5b48-123">It is a property of the OneNote **Application** class, accessed through **Application.Windows**.</span></span> <span data-ttu-id="e5b48-124">Isso retorna o conjunto enumerado de janelas do OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-124">This returns the enumerated set of OneNote windows.</span></span> 
  
<span data-ttu-id="e5b48-125">**Propriedades**</span><span class="sxs-lookup"><span data-stu-id="e5b48-125">**Properties**</span></span>

|<span data-ttu-id="e5b48-126">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e5b48-126">**Name**</span></span>|<span data-ttu-id="e5b48-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e5b48-127">**Type**</span></span>|<span data-ttu-id="e5b48-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e5b48-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e5b48-129">**Contagem**</span><span class="sxs-lookup"><span data-stu-id="e5b48-129">**Count**</span></span> <br/> |<span data-ttu-id="e5b48-130">ULong</span><span class="sxs-lookup"><span data-stu-id="e5b48-130">ulong</span></span>  <br/> |<span data-ttu-id="e5b48-131">Obtém o número dos objetos Window no **conjunto** do Windows.</span><span class="sxs-lookup"><span data-stu-id="e5b48-131">Gets the number of **Window** objects in the **Windows** set.</span></span>  <br/> |
|<span data-ttu-id="e5b48-132">**CurrentWindow**</span><span class="sxs-lookup"><span data-stu-id="e5b48-132">**CurrentWindow**</span></span> <br/> |<span data-ttu-id="e5b48-133">**Janela**</span><span class="sxs-lookup"><span data-stu-id="e5b48-133">**Window**</span></span> <br/> |<span data-ttu-id="e5b48-134">Obtém o objeto**janela**da janela ativa do OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-134">Gets the **Window** object of the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="e5b48-135">**Items**</span><span class="sxs-lookup"><span data-stu-id="e5b48-135">**Items**</span></span> <br/> |<span data-ttu-id="e5b48-136">**Janela**</span><span class="sxs-lookup"><span data-stu-id="e5b48-136">**Window**</span></span> <br/> |<span data-ttu-id="e5b48-137">Retorna o objeto**janela**que corresponde ao valor de índice passado.</span><span class="sxs-lookup"><span data-stu-id="e5b48-137">Returns the **Window** object that corresponds to the index value passed.</span></span> <span data-ttu-id="e5b48-138">Essa propriedade não pode ser acessada diretamente.</span><span class="sxs-lookup"><span data-stu-id="e5b48-138">This property cannot be accessed directly.</span></span> <span data-ttu-id="e5b48-139">Para retornar um objeto **janela**, use **Windows [índice (uint)]**.</span><span class="sxs-lookup"><span data-stu-id="e5b48-139">To return a **Window** object, use **Windows [(uint) index]**.</span></span>  <br/> |
   
### <a name="window-interface"></a><span data-ttu-id="e5b48-140">Interface de janela</span><span class="sxs-lookup"><span data-stu-id="e5b48-140">Window interface</span></span>

<span data-ttu-id="e5b48-141">A interface **janela** também permite ao usuário acessar certas propriedades de cada janela.</span><span class="sxs-lookup"><span data-stu-id="e5b48-141">The **Window** interface allows the user to access certain properties of each window.</span></span> <span data-ttu-id="e5b48-142">Cada janela do OneNote pode ser acessada por enumerar através da propriedade **Windows**da classe **aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="e5b48-142">Each OneNote window can be accessed by enumerating through the **Windows** property of the **Application** class.</span></span> 
  
<span data-ttu-id="e5b48-143">**Propriedades**</span><span class="sxs-lookup"><span data-stu-id="e5b48-143">**Properties**</span></span>

|<span data-ttu-id="e5b48-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e5b48-144">**Name**</span></span>|<span data-ttu-id="e5b48-145">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e5b48-145">**Type**</span></span>|<span data-ttu-id="e5b48-146">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e5b48-146">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e5b48-147">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="e5b48-147">**Active**</span></span> <br/> |<span data-ttu-id="e5b48-148">bool</span><span class="sxs-lookup"><span data-stu-id="e5b48-148">bool</span></span>  <br/> |<span data-ttu-id="e5b48-149">Obtém ou define um valor que indica se a janela é a janela ativa do OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-149">Gets or sets a value that indicates whether the window is the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="e5b48-150">**Application**</span><span class="sxs-lookup"><span data-stu-id="e5b48-150">**Application**</span></span> <br/> |<span data-ttu-id="e5b48-151">**Application**</span><span class="sxs-lookup"><span data-stu-id="e5b48-151">**Application**</span></span> <br/> |<span data-ttu-id="e5b48-152">Obtém o objeto **aplicativo** do OneNote que estão associados com a janela.</span><span class="sxs-lookup"><span data-stu-id="e5b48-152">Gets the OneNote **Application** object that is associated with the window.</span></span>  <br/> |
|<span data-ttu-id="e5b48-153">**CurrentPageId**</span><span class="sxs-lookup"><span data-stu-id="e5b48-153">**CurrentPageId**</span></span> <br/> |<span data-ttu-id="e5b48-154">string</span><span class="sxs-lookup"><span data-stu-id="e5b48-154">string</span></span>  <br/> |<span data-ttu-id="e5b48-155">Obtém a ID de objeto da página do OneNote ativa da janela.</span><span class="sxs-lookup"><span data-stu-id="e5b48-155">Gets the object ID of the active OneNote page of the window.</span></span>  <br/> |
|<span data-ttu-id="e5b48-156">**CurrentSectionId**</span><span class="sxs-lookup"><span data-stu-id="e5b48-156">**CurrentSectionId**</span></span> <br/> |<span data-ttu-id="e5b48-157">string</span><span class="sxs-lookup"><span data-stu-id="e5b48-157">string</span></span>  <br/> |<span data-ttu-id="e5b48-158">Obtém a ID de objeto da seção do OneNote ativa da janela.</span><span class="sxs-lookup"><span data-stu-id="e5b48-158">Gets the object ID of the active OneNote section of the window.</span></span>  <br/> |
|<span data-ttu-id="e5b48-159">**CurrentSectionGroupId**</span><span class="sxs-lookup"><span data-stu-id="e5b48-159">**CurrentSectionGroupId**</span></span> <br/> |<span data-ttu-id="e5b48-160">string</span><span class="sxs-lookup"><span data-stu-id="e5b48-160">string</span></span>  <br/> |<span data-ttu-id="e5b48-161">Obtém a ID de objeto da seção de grupo ativa da janela do OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-161">Gets the object ID of the active OneNote section group of the window.</span></span>  <br/> |
|<span data-ttu-id="e5b48-162">**CurrentNotebookId**</span><span class="sxs-lookup"><span data-stu-id="e5b48-162">**CurrentNotebookId**</span></span> <br/> |<span data-ttu-id="e5b48-163">string</span><span class="sxs-lookup"><span data-stu-id="e5b48-163">string</span></span>  <br/> |<span data-ttu-id="e5b48-164">Obtém a ID de objeto do bloco de anotações ativo na janela do OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-164">Gets the object ID of the active OneNote notebook of the window.</span></span>  <br/> |
|<span data-ttu-id="e5b48-165">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="e5b48-165">**DockedLocation**</span></span> <br/> |<span data-ttu-id="e5b48-166">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="e5b48-166">**DockedLocation**</span></span> <br/> |<span data-ttu-id="e5b48-167">Obtém ou define a localização encaixada da janela do OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-167">Gets or sets the docked location of the OneNote window.</span></span>  <br/> |
|<span data-ttu-id="e5b48-168">**FullPageView**</span><span class="sxs-lookup"><span data-stu-id="e5b48-168">**FullPageView**</span></span> <br/> |<span data-ttu-id="e5b48-169">bool</span><span class="sxs-lookup"><span data-stu-id="e5b48-169">bool</span></span>  <br/> |<span data-ttu-id="e5b48-170">Obtém ou define um valor que indica se a janela está no modo de exibição de página inteira (exibição mínima de interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="e5b48-170">Gets or sets a value that indicates whether the window is in Full Page view (minimal UI view).</span></span>  <br/> |
|<span data-ttu-id="e5b48-171">**SideNote**</span><span class="sxs-lookup"><span data-stu-id="e5b48-171">**SideNote**</span></span> <br/> |<span data-ttu-id="e5b48-172">bool</span><span class="sxs-lookup"><span data-stu-id="e5b48-172">bool</span></span>  <br/> |<span data-ttu-id="e5b48-173">Obtém ou define um valor que indica se a janela é uma janela de anotação rápida.</span><span class="sxs-lookup"><span data-stu-id="e5b48-173">Gets or sets a value that indicates whether the window is a quick note window.</span></span>  <br/> |
|<span data-ttu-id="e5b48-174">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="e5b48-174">**WindowHandle**</span></span> <br/> |<span data-ttu-id="e5b48-175">ULong</span><span class="sxs-lookup"><span data-stu-id="e5b48-175">ulong</span></span>  <br/> |<span data-ttu-id="e5b48-176">É a ID de alça da janela do OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-176">Gets the handle ID of the OneNote window.</span></span>  <br/> |
   
<span data-ttu-id="e5b48-177">**Métodos**</span><span class="sxs-lookup"><span data-stu-id="e5b48-177">**Methods**</span></span>
  
<span data-ttu-id="e5b48-178">Você pode usar os seguintes métodos das interfaces**janela**para acessar objetos específicos na janela do OneNote ou nas URLs especificadas.</span><span class="sxs-lookup"><span data-stu-id="e5b48-178">You can use the following methods of the **Window** interface to navigate to specified objects in the OneNote window or to specified URLs.</span></span> 
  
<span data-ttu-id="e5b48-179">**NavigateTo**</span><span class="sxs-lookup"><span data-stu-id="e5b48-179">**NavigateTo**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5b48-180">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e5b48-180">**Description**</span></span> <br/> |<span data-ttu-id="e5b48-181">Leva até um objeto específico na janela do OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-181">Navigates to the specified object in the OneNote window.</span></span> <span data-ttu-id="e5b48-182">Por exemplo, você pode navegar em seções, páginas elementos de estrutura das páginas.</span><span class="sxs-lookup"><span data-stu-id="e5b48-182">For example, you can navigate to sections, pages, and outline elements within pages.</span></span>  <br/> |
|<span data-ttu-id="e5b48-183">**A sintaxe que você escolher da tabela de sintaxe de propriedade de valor múltiplo é especificada como um valor do parâmetro em um cmdlet. Por exemplo, o comando a seguir adiciona vários valores para uma propriedade com valores múltiplos:**</span><span class="sxs-lookup"><span data-stu-id="e5b48-183">**Syntax**</span></span> <br/> | <span data-ttu-id="e5b48-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span><span class="sxs-lookup"><span data-stu-id="e5b48-184"></span></span> <br/> |
|<span data-ttu-id="e5b48-185">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="e5b48-185">**Parameters**</span></span> <br/> | <span data-ttu-id="e5b48-186">_bstrHierarchyObjectID_: Hierarquia do OneNote ID do objeto que você quer navegar.</span><span class="sxs-lookup"><span data-stu-id="e5b48-186">_bstrHierarchyObjectID_—The hierarchy OneNote ID of the object you want to navigate to.</span></span> <span data-ttu-id="e5b48-187">A ID de objeto pode fazer referência a um bloco de anotações do OneNote, seção, grupo de seção ou página.</span><span class="sxs-lookup"><span data-stu-id="e5b48-187">The object ID can reference a OneNote notebook, section, section group, or page.</span></span>  <br/>  <span data-ttu-id="e5b48-188">_bstrObjectID_, a ID do OneNote de um objeto específico para navegar até em uma página do OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-188">_bstrObjectID_—The OneNote ID of the specific object to navigate to within a OneNote page.</span></span> <span data-ttu-id="e5b48-189">Se o usuário não quiser navegar até um objeto específico em uma página, esse parâmetro será definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="e5b48-189">If the user does not want to navigate to a specific object on a page, this parameter is set to null.</span></span>  <br/> |
   
<span data-ttu-id="e5b48-190">**NavigateToUrl**</span><span class="sxs-lookup"><span data-stu-id="e5b48-190">**NavigateToUrl**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5b48-191">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e5b48-191">**Description**</span></span> <br/> |<span data-ttu-id="e5b48-192">Se for aprovado um link do OneNote (onenote: / /), a janela do OneNote abrirá no local correspondente no OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5b48-192">If passed a OneNote link (onenote://), opens the OneNote window to the corresponding location in OneNote.</span></span> <span data-ttu-id="e5b48-193">No entanto, se o link está um link externo, como https:// ou file://,uma caixa de diálogo de segurança aparecerá.</span><span class="sxs-lookup"><span data-stu-id="e5b48-193">However, if the link is an external link, such as https:// or file://, a security dialog box will appear.</span></span> <span data-ttu-id="e5b48-194">Após a demissão, o OneNote tentará abrir o link e um erro HResult.hrObjectDoesNotExist será retornado.</span><span class="sxs-lookup"><span data-stu-id="e5b48-194">Upon dismissal, OneNote attempts to open up the link and an HResult.hrObjectDoesNotExist error is returned.</span></span>  <br/> |
|<span data-ttu-id="e5b48-195">**A sintaxe que você escolher da tabela de sintaxe de propriedade de valor múltiplo é especificada como um valor do parâmetro em um cmdlet. Por exemplo, o comando a seguir adiciona vários valores para uma propriedade com valores múltiplos:**</span><span class="sxs-lookup"><span data-stu-id="e5b48-195">**Syntax**</span></span> <br/> | <span data-ttu-id="e5b48-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span><span class="sxs-lookup"><span data-stu-id="e5b48-196"></span></span> <br/> |
|<span data-ttu-id="e5b48-197">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="e5b48-197">**Parameters**</span></span> <br/> | <span data-ttu-id="e5b48-198">_bstrUrl_, a URL para navegar até.</span><span class="sxs-lookup"><span data-stu-id="e5b48-198">_bstrUrl_—The URL to navigate to.</span></span>  <br/> |
   
<span data-ttu-id="e5b48-199">**SetDockedLocation**</span><span class="sxs-lookup"><span data-stu-id="e5b48-199">**SetDockedLocation**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5b48-200">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e5b48-200">**Description**</span></span> <br/> |<span data-ttu-id="e5b48-201">Encaixa a janela na localização especificada por **dockLocation** e pelo monitor na **ptMonitor**.</span><span class="sxs-lookup"><span data-stu-id="e5b48-201">Docks the window to the location specified by **dockLocation** and the monitor at **ptMonitor**.</span></span>  <br/> |
|<span data-ttu-id="e5b48-202">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="e5b48-202">**Syntax**</span></span> <br/> | <span data-ttu-id="e5b48-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span><span class="sxs-lookup"><span data-stu-id="e5b48-203"></span></span> <br/> |
|<span data-ttu-id="e5b48-204">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="e5b48-204">**Parameters**</span></span> <br/> | <span data-ttu-id="e5b48-205">_dockLocation_ -indica o local encaixado de uma janela do OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="e5b48-205">_dockLocation_ - Indicates the docked location of a OneNote 2013 window.</span></span>  <br/>  <span data-ttu-id="e5b48-206">_ptMonitor_ -(opcional) indica em coordenadas x,y em qual monitor a janela deve ser encaixada.</span><span class="sxs-lookup"><span data-stu-id="e5b48-206">_ptMonitor_ - (Optional) Indicates in x,y co-ordinates which monitor the window should be docked to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="e5b48-207">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e5b48-207">Example</span></span>

<span data-ttu-id="e5b48-208">O seguinte código percorre o OneNote do windows para encontrar uma janela encaixada.</span><span class="sxs-lookup"><span data-stu-id="e5b48-208">The following code iterates through the OneNote windows to find a docked window.</span></span> <span data-ttu-id="e5b48-209">Se não houver nenhuma janela encaixada, o exemplo encaixa a janela ativa.</span><span class="sxs-lookup"><span data-stu-id="e5b48-209">If no docked window exists, the example docks the active window.</span></span> <span data-ttu-id="e5b48-210">Se não houver nenhuma janela encaixada, o código criará uma nova janela encaixada.</span><span class="sxs-lookup"><span data-stu-id="e5b48-210">If no active window exists, the code creates a new docked window.</span></span>
  
```cs
using System;
using System.Diagnostics;
using Microsoft.Office.Interop.OneNote;
namespace SampleWND
{
    class DockOneNoteWindow
    {
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = new Microsoft.Office.Interop.OneNote.Application();
            // Search through all OneNote windows for a docked window and activate it.
            bool foundDockedWND = false;
            for (int i = 0; i < app.Windows.Count; i++)
            {
                if (app.Windows[(uint) i].DockedLocation != DockLocation.dlNone)
                {
                    foundDockedWND = true;
                    app.Windows[(uint) i].Active = true;
                }
            }
            
            // If no docked window exists, dock the active window.
            if (!foundDockedWND && (app.Windows.Count > 0))
                app.Windows.CurrentWindow.DockedLocation = DockLocation.dlDefault;
            // If no active window exists, create a new docked window.
            if (app.Windows.Count < 1)
            {
                Process oneProc = new Process();
                oneProc.StartInfo.FileName = "onenote.exe";
                oneProc.StartInfo.Arguments = "/docked";
                oneProc.Start();
            }
        }
    }
}

```

## <a name="see-also"></a><span data-ttu-id="e5b48-211">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5b48-211">See also</span></span>

- [<span data-ttu-id="e5b48-212">Referência do desenvolvedor do OneNote</span><span class="sxs-lookup"><span data-stu-id="e5b48-212">OneNote developer reference</span></span>](onenote-developer-reference.md)

