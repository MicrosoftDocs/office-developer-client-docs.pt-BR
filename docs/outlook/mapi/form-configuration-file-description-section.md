---
title: Seção de [descrição] do arquivo de configuração de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d3673c3b10afb55121339e335163ce9b2e5937e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766578"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="213ef-103">Seção de [descrição] do arquivo de configuração de formulário</span><span class="sxs-lookup"><span data-stu-id="213ef-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="213ef-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="213ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="213ef-105">A seção **[descrição]** lista todas as propriedades do formulário que estão associadas a controles de interface do usuário, mais atributos que são usados na localização de formulário do formulário.</span><span class="sxs-lookup"><span data-stu-id="213ef-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="213ef-106">O **MessageClass**, **Clsid**e entradas de **DisplayName** , que identificam o nome de classe de mensagem do formulário, seu GUID e nome de exibição da classe de mensagem, respectivamente, são entradas necessárias usadas para localizar o formulário dentro da biblioteca de formulário .</span><span class="sxs-lookup"><span data-stu-id="213ef-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="213ef-107">As entradas restantes são opcionais.</span><span class="sxs-lookup"><span data-stu-id="213ef-107">The remaining entries are optional.</span></span> <span data-ttu-id="213ef-108">O formato da seção **[descrição]** é:</span><span class="sxs-lookup"><span data-stu-id="213ef-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="213ef-109">A seção **[descrição]** lista todas as propriedades do formulário que estão associadas a controles de interface do usuário, mais atributos que são usados na localização de formulário do formulário.</span><span class="sxs-lookup"><span data-stu-id="213ef-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="213ef-110">O **MessageClass**, **Clsid**e entradas de **DisplayName** , que identificam o nome de classe de mensagem do formulário, seu GUID e nome de exibição da classe de mensagem, respectivamente, são entradas necessárias usadas para localizar o formulário dentro da biblioteca de formulário .</span><span class="sxs-lookup"><span data-stu-id="213ef-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="213ef-111">As entradas restantes são opcionais.</span><span class="sxs-lookup"><span data-stu-id="213ef-111">The remaining entries are optional.</span></span> <span data-ttu-id="213ef-112">O formato da seção **[descrição]** é:</span><span class="sxs-lookup"><span data-stu-id="213ef-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="213ef-113">**[Descrição] MessageClass** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="213ef-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="213ef-114">**CLSID** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="213ef-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="213ef-115">**DisplayName** =  _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="213ef-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="213ef-116">**SmallIcon** =  _caminho_</span><span class="sxs-lookup"><span data-stu-id="213ef-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="213ef-117">**LargeIcon** =  _caminho_</span><span class="sxs-lookup"><span data-stu-id="213ef-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="213ef-118">Entradas opcionais são:</span><span class="sxs-lookup"><span data-stu-id="213ef-118">Optional entries are:</span></span>
  
 <span data-ttu-id="213ef-119">**Categoria** =  _exibido a cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="213ef-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="213ef-120">**Subcategoria** =  _exibido a cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="213ef-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="213ef-121">**Comentário** =  _exibido a cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="213ef-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="213ef-122">**Proprietário** =  _exibido a cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="213ef-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="213ef-123">**Número** =  _exibido a cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="213ef-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="213ef-124">**Versão** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="213ef-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="213ef-125">**Localidade** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="213ef-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="213ef-126">**Oculto** =  _inteiro_</span><span class="sxs-lookup"><span data-stu-id="213ef-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="213ef-127">**DesignerToolName** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="213ef-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="213ef-128">**DesignerToolGuid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="213ef-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="213ef-129">**DesignerRuntimeGuid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="213ef-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="213ef-130">**ComposeInFolder** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="213ef-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="213ef-131">**ComposeCommand** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="213ef-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="213ef-132">As entradas de **categoria** e uma **subcategoria** são usadas pelo instaladores de formulário para configurar a categorização de padrão de formulários dentro da interface do usuário do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="213ef-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="213ef-133">Por exemplo, uma hierarquia pode ser configurada tal onde "Help Desk" é a categoria e "Software" e "Hardware" eram as subcategorias.</span><span class="sxs-lookup"><span data-stu-id="213ef-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="213ef-134">Esta categorização, em seguida, pode ser usada por aplicativos de visualizador para exibir mensagens de uma maneira mais organizada.</span><span class="sxs-lookup"><span data-stu-id="213ef-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="213ef-135">As entradas de **comentário**, **proprietário**e **número** são todas as cadeias de caracteres de comentário que aparecem na interface do usuário do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="213ef-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="213ef-136">Estas são as propriedades específicas de formulário que podem ser usadas a critério do desenvolvedor do formulário.</span><span class="sxs-lookup"><span data-stu-id="213ef-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="213ef-137">Por exemplo, a entrada de **comentário** pode ser usada para indicar a finalidade do formulário, a entrada do **proprietário** usada para indicar a pessoa ou organização responsável por manter o formulário e o número usado para rastrear uma versão diferente do formulário.</span><span class="sxs-lookup"><span data-stu-id="213ef-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="213ef-138">Para o **comentário** de entrada, até dez linhas de comentários pode ser incluída.</span><span class="sxs-lookup"><span data-stu-id="213ef-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="213ef-139">A primeira linha de comentários usa a palavra "Comentário" como a chave, a segunda linha de comentários usa "Comment1" como a chave, e assim por diante por meio de "Comment9".</span><span class="sxs-lookup"><span data-stu-id="213ef-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="213ef-140">As entradas **LargeIcon** e **SmallIcon** são usadas para especificar o caminho para os recursos de ícone usado para exibir ícones na interface de usuário do aplicativo cliente, que normalmente é para linhas de tabela que incluem **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou colunas de propriedade **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="213ef-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="213ef-141">Nomes de arquivo de ícone podem ser especificados como nomes de caminho relativo para o diretório onde o arquivo de configuração do formulário está instalado.</span><span class="sxs-lookup"><span data-stu-id="213ef-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="213ef-142">A entrada de **versão** é usada para indicar o número da versão do formulário.</span><span class="sxs-lookup"><span data-stu-id="213ef-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="213ef-143">**Locale** é o identificador de idioma de três letras da biblioteca de formulários de destino.</span><span class="sxs-lookup"><span data-stu-id="213ef-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="213ef-144">Uma lista desses identificadores pode ser encontrada na _referência do programador do Win32_.</span><span class="sxs-lookup"><span data-stu-id="213ef-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="213ef-145">A entrada de **oculto** indica se o formulário deve ser exibido na interface do usuário de um provedor biblioteca de formulário: 1 indica que o arquivo está oculto e 0 indica que o formulário está visível.</span><span class="sxs-lookup"><span data-stu-id="213ef-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="213ef-146">Um arquivo de configuração do formulário de exemplo é mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="213ef-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="213ef-147">A entrada **ComposeInFolder** controla se o formulário foi projetado para ser colocado na pasta atual ou na caixa de entrada do usuário quando o usuário salva a mensagem enquanto escrevendo: 1 indica que o formulário deve ir na pasta atual e 0 indica que ele deve vá na caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="213ef-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="213ef-148">A entrada **ComposeCommand** é a cadeia de caracteres sejam colocadas no aplicativo cliente do menu redigir.</span><span class="sxs-lookup"><span data-stu-id="213ef-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="213ef-149">Se não for especificado, a entrada **DisplayName** será usada.</span><span class="sxs-lookup"><span data-stu-id="213ef-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
```cpp
[Description]
MessageClass = IPM.Help
Clsid = {00020D31-0000-0000-C000-000000000046}
DisplayName = Help Desk Request Form
;optional entries
Category = Help Desk Requests
Subcategory = New Requests
Comment = Use this form to request network assistance
Owner = Help Desk
Number = 1
SmallIcon = C:\WINDOWS|EFORMS\HELPDESK\HDSMALL.ICO
LargeIcon = C:\WINDOWS|EFORMS\HELPDESK\HDLARGE.ICO
Version = 1.00
Locale = enu
Hidden = 0
ComposeInFolder = 0
ComposeCommand = &Help Desk Request
 
```


