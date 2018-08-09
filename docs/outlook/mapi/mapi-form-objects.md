---
title: Objetos de formulário MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 426d3d5787f4ef8cde2883c5e2eb3699dd664965
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767865"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="bf0e2-103">Objetos de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="bf0e2-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="bf0e2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf0e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf0e2-105">Objetos de formulário são criados dinamicamente pelos servidores de formulário para exibir mensagens específicas e permitir que os usuários interajam com eles.</span><span class="sxs-lookup"><span data-stu-id="bf0e2-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="bf0e2-106">Um objeto form é, portanto, uma instanciação da classe derivada de [IMAPIForm](imapiformiunknown.md) que é implementada pelo servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="bf0e2-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="bf0e2-107">Quando um aplicativo cliente abre uma mensagem, o servidor de formulário para a classe de mensagem que cria um objeto de formulário para manipular a mensagem.</span><span class="sxs-lookup"><span data-stu-id="bf0e2-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="bf0e2-108">O objeto form sua interface de cria e exibe as propriedades da mensagem nela.</span><span class="sxs-lookup"><span data-stu-id="bf0e2-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="bf0e2-109">O objeto form e sua interface persiste até que o usuário feche.</span><span class="sxs-lookup"><span data-stu-id="bf0e2-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="bf0e2-110">O objeto form lida com todas as alterações feitas os valores das propriedades da mensagem.</span><span class="sxs-lookup"><span data-stu-id="bf0e2-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="bf0e2-111">Além disso, as interfaces de formulário MAPI definem um mecanismo pelo qual um objeto de formulário pode carregar e exibir uma série de mensagens.</span><span class="sxs-lookup"><span data-stu-id="bf0e2-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="bf0e2-112">Esse é um mecanismo de eficiência, pois evita destruição desnecessária e criação de objetos de mensagem e suas interfaces.</span><span class="sxs-lookup"><span data-stu-id="bf0e2-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="bf0e2-113">Quando solicitado pelo cliente de mensagens para carregar uma mensagem diferente, o objeto de formulário deve salvar quaisquer alterações às propriedades da mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="bf0e2-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="bf0e2-114">Para obter informações sobre a perspectiva de um aplicativo cliente de objetos de formulário, consulte [Objetos de formulário personalizado de MAPI](mapi-custom-form-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bf0e2-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bf0e2-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf0e2-115">See also</span></span>



[<span data-ttu-id="bf0e2-116">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="bf0e2-116">MAPI Forms</span></span>](mapi-forms.md)

