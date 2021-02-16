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
# <a name="mapi-form-objects"></a>Objetos de formulário MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os objetos de formulário são criados dinamicamente por servidores de formulário para exibir mensagens específicas e permitir que os usuários interajam com eles. Um objeto de formulário é, portanto, uma instaciação da classe derivada de [IMAPIForm](imapiformiunknown.md) implementada pelo servidor de formulário. Quando um aplicativo cliente abre uma mensagem, o servidor de formulário para essa classe de mensagem cria um objeto de formulário para manipular a mensagem. Em seguida, o objeto de formulário cria sua interface e exibe as propriedades da mensagem nele. O objeto de formulário e sua interface persistem até que o usuário o feche. O objeto de formulário lida com quaisquer alterações nos valores das propriedades da mensagem. 
  
Além disso, as interfaces de formulário MAPI definem um mecanismo pelo qual um objeto de formulário pode carregar e exibir uma série de mensagens. Esse é um mecanismo de eficiência, pois evita destruição e criação de objetos de mensagem desnecessários e suas interfaces. Quando solicitado pelo cliente de mensagens a carregar uma mensagem diferente, o objeto de formulário deve salvar quaisquer alterações nas propriedades da mensagem atual.
  
Para obter informações sobre a perspectiva de objetos de formulário de um aplicativo cliente, consulte [MAPI Custom Form Objects](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

