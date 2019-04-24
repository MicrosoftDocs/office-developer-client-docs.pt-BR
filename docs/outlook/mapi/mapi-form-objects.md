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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351461"
---
# <a name="mapi-form-objects"></a>Objetos de formulário MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os objetos de formulário são criados dinamicamente por servidores de formulário para exibir mensagens específicas e permitir que os usuários interajam com elas. Um objeto Form é, portanto, uma instanciação da classe derivada de [IMAPIForm](imapiformiunknown.md) que é implementada pelo servidor de formulário. Quando um aplicativo cliente abre uma mensagem, o servidor de formulário dessa classe de mensagem cria um objeto Form para lidar com a mensagem. Em seguida, o objeto Form cria sua interface e exibe as propriedades da mensagem nele. O objeto Form e sua interface persistem até que o usuário o feche. O objeto Form trata quaisquer alterações nos valores das propriedades da mensagem. 
  
Além disso, as interfaces de formulário MAPI definem um mecanismo pelo qual um objeto Form pode carregar e exibir uma série de mensagens. Esse é um mecanismo de eficiência, pois evita a destruição e a criação de objetos de mensagens e de suas interfaces desnecessárias. Quando solicitado pelo cliente de mensagens para carregar uma mensagem diferente, o objeto Form deve salvar as alterações nas propriedades da mensagem atual.
  
Para obter informações sobre a perspectiva de objetos de formulário de um aplicativo cliente, consulte [MAPI Custom Form Objects](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

