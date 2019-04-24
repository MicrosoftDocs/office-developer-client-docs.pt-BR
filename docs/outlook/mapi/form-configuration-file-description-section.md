---
title: Seção do arquivo de configuração de formulários [Descrição]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320983"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="c2db4-103">Seção do arquivo de configuração de formulários [Descrição]</span><span class="sxs-lookup"><span data-stu-id="c2db4-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="c2db4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2db4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2db4-105">A seção **[Descrição]** lista todas as propriedades do formulário que estão associadas aos controles na interface do usuário do formulário, além de atributos usados na localização do formulário.</span><span class="sxs-lookup"><span data-stu-id="c2db4-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="c2db4-106">As \*\*\*\* entradas MessageClass, **CLSID**e **DisplayName** , que identificam o nome da classe de mensagem do formulário, seu GUID e o nome de exibição da classe de mensagem, respectivamente, são entradas obrigatórias usadas para localizar o formulário na biblioteca de formulários .</span><span class="sxs-lookup"><span data-stu-id="c2db4-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="c2db4-107">As entradas restantes são opcionais.</span><span class="sxs-lookup"><span data-stu-id="c2db4-107">The remaining entries are optional.</span></span> <span data-ttu-id="c2db4-108">O formato da seção **[Descrição]** é:</span><span class="sxs-lookup"><span data-stu-id="c2db4-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="c2db4-109">A seção **[Descrição]** lista todas as propriedades do formulário que estão associadas aos controles na interface do usuário do formulário, além de atributos usados na localização do formulário.</span><span class="sxs-lookup"><span data-stu-id="c2db4-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="c2db4-110">As \*\*\*\* entradas MessageClass, **CLSID**e **DisplayName** , que identificam o nome da classe de mensagem do formulário, seu GUID e o nome de exibição da classe de mensagem, respectivamente, são entradas obrigatórias usadas para localizar o formulário na biblioteca de formulários .</span><span class="sxs-lookup"><span data-stu-id="c2db4-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="c2db4-111">As entradas restantes são opcionais.</span><span class="sxs-lookup"><span data-stu-id="c2db4-111">The remaining entries are optional.</span></span> <span data-ttu-id="c2db4-112">O formato da seção **[Descrição]** é:</span><span class="sxs-lookup"><span data-stu-id="c2db4-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="c2db4-113">\*\*Descrição \*\* =  _Cadeia de caracteres_ MessageClass</span><span class="sxs-lookup"><span data-stu-id="c2db4-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="c2db4-114">\*\*\*\* =  _GUID_ do CLSID</span><span class="sxs-lookup"><span data-stu-id="c2db4-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="c2db4-115">**DisplayName** =  __ disjogadostring</span><span class="sxs-lookup"><span data-stu-id="c2db4-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="c2db4-116">\*\*\*\* =  _Caminho_ de SmallIcon</span><span class="sxs-lookup"><span data-stu-id="c2db4-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="c2db4-117">\*\*\*\* =  _Caminho_ LargeIcon</span><span class="sxs-lookup"><span data-stu-id="c2db4-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="c2db4-118">As entradas opcionais são:</span><span class="sxs-lookup"><span data-stu-id="c2db4-118">Optional entries are:</span></span>
  
 <span data-ttu-id="c2db4-119">\*\*\*\* =  _Cadeia de caracteres exibida_ na categoria</span><span class="sxs-lookup"><span data-stu-id="c2db4-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="c2db4-120">\*\*\*\* =  _Cadeia de caracteres exibida_ na subcategoria</span><span class="sxs-lookup"><span data-stu-id="c2db4-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="c2db4-121">\*\*\*\* =  _Cadeia de caracteres exibida_ de comentário</span><span class="sxs-lookup"><span data-stu-id="c2db4-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="c2db4-122">\*\*\*\* =  _Cadeia de caracteres exibida_ do proprietário</span><span class="sxs-lookup"><span data-stu-id="c2db4-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="c2db4-123">\*\*\*\* =  _Cadeia de caracteres exibida_ de número</span><span class="sxs-lookup"><span data-stu-id="c2db4-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="c2db4-124">\*\*\*\* =  _Inteiro_ de versão</span><span class="sxs-lookup"><span data-stu-id="c2db4-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="c2db4-125">\*\*\*\* =  _Cadeia de caracteres_ de localidade</span><span class="sxs-lookup"><span data-stu-id="c2db4-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="c2db4-126">\*\*\*\* =  _Inteiro_ oculto</span><span class="sxs-lookup"><span data-stu-id="c2db4-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="c2db4-127">\*\*\*\* =  _Cadeia de caracteres_ DesignerToolName</span><span class="sxs-lookup"><span data-stu-id="c2db4-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="c2db4-128">**DesignerToolGuid** =  _CLSID_</span><span class="sxs-lookup"><span data-stu-id="c2db4-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="c2db4-129">**DesignerRuntimeGuid** =  _CLSID_</span><span class="sxs-lookup"><span data-stu-id="c2db4-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="c2db4-130">**ComposeInFolder** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="c2db4-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="c2db4-131">\*\*\*\* =  _Cadeia de caracteres_ ComposeCommand</span><span class="sxs-lookup"><span data-stu-id="c2db4-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="c2db4-132">As entradas de **categoria** e de subcategoria são usadas por instaladores de formulário para configurar a categorização padrão de formulários dentro da interface do usuário do aplicativo cliente. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c2db4-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="c2db4-133">Por exemplo, uma hierarquia pode ser configurada onde "Help Desk" é a categoria e "software" e "hardware" foram as subcategorias.</span><span class="sxs-lookup"><span data-stu-id="c2db4-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="c2db4-134">Essa categorização pode ser usada por aplicativos de visualização para exibir mensagens de uma maneira mais organizada.</span><span class="sxs-lookup"><span data-stu-id="c2db4-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="c2db4-135">As entradas de **Comentário**, **proprietário**e **número** são todas as cadeias de caracteres de comentário que aparecem na interface de usuário do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="c2db4-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="c2db4-136">São propriedades específicas de formulário que podem ser usadas com a critério do desenvolvedor de formulários.</span><span class="sxs-lookup"><span data-stu-id="c2db4-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="c2db4-137">Por exemplo, a entrada de **Comentário** pode ser usada para indicar a finalidade do formulário, a entrada do **proprietário** usada para indicar a pessoa ou organização responsável por manter o formulário e o número usado para controlar a versão diferente do formulário.</span><span class="sxs-lookup"><span data-stu-id="c2db4-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="c2db4-138">Para a entrada de **Comentário** , podem ser incluídas até dez linhas de comentários.</span><span class="sxs-lookup"><span data-stu-id="c2db4-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="c2db4-139">A primeira linha de comentários usa a palavra "Comment" como a chave, a segunda linha de comentários usa "Comment1" como a chave e assim por diante por meio de "Comment9".</span><span class="sxs-lookup"><span data-stu-id="c2db4-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="c2db4-140">As entradas **LargeIcon** e **SmallIcon** são usadas para especificar o caminho dos recursos de ícone usados para exibir ícones na interface de usuário do aplicativo cliente, geralmente é para linhas de tabela que incluem o **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c2db4-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="c2db4-141">Os nomes de arquivos de ícone podem ser especificados como caminhos relativos ao diretório onde o arquivo de configuração de formulário está instalado.</span><span class="sxs-lookup"><span data-stu-id="c2db4-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="c2db4-142">A entrada de **versão** é usada para indicar o número de versão do formulário.</span><span class="sxs-lookup"><span data-stu-id="c2db4-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="c2db4-143">**Locale** é o identificador de idioma de três letras da biblioteca de formulários de destino.</span><span class="sxs-lookup"><span data-stu-id="c2db4-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="c2db4-144">Uma lista desses identificadores pode ser encontrada na _referência do programador do Win32_.</span><span class="sxs-lookup"><span data-stu-id="c2db4-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="c2db4-145">A entrada **Hidden** indica se o formulário deve ser exibido na interface de usuário de um provedor de biblioteca de formulários: 1 indica que o arquivo está oculto e 0 indica que o formulário está visível.</span><span class="sxs-lookup"><span data-stu-id="c2db4-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="c2db4-146">Um exemplo de arquivo de configuração de formulário é mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="c2db4-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="c2db4-147">A entrada **ComposeInFolder** controla se o formulário foi projetado para ser colocado na pasta atual ou na caixa de entrada do usuário quando o usuário salvar a mensagem ao redigi-la: 1 indica que o formulário deve ir na pasta atual e 0 indica que ele deve Vá na caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2db4-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="c2db4-148">A entrada **ComposeCommand** é a cadeia de caracteres a ser colocada no menu de redação do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="c2db4-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="c2db4-149">Se isso não for especificado, a entrada **DisplayName** será usada.</span><span class="sxs-lookup"><span data-stu-id="c2db4-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


