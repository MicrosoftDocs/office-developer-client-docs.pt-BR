---
title: Identificadores de entrada de longo prazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409220"
---
# <a name="long-term-entry-identifiers"></a>Identificadores de entrada de longo prazo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um identificador de entrada de longo prazo é atribuído por um provedor de serviços a um objeto quando um objeto requer um identificador com uma vida útil prolongada. Os identificadores de entrada de longo prazo são sempre válidos para semanas ou meses e podem ser válidos em outras estações de trabalho, dependendo do provedor. Os identificadores de longo prazo criados por provedores de catálogo de endereços para destinatários personalizados são válidos universalmente. 
  
Os identificadores de entrada de longo prazo são atribuídos a repositórios de mensagens, pastas, mensagens, contêineres de catálogos de endereços, usuários de mensagens e listas de distribuição. Quando os aplicativos cliente chamam o método [IMAPIProp::](imapiprop-getprops.md) GetProps desses objetos, é sempre um identificador de entrada de longo prazo que é retornado. 
  
Os identificadores de entrada de longo prazo devem ser exclusivos em todos os repositórios de mensagens no perfil ativo; Portanto, quando uma mensagem ou pasta é copiada de um repositório de mensagens para outro, ela deve ser atribuída a um novo identificador de entrada. Quando um objeto do repositório de mensagens é movido, o provedor de armazenamento de mensagens que implementa a movimentação determina se o identificador de entrada original permanecerá válido. Alguns provedores de serviços atribuem novos identificadores de entrada a objetos movidos; outros não. Se houver uma alteração, o novo identificador de entrada será incluído nas informações passadas aos clientes quando eles forem notificados sobre a movimentação. 
  
Normalmente, os provedores de repositórios de mensagens implementam o seguinte comportamento quando movem pastas:
  
- Quando uma pasta é movida de um repositório de mensagens para outro repositório de um tipo diferente, o identificador de entrada é garantido para alteração.
    
- Quando uma pasta é movida de um repositório de mensagens para outro repositório do mesmo tipo, o identificador de entrada quase sempre é alterado.
    
- Quando uma pasta é movida para outro local no mesmo repositório de mensagens, o identificador de entrada pode ou não ser alterado, dependendo do provedor de repositório de mensagens.
    
A renomeação de uma pasta sem alterar sua pasta pai normalmente não faz com que o identificador de entrada seja alterado. 
  
## <a name="see-also"></a>Confira também



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

