---
title: Verbos de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: dbd08437dfdd38c3a43cbf12eae8710cc8e3661e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424025"
---
# <a name="form-verbs"></a><span data-ttu-id="1a18d-103">Verbos de formulário</span><span class="sxs-lookup"><span data-stu-id="1a18d-103">Form verbs</span></span>

<span data-ttu-id="1a18d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a18d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a18d-105">A interface de usuário de um formulário normalmente oferece itens de menu ou controles que permitem que os usuários executem algum tipo de ação com o formulário.</span><span class="sxs-lookup"><span data-stu-id="1a18d-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="1a18d-106">É o trabalho do servidor de formulário para lidar com essas ações do usuário.</span><span class="sxs-lookup"><span data-stu-id="1a18d-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="1a18d-107">Essa interface é implementada usando as APIs padrão do Win32; escrever um é como escrever outras interfaces para programas normais do Win32.</span><span class="sxs-lookup"><span data-stu-id="1a18d-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="1a18d-108">Frequentemente, as ações do usuário são associadas a verbos.</span><span class="sxs-lookup"><span data-stu-id="1a18d-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="1a18d-109">Um verbo é o nome de uma ação específica para uma determinada classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1a18d-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="1a18d-110">Por exemplo, **Reply** é um verbo que é implementado por muitos servidores de formulário, cada um deles pode ter uma interpretação diferente desse verbo.</span><span class="sxs-lookup"><span data-stu-id="1a18d-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="1a18d-111">Às vezes, os verbos são chamados de comandos.</span><span class="sxs-lookup"><span data-stu-id="1a18d-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1a18d-112">Nem todos os itens de menu e controles em um formulário correspondem a um verbo.</span><span class="sxs-lookup"><span data-stu-id="1a18d-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="1a18d-113">Por exemplo, um botão **Cancelar** não corresponde a um verbo cancelar no servidor de formulários.</span><span class="sxs-lookup"><span data-stu-id="1a18d-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="1a18d-114">Normalmente, os verbos são associados a ações específicas de uma determinada classe de mensagem ou de um conjunto de classes de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1a18d-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="1a18d-115">Embora diferentes classes de mensagens possam suportar diferentes conjuntos de verbos, todos dão suporte ao mínimo de verbo aberto, que exibe a interface do usuário do formulário e o carrega com os valores de propriedade da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1a18d-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="1a18d-116">Os verbos podem não receber parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1a18d-116">Verbs may take no parameters.</span></span> <span data-ttu-id="1a18d-117">Formulários que exportam comandos com parâmetros variáveis devem usar mecanismos de automação.</span><span class="sxs-lookup"><span data-stu-id="1a18d-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="1a18d-118">Os clientes podem determinar quais verbos são compatíveis com uma determinada classe de mensagens por meio do método [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) , que é implementado pelo Gerenciador de formulários MAPI.</span><span class="sxs-lookup"><span data-stu-id="1a18d-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="1a18d-119">O gerente de formulários obtém essas informações no arquivo de configuração do formulário.</span><span class="sxs-lookup"><span data-stu-id="1a18d-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="1a18d-120">O conjunto de verbos retornado por esse método é usado pelo cliente para mostrar o usuário quais comandos podem ser executados em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="1a18d-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="1a18d-121">Por exemplo, um cliente pode permitir que os usuários cliquem com o botão direito do mouse sobre uma mensagem para exibir verbos aplicáveis a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="1a18d-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a18d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a18d-122">See also</span></span>

- [<span data-ttu-id="1a18d-123">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="1a18d-123">MAPI Forms</span></span>](mapi-forms.md)

