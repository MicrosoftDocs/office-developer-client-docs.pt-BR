---
title: Implementação da folha de propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3f1c6497a182231645691f669d8900d33b495503
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430046"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="91fdf-103">Implementação da folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="91fdf-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="91fdf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91fdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91fdf-105">Uma folha de propriedades é uma caixa de diálogo para exibir as propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="91fdf-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="91fdf-106">As propriedades podem ser somente leitura, permitindo que o usuário apenas as visualize ou a leitura/gravação, permitindo que o usuário faça alterações.</span><span class="sxs-lookup"><span data-stu-id="91fdf-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="91fdf-107">Uma folha de propriedades contém uma ou mais janelas filhas sobrepostas chamadas de páginas.</span><span class="sxs-lookup"><span data-stu-id="91fdf-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="91fdf-108">Cada página contém janelas de controle para a configuração de um grupo de propriedades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="91fdf-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="91fdf-109">Os usuários navegam de uma página para a página selecionando uma guia que traz a página correspondente para o primeiro plano da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="91fdf-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="91fdf-110">Os provedores de serviços devem implementar uma folha de propriedades que exibe um conjunto mínimo de propriedades relacionadas à configuração no serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="91fdf-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="91fdf-111">Se você permitir que essas propriedades do serviço de mensagens sejam alteradas, poderá permitir que os usuários de aplicativos cliente, como o painel de controle, façam as alterações ou implementem as alterações de forma programática.</span><span class="sxs-lookup"><span data-stu-id="91fdf-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="91fdf-112">A implementação de folhas de propriedades para exibir e editar outros tipos de propriedades é opcional.</span><span class="sxs-lookup"><span data-stu-id="91fdf-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="91fdf-113">Normalmente, você precisará exibir uma folha de propriedades nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="91fdf-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="91fdf-114">Quando um cliente chama o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) do objeto de status.</span><span class="sxs-lookup"><span data-stu-id="91fdf-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="91fdf-115">Quando MAPI chama o método de logon do objeto do provedor.</span><span class="sxs-lookup"><span data-stu-id="91fdf-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="91fdf-116">Quando MAPI chama a função de ponto de entrada para o serviço de mensagens do provedor.</span><span class="sxs-lookup"><span data-stu-id="91fdf-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="91fdf-117">Os provedores de transporte também implementam folhas de propriedades para exibir propriedades relacionadas a opções de mensagens e provedores de catálogos de endereços implementam folhas de propriedades para exibir e editar informações detalhadas sobre usuários de mensagens e listas de distribuição, pesquisa avançada critérios e modelos para inserir novos usuários.</span><span class="sxs-lookup"><span data-stu-id="91fdf-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="91fdf-118">Você pode usar uma das três técnicas a seguir para criar uma folha de propriedades:</span><span class="sxs-lookup"><span data-stu-id="91fdf-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="91fdf-119">Manualmente, como faria com qualquer caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="91fdf-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="91fdf-120">Usando o controle comum de folha de propriedades fornecido no Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="91fdf-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="91fdf-121">Usando uma tabela de exibição MAPI.</span><span class="sxs-lookup"><span data-stu-id="91fdf-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="91fdf-122">Os provedores devem escolher a última opção (criar uma folha de propriedades usando uma tabela de exibição).</span><span class="sxs-lookup"><span data-stu-id="91fdf-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="91fdf-123">Esta é a opção mais simples porque elimina a necessidade de trabalhar com a interface de usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="91fdf-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="91fdf-124">Para implementar uma folha de propriedades criada a partir de uma tabela de exibição para suas propriedades do serviço de mensagens, use o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="91fdf-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="91fdf-125">Chame [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) para abrir uma seção no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="91fdf-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="91fdf-126">Passe seu [MAPIUID](mapiuid.md) ou nulo para abrir a seção de perfil do provedor.</span><span class="sxs-lookup"><span data-stu-id="91fdf-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="91fdf-127">Chame [CreateIProp](createiprop.md) para criar um objeto de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="91fdf-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="91fdf-128">Chame o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) da seção de perfil para copiar todas as propriedades da seção para o objeto de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="91fdf-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="91fdf-129">Crie uma tabela de exibição criando uma ou mais estruturas [DTPAGE](dtpage.md) que descrevem os controles a serem exibidos na folha de propriedades e chamando a função [BuildDisplayTable](builddisplaytable.md) ou implementando código personalizado.</span><span class="sxs-lookup"><span data-stu-id="91fdf-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="91fdf-130">Chamar [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) para exibir uma folha de propriedades que tenha as propriedades copiadas.</span><span class="sxs-lookup"><span data-stu-id="91fdf-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="91fdf-131">Passe um ponteiro para o objeto de dados de propriedade como o parâmetro _lpConfigData_ e um ponteiro para a tabela de exibição como o parâmetro _lpDisplayTable_ .</span><span class="sxs-lookup"><span data-stu-id="91fdf-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="91fdf-132">Se você deseja substituir o modo de acesso padrão para esta folha de propriedades, não defina o sinalizador DT_EDITABLE para cada controle na tabela de exibição que representa uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="91fdf-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="91fdf-133">Quando todas as alterações tiverem sido feitas na folha de propriedades, chame o método **IMAPIProp:: CopyTo** do objeto de dados de propriedade para copiar as propriedades alteradas de volta para a seção perfil.</span><span class="sxs-lookup"><span data-stu-id="91fdf-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="91fdf-134">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="91fdf-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="91fdf-135">Para obter informações detalhadas sobre como exibir tabelas, consulte [Exibir tabela de implementação](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="91fdf-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="91fdf-136">Para obter informações sobre a implementação de um controle, consulte [controle de implementação de objeto](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="91fdf-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="91fdf-137">Para recuperar o índice de um controle selecionado por um usuário em uma caixa de listagem exibir tabela, aguarde até que o usuário clique em **OK** ou **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="91fdf-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="91fdf-138">Neste ponto, o identificador de entrada do item selecionado é gravado novamente na interface [IMAPIProp: IUnknown](imapipropiunknown.md) como o valor da propriedade especificada pelo membro **UlPRSetProperty** na estrutura [DTBLLBX](dtbllbx.md) .</span><span class="sxs-lookup"><span data-stu-id="91fdf-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="91fdf-139">Se você precisar adicionar ou remover itens da sua caixa de listagem, usando uma tabela de exibição e o método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) não funcionará.</span><span class="sxs-lookup"><span data-stu-id="91fdf-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="91fdf-140">Em vez disso, considere a implementação de uma folha de propriedades com a API de folha de propriedades do Win32 contida no arquivo Comdlg32. dll.</span><span class="sxs-lookup"><span data-stu-id="91fdf-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91fdf-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="91fdf-141">See also</span></span>



[<span data-ttu-id="91fdf-142">Provedores de serviço MAPI</span><span class="sxs-lookup"><span data-stu-id="91fdf-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

