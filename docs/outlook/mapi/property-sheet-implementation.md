---
title: Implementação da folha de propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 406451adac3cd73286feb787bd6b4d2f356aa283
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770194"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="acc21-103">Implementação da folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="acc21-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="acc21-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="acc21-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="acc21-105">Uma folha de propriedades é uma caixa de diálogo para exibir as propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="acc21-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="acc21-106">As propriedades podem ser somente leitura, permitindo que o usuário apenas para exibi-los, ou leitura/gravação, permitindo que o usuário faça alterações.</span><span class="sxs-lookup"><span data-stu-id="acc21-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="acc21-107">Uma folha de propriedades contém uma ou mais janelas sobrepostas filho chamadas páginas.</span><span class="sxs-lookup"><span data-stu-id="acc21-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="acc21-108">Cada página contém o controle do windows para configurar um grupo de propriedades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="acc21-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="acc21-109">Os usuários navegar pelas páginas selecionando uma guia que traz a página correspondente para o primeiro plano da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="acc21-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="acc21-110">Provedores de serviços devem implementar uma folha de propriedades que exibe um conjunto mínimo de propriedades relacionadas a configuração no serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="acc21-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="acc21-111">Se você permitir essas propriedades do serviço de mensagem a ser alterado, você pode permitir que os usuários do cliente de aplicativos, como o painel de controle, para fazer as alterações ou implementar as alterações programaticamente.</span><span class="sxs-lookup"><span data-stu-id="acc21-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="acc21-112">A implementação de folhas de propriedades para exibir e editar outros tipos de propriedades é opcional.</span><span class="sxs-lookup"><span data-stu-id="acc21-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="acc21-113">Normalmente, você precisará de uma folha de propriedades de exibição nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="acc21-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="acc21-114">Quando um cliente chama o método de [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) do objeto seu status.</span><span class="sxs-lookup"><span data-stu-id="acc21-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="acc21-115">Quando o MAPI chama o método de logon do objeto do provedor.</span><span class="sxs-lookup"><span data-stu-id="acc21-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="acc21-116">Quando o MAPI chama a função do ponto de entrada para o serviço de mensagem do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="acc21-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="acc21-117">Provedores de transporte também implementam folhas de propriedades para exibir as propriedades relacionadas às opções de mensagem e folhas de propriedades para exibir e editar informações detalhadas sobre as mensagens de usuários e listas de distribuição, pesquisa avançada de implementar provedores do catálogo de endereços critérios e modelos para inserir novos usuários.</span><span class="sxs-lookup"><span data-stu-id="acc21-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="acc21-118">Você pode usar uma das três técnicas a seguir para criar uma folha de propriedades:</span><span class="sxs-lookup"><span data-stu-id="acc21-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="acc21-119">Manualmente, como faria com qualquer caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="acc21-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="acc21-120">Usando o controle comuns da folha de propriedade fornecido no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="acc21-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="acc21-121">Usando uma MAPI exibe a tabela.</span><span class="sxs-lookup"><span data-stu-id="acc21-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="acc21-122">Provedores devem escolher a última opção (criar uma folha de propriedades usando uma tabela de exibição).</span><span class="sxs-lookup"><span data-stu-id="acc21-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="acc21-123">Esta é a opção mais simples, pois elimina a necessidade de trabalhar com a interface de usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="acc21-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="acc21-124">Para implementar uma folha de propriedades construída a partir de uma tabela de exibição para as propriedades do serviço de mensagem, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="acc21-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="acc21-125">Chame [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para abrir uma seção no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="acc21-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="acc21-126">Passe o [MAPIUID](mapiuid.md) ou NULL para abrir a seção de perfil do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="acc21-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="acc21-127">Chame [CreateIProp](createiprop.md) para criar um objeto de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="acc21-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="acc21-128">Chame o método de [IMAPIProp::CopyTo](imapiprop-copyto.md) da seção perfil para copiar todas as propriedades da seção para o objeto de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="acc21-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="acc21-129">Crie uma tabela de exibição com a criação de uma ou mais estruturas [DTPAGE](dtpage.md) que descrevem os controles para que ele apareça na folha de propriedades e chamar a função [BuildDisplayTable](builddisplaytable.md) ou por meio da implementação código personalizado.</span><span class="sxs-lookup"><span data-stu-id="acc21-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="acc21-130">Chame [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para exibir uma folha de propriedades que tem as propriedades copiadas.</span><span class="sxs-lookup"><span data-stu-id="acc21-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="acc21-131">Passe um ponteiro para o objeto de dados de propriedade como o parâmetro _lpConfigData_ e um ponteiro para a tabela de exibição como o parâmetro _lpDisplayTable_ .</span><span class="sxs-lookup"><span data-stu-id="acc21-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="acc21-132">Se você quiser substituir o modo de acesso padrão para essa folha de propriedades, não defina o sinalizador DT_EDITABLE para cada controle na tabela de exibição que representa uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="acc21-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="acc21-133">Quando todas as alterações são feitas na folha de propriedades, chame o método de **IMAPIProp::CopyTo** do objeto de dados de propriedade para copiar as propriedades alteradas voltar para a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="acc21-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="acc21-134">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="acc21-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="acc21-135">Para obter informações detalhadas sobre tabelas de exibição, consulte [Exibir implementação da tabela](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="acc21-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="acc21-136">Para obter informações sobre como implementar um controle, consulte [Implementação do objeto de controle](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="acc21-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="acc21-137">Para recuperar o índice de um controle que um usuário seleciona em uma caixa de listagem da tabela de exibição, aguarde até que o usuário clica **Okey** ou em **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="acc21-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="acc21-138">Neste ponto, o identificador de entrada do item selecionado será gravado novamente o [IMAPIProp: IUnknown](imapipropiunknown.md) interface como o valor da propriedade especificada pelo membro **ulPRSetProperty** na estrutura [DTBLLBX](dtbllbx.md) .</span><span class="sxs-lookup"><span data-stu-id="acc21-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="acc21-139">Se você precisar ser capaz de adicionar ou remover itens da sua caixa de listagem, usar uma tabela de exibição e o método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) não funcionará.</span><span class="sxs-lookup"><span data-stu-id="acc21-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="acc21-140">Em vez disso, considere a implementação de uma folha de propriedades com a API de folha de propriedade Win32 contida no arquivo Comdlg32.</span><span class="sxs-lookup"><span data-stu-id="acc21-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="acc21-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="acc21-141">See also</span></span>



[<span data-ttu-id="acc21-142">Provedores de serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="acc21-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

