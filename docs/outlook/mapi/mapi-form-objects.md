---
title: Objetos de formulário MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5a7c6c575f277a91a18f0d834e26d3d376613fba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404782"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="0c145-103">Objetos de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="0c145-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="0c145-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c145-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c145-105">Os objetos de formulário são criados dinamicamente por servidores de formulário para exibir mensagens específicas e permitir que os usuários interajam com eles.</span><span class="sxs-lookup"><span data-stu-id="0c145-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="0c145-106">Um objeto de formulário é, portanto, uma instaciação da classe derivada de [IMAPIForm](imapiformiunknown.md) implementada pelo servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="0c145-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="0c145-107">Quando um aplicativo cliente abre uma mensagem, o servidor de formulário para essa classe de mensagem cria um objeto de formulário para manipular a mensagem.</span><span class="sxs-lookup"><span data-stu-id="0c145-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="0c145-108">Em seguida, o objeto de formulário cria sua interface e exibe as propriedades da mensagem nele.</span><span class="sxs-lookup"><span data-stu-id="0c145-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="0c145-109">O objeto de formulário e sua interface persistem até que o usuário o feche.</span><span class="sxs-lookup"><span data-stu-id="0c145-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="0c145-110">O objeto de formulário lida com quaisquer alterações nos valores das propriedades da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0c145-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="0c145-111">Além disso, as interfaces de formulário MAPI definem um mecanismo pelo qual um objeto de formulário pode carregar e exibir uma série de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0c145-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="0c145-112">Esse é um mecanismo de eficiência, pois evita destruição e criação de objetos de mensagem desnecessários e suas interfaces.</span><span class="sxs-lookup"><span data-stu-id="0c145-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="0c145-113">Quando solicitado pelo cliente de mensagens a carregar uma mensagem diferente, o objeto de formulário deve salvar quaisquer alterações nas propriedades da mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="0c145-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="0c145-114">Para obter informações sobre a perspectiva de objetos de formulário de um aplicativo cliente, consulte [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0c145-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0c145-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c145-115">See also</span></span>



[<span data-ttu-id="0c145-116">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="0c145-116">MAPI Forms</span></span>](mapi-forms.md)

