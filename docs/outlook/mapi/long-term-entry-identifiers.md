---
title: Long-Term de entrada de usuário
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
# <a name="long-term-entry-identifiers"></a>Long-Term de entrada de usuário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um identificador de entrada de longo prazo é atribuído por um provedor de serviços a um objeto quando um objeto exige um identificador com um tempo de vida prolongado. Os identificadores de entrada de longo prazo são sempre válidos por semanas ou meses e podem ser válidos em outras estações de trabalho, dependendo do provedor. Os identificadores de longo prazo criados pelos provedores de livro de endereços para destinatários personalizados são universalmente válidos. 
  
Identificadores de entrada de longo prazo são atribuídos a armazenamentos de mensagens, pastas, mensagens, contêineres de agendamento de endereços, usuários de mensagens e listas de distribuição. Quando os aplicativos cliente chamam o método [IMAPIProp::GetProps](imapiprop-getprops.md) desses objetos, é sempre um identificador de entrada de longo prazo que é retornado. 
  
Os identificadores de entrada de longo prazo devem ser exclusivos em todos os armazenamentos de mensagens no perfil ativo; portanto, quando uma mensagem ou pasta é copiada de um armazenamento de mensagens para outro, deve ser atribuído um novo identificador de entrada. Quando um objeto de armazenamento de mensagens é movido, o provedor de armazenamento de mensagens que implementa a movimentação determina se o identificador de entrada original permanecerá válido. Alguns provedores de serviços atribuem novos identificadores de entrada a objetos movidos; outras não fazem isso. Se houver uma alteração, o novo identificador de entrada será incluído nas informações passadas aos clientes quando eles são notificados sobre a movimentação. 
  
Normalmente, os provedores de armazenamento de mensagens implementam o seguinte comportamento ao mover pastas:
  
- Quando uma pasta é movida de um armazenamento de mensagens para outro armazenamento de um tipo diferente, o identificador de entrada tem garantia de alteração.
    
- Quando uma pasta é movida de um armazenamento de mensagens para outro do mesmo tipo, o identificador de entrada quase sempre muda.
    
- Quando uma pasta é movida para outro local dentro do mesmo armazenamento de mensagens, o identificador de entrada pode ou não mudar, dependendo do provedor do armazenamento de mensagens.
    
Renomear uma pasta sem alterar sua pasta pai geralmente não faz com que o identificador de entrada mude. 
  
## <a name="see-also"></a>Confira também



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

