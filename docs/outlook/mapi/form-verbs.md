---
title: Verbos de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 27999c141fdeb3e1610213db128bc4ad3d049e6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594095"
---
# <a name="form-verbs"></a><span data-ttu-id="131f0-103">Verbos de formulário</span><span class="sxs-lookup"><span data-stu-id="131f0-103">Form verbs</span></span>

<span data-ttu-id="131f0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="131f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="131f0-105">Normalmente, a interface do usuário de um formulário oferece itens de menu ou controles que permitem que os usuários podem fazer algum tipo de ação com o formulário.</span><span class="sxs-lookup"><span data-stu-id="131f0-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="131f0-106">É a função do servidor de formulário para lidar com essas ações do usuário.</span><span class="sxs-lookup"><span data-stu-id="131f0-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="131f0-107">Esta interface é implementada por meio de APIs do Win32 padrão; escrever um é como escrever outras interfaces para programas de Win32 regulares.</span><span class="sxs-lookup"><span data-stu-id="131f0-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="131f0-108">Muitas vezes, ações do usuário estão associadas a verbos.</span><span class="sxs-lookup"><span data-stu-id="131f0-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="131f0-109">Um verbo é o nome de uma ação que é específico para uma determinada classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="131f0-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="131f0-110">Por exemplo, a **resposta** é um verbo que é implementado por muitos servidores de formulário, cada um deles pode ter uma interpretação diferente da verbo.</span><span class="sxs-lookup"><span data-stu-id="131f0-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="131f0-111">Verbos às vezes são referidos como comandos.</span><span class="sxs-lookup"><span data-stu-id="131f0-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="131f0-112">Nem todos os itens de menu e controles em um formulário correspondem a um verbo.</span><span class="sxs-lookup"><span data-stu-id="131f0-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="131f0-113">Por exemplo, um botão **Cancelar** não corresponde a um verbo Cancelar dentro do servidor do formulário.</span><span class="sxs-lookup"><span data-stu-id="131f0-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="131f0-114">Geralmente, os verbos estão associados a ações que são específicas para uma classe de mensagem específica ou um conjunto de classes de mensagem.</span><span class="sxs-lookup"><span data-stu-id="131f0-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="131f0-115">Embora as classes de mensagem diferente podem oferecer suporte a diferentes conjuntos de verbos, todos oferecem suporte pelo menos um verbo Open, que exibe a interface do usuário do formulário e o carrega com valores de propriedade da mensagem.</span><span class="sxs-lookup"><span data-stu-id="131f0-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="131f0-116">Verbos podem levar sem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="131f0-116">Verbs may take no parameters.</span></span> <span data-ttu-id="131f0-117">Formulários que exportam comandos com parâmetros variáveis devem usar os mecanismos de automação.</span><span class="sxs-lookup"><span data-stu-id="131f0-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="131f0-118">Clientes podem determinar quais verbos são suportados por uma classe de mensagem específica por meio do método [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) , que é implementado pelo gerente de formulário de MAPI.</span><span class="sxs-lookup"><span data-stu-id="131f0-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="131f0-119">O gerente do formulário obtém essas informações do arquivo de configuração do formulário.</span><span class="sxs-lookup"><span data-stu-id="131f0-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="131f0-120">O conjunto de acordo com o verbo retornado por esse método é usado pelo cliente para mostrar o usuário os comandos que podem ser executados em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="131f0-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="131f0-121">Por exemplo, um cliente pode permitir que os usuários clique com o botão direito do mouse em uma mensagem para exibir os verbos aplicáveis a mensagem.</span><span class="sxs-lookup"><span data-stu-id="131f0-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="131f0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="131f0-122">See also</span></span>

- [<span data-ttu-id="131f0-123">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="131f0-123">MAPI Forms</span></span>](mapi-forms.md)

