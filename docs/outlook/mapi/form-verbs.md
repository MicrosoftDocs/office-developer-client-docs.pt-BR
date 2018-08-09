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
ms.openlocfilehash: 1ecc80feec2b0a86f35d03f1ca4f75ea9ff094e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766592"
---
# <a name="form-verbs"></a><span data-ttu-id="85c29-103">Verbos de formulário</span><span class="sxs-lookup"><span data-stu-id="85c29-103">Form verbs</span></span>

<span data-ttu-id="85c29-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85c29-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85c29-105">Normalmente, a interface do usuário de um formulário oferece itens de menu ou controles que permitem que os usuários podem fazer algum tipo de ação com o formulário.</span><span class="sxs-lookup"><span data-stu-id="85c29-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="85c29-106">É a função do servidor de formulário para lidar com essas ações do usuário.</span><span class="sxs-lookup"><span data-stu-id="85c29-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="85c29-107">Esta interface é implementada por meio de APIs do Win32 padrão; escrever um é como escrever outras interfaces para programas de Win32 regulares.</span><span class="sxs-lookup"><span data-stu-id="85c29-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="85c29-108">Muitas vezes, ações do usuário estão associadas a verbos.</span><span class="sxs-lookup"><span data-stu-id="85c29-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="85c29-109">Um verbo é o nome de uma ação que é específico para uma determinada classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="85c29-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="85c29-110">Por exemplo, a **resposta** é um verbo que é implementado por muitos servidores de formulário, cada um deles pode ter uma interpretação diferente da verbo.</span><span class="sxs-lookup"><span data-stu-id="85c29-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="85c29-111">Verbos às vezes são referidos como comandos.</span><span class="sxs-lookup"><span data-stu-id="85c29-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="85c29-112">Nem todos os itens de menu e controles em um formulário correspondem a um verbo.</span><span class="sxs-lookup"><span data-stu-id="85c29-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="85c29-113">Por exemplo, um botão **Cancelar** não corresponde a um verbo Cancelar dentro do servidor do formulário.</span><span class="sxs-lookup"><span data-stu-id="85c29-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="85c29-114">Geralmente, os verbos estão associados a ações que são específicas para uma classe de mensagem específica ou um conjunto de classes de mensagem.</span><span class="sxs-lookup"><span data-stu-id="85c29-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="85c29-115">Embora as classes de mensagem diferente podem oferecer suporte a diferentes conjuntos de verbos, todos oferecem suporte pelo menos um verbo Open, que exibe a interface do usuário do formulário e o carrega com valores de propriedade da mensagem.</span><span class="sxs-lookup"><span data-stu-id="85c29-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="85c29-116">Verbos podem levar sem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="85c29-116">Verbs may take no parameters.</span></span> <span data-ttu-id="85c29-117">Formulários que exportam comandos com parâmetros variáveis devem usar os mecanismos de automação.</span><span class="sxs-lookup"><span data-stu-id="85c29-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="85c29-118">Clientes podem determinar quais verbos são suportados por uma classe de mensagem específica por meio do método [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) , que é implementado pelo gerente de formulário de MAPI.</span><span class="sxs-lookup"><span data-stu-id="85c29-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="85c29-119">O gerente do formulário obtém essas informações do arquivo de configuração do formulário.</span><span class="sxs-lookup"><span data-stu-id="85c29-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="85c29-120">O conjunto de acordo com o verbo retornado por esse método é usado pelo cliente para mostrar o usuário os comandos que podem ser executados em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="85c29-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="85c29-121">Por exemplo, um cliente pode permitir que os usuários clique com o botão direito do mouse em uma mensagem para exibir os verbos aplicáveis a mensagem.</span><span class="sxs-lookup"><span data-stu-id="85c29-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85c29-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="85c29-122">See also</span></span>

- [<span data-ttu-id="85c29-123">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="85c29-123">MAPI Forms</span></span>](mapi-forms.md)

