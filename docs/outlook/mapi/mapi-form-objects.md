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
ms.openlocfilehash: 0cece598d4ad337e29edb3bb98b302de900e056d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593463"
---
# <a name="mapi-form-objects"></a>Objetos de formulário MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Objetos de formulário são criados dinamicamente pelos servidores de formulário para exibir mensagens específicas e permitir que os usuários interajam com eles. Um objeto form é, portanto, uma instanciação da classe derivada de [IMAPIForm](imapiformiunknown.md) que é implementada pelo servidor de formulário. Quando um aplicativo cliente abre uma mensagem, o servidor de formulário para a classe de mensagem que cria um objeto de formulário para manipular a mensagem. O objeto form sua interface de cria e exibe as propriedades da mensagem nela. O objeto form e sua interface persiste até que o usuário feche. O objeto form lida com todas as alterações feitas os valores das propriedades da mensagem. 
  
Além disso, as interfaces de formulário MAPI definem um mecanismo pelo qual um objeto de formulário pode carregar e exibir uma série de mensagens. Esse é um mecanismo de eficiência, pois evita destruição desnecessária e criação de objetos de mensagem e suas interfaces. Quando solicitado pelo cliente de mensagens para carregar uma mensagem diferente, o objeto de formulário deve salvar quaisquer alterações às propriedades da mensagem atual.
  
Para obter informações sobre a perspectiva de um aplicativo cliente de objetos de formulário, consulte [Objetos de formulário personalizado de MAPI](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

