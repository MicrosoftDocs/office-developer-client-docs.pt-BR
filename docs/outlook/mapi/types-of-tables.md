---
title: Tipos de tabelas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1fc4f20-511f-4721-8f09-ec2a5fd0ccb0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 732b3d724c855d978250afff3d05c7f19909a5b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426461"
---
# <a name="types-of-tables"></a>Tipos de tabelas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há vários tipos diferentes de tabelas, cada tipo diferenciado pelas informações que apresenta. Tabelas permitem que aplicativos cliente e provedores de serviços acessem e manipulem prontamente as propriedades importantes de muitos tipos de objetos. 
  
Algumas tabelas, como tabelas de conteúdo, fornecem uma maneira alternativa de acessar propriedades. Por exemplo, um cliente pode recuperar o assunto de uma mensagem — sua propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) — diretamente da mensagem chamando seu método [IMAPIProp::GetProps](imapiprop-getprops.md) ou por meio da tabela de conteúdo da mensagem. Outras tabelas fornecem a única maneira de acessar as propriedades do objeto. Por exemplo, um cliente não pode acessar a propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) do anexo chamando **IMAPIProp::GetProps**; ela deve sempre recuperar a tabela de anexos da mensagem à qual está anexada. **PR_ATTACH_METHOD** é uma coluna necessária em todas as tabelas de anexos. 
  
Um modo de exibição de tabela pode ser estático ou dinâmico. Com uma exibição de tabela estática, as alterações nos dados subjacentes não fazem com que o ponto de vista seja atualizado. Depois que a exibição tiver sido instaliada, ela não será mudada. Os usuários de tabelas estáticas podem ser informados das alterações nos dados por meio de notificações de tabela. Um modo de exibição de tabela dinâmica é atualizado quando são feitas alterações nos dados. Há dois tipos de tabelas dinâmicas: uma que atualiza as colunas de cada linha, mas as linhas permanecem estáticas e uma que atualiza as colunas e linhas. Esse último tipo de tabela sempre reflete exatamente os dados subjacentes.
  
As tabelas têm um conjunto de colunas padrão, o conjunto mínimo de colunas que um cliente ou provedor de serviços pode esperar ver ao recuperar linhas de uma tabela que ainda não foi afetada por uma chamada [IMAPITable::SetColumns.](imapitable-setcolumns.md) Os clientes e provedores de serviços podem adicionar ou remover colunas desse conjunto padrão chamando o **método SetColumns.** As alterações podem ser feitas estaticamente ou dinamicamente, seguindo uma solicitação do cliente. Nem todas as tabelas suportam modificação de conjunto dinâmico de colunas. 
  
As tabelas MAPI e seus implementadores e usuários são:
  
|**Table**|**Implementadores**|
|:-----|:-----|
|Anexo  <br/> |Implementado pelos provedores de armazenamento de mensagens. Usado por clientes e provedores de transporte.  <br/> |
|Conteúdos  <br/> |Implementado por provedores de armazenamento de mensagens e de agendas. Usado por clientes.  <br/> |
|Display  <br/> |Implementado por MAPI e provedores de serviços. Usado por MAPI e provedores de serviços.  <br/> |
|Hierarquia  <br/> |Implementado por provedores de armazenamento de mensagens e de agendas. Usado por clientes.  <br/> |
|Serviço de mensagens  <br/> |Implementado por MAPI. Usado por clientes.  <br/> |
|Armazenamento de mensagens  <br/> |Implementado por MAPI. Usado por clientes.  <br/> |
|Único  <br/> |Implementado pelos provedores de livro de endereços. Usado por MAPI.  <br/> |
|Fila de saída  <br/> |Implementado pelos provedores de armazenamento de mensagens. Usado pelo spooler MAPI.  <br/> |
|Perfil  <br/> |Implementado por MAPI. Usado por clientes.  <br/> |
|Provedor  <br/> |Implementado por MAPI. Usado por clientes.  <br/> |
|Pasta de recebimento  <br/> |Implementado pelos provedores de armazenamento de mensagens. Usado por clientes.  <br/> |
|Destinatário  <br/> |Implementado pelos provedores de armazenamento de mensagens. Usado por clientes e provedores de transporte.  <br/> |
|Status  <br/> |Implementado por MAPI e provedores de serviços. Usado por clientes.  <br/> |
   
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

