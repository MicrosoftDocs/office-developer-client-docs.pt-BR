---
title: Identificadores de entrada de longo prazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 589420db48edb348a22f34ce72b948f4d8207ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767781"
---
# <a name="long-term-entry-identifiers"></a>Identificadores de entrada de longo prazo

  
  
**Aplica-se a**: Outlook 
  
Um identificador de entrada de longo prazo é atribuído por um provedor de serviço a um objeto quando um objeto exige um identificador com um tempo de vida prolongado. Identificadores de entrada de longo prazo sempre são válidos por semanas ou meses e podem ser válidos em outras estações de trabalho, dependendo do provedor. Os identificadores de longo prazo criados por provedores de catálogo de endereço para destinatários personalizados são válidos universal. 
  
Identificadores de entrada de longo prazo são atribuídos a armazenamentos de mensagens, pastas, mensagens, contêineres do catálogo de endereços, mensagens usuários e distribuição de listas. Quando os aplicativos cliente chamam o método [IMAPIProp::GetProps](imapiprop-getprops.md) desses objetos, sempre é um identificador de entrada de longo prazo que é retornado. 
  
Identificadores de entrada de longo prazo devem ser exclusivos entre todos os repositórios de mensagem no perfil ativo; Portanto, quando uma mensagem ou a pasta é copiada do repositório de uma mensagem para outro, ele deve ser atribuído um novo identificador de entrada. Quando um objeto de repositório de mensagem é movido, o provedor de armazenamento de mensagem que implementa a movimentação determina se o identificador de entrada original permanecerá válido. Alguns provedores de serviços atribuem novos identificadores de entrada aos objetos movidos; outros não. Se houver uma alteração, o novo identificador de entrada será incluído nas informações do passado para clientes quando eles são notificados sobre a movimentação. 
  
Normalmente, provedores de armazenamento de mensagem implementam o seguinte comportamento quando movem pastas:
  
- Quando uma pasta é movida do repositório de uma mensagem para outro repositório de um tipo diferente, o identificador de entrada é garantido para alterar.
    
- Quando uma pasta é movida do repositório de uma mensagem para outro repositório do mesmo tipo, o identificador de entrada quase sempre é alterado.
    
- Quando uma pasta é movida para outro local dentro do mesmo repositório de mensagem, o identificador de entrada pode ou não pode mudar, dependendo do provedor de armazenamento de mensagem.
    
Renomear uma pasta sem alterar sua pasta pai geralmente não faz com que o identificador de entrada alterar. 
  
## <a name="see-also"></a>Confira também



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

