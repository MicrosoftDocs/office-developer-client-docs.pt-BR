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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356571"
---
# <a name="types-of-tables"></a>Tipos de tabelas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há muitos tipos diferentes de tabelas, cada tipo diferenciado pelas informações apresentadas. As tabelas permitem que aplicativos clientes e provedores de serviços acessem prontamente e manipulem as propriedades importantes de vários tipos de objetos. 
  
Algumas tabelas, como tabelas de conteúdo, fornecem uma maneira alternativa de acessar as propriedades. Por exemplo, um cliente pode recuperar o assunto de uma mensagem — sua propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) — diretamente da mensagem chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps ou por meio da tabela de conteúdo da mensagem. Outras tabelas fornecem a única maneira de acessar as propriedades do objeto. Por exemplo, um cliente não pode acessar a propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) de um anexo chamando **IMAPIProp::** GetProps; deve sempre recuperar a tabela de anexos da mensagem à qual está conectada. **PR_ATTACH_METHOD** é uma coluna obrigatória em todas as tabelas de anexo. 
  
Um modo de exibição de tabela pode ser estático ou dinâmico. Com um modo de exibição de tabela estática, as alterações nos dados subjacentes não fazem com que o modo de exibição seja atualizado. Depois que o modo de exibição tiver sido instanciado, ele não será alterado. Usuários de tabelas estáticas podem ser informados de alterações nos dados por meio de notificações de tabela. Um modo de exibição de tabela dinâmica é atualizado quando são feitas alterações nos dados. Há dois tipos de tabelas dinâmicas: uma que atualiza as colunas de cada linha, mas as linhas permanecem estáticas e uma que atualiza as colunas e as linhas. Esse último tipo de tabela sempre reflete exatamente os dados subjacentes.
  
As tabelas têm um conjunto de colunas padrão, o conjunto mínimo de colunas que um cliente ou provedor de serviços pode esperar ver ao recuperar linhas de uma tabela que ainda não foi afetada por uma chamada imApitable [::](imapitable-setcolumns.md) SetColumns. Os clientes e provedores de serviços podem adicionar ou remover colunas desse conjunto padrão chamando o método setColumns. **** As alterações podem ser feitas de forma estática ou dinâmica, seguindo uma solicitação de cliente. Nem todas as tabelas dão suporte à modificação dinâmica do conjunto de colunas. 
  
As tabelas MAPI e seus implementadores e usuários são:
  
|**Table**|**Implementadores**|
|:-----|:-----|
|Anexo  <br/> |Implementado por provedores de repositório de mensagens. Usado por clientes e provedores de transporte.  <br/> |
|Conteúdos  <br/> |Implementado por repositórios de mensagens e provedores de catálogo de endereços. Usado por clientes.  <br/> |
|Exibir  <br/> |Implementado por MAPI e provedores de serviço. Usado por MAPI e provedores de serviço.  <br/> |
|Hierarquia  <br/> |Implementado por repositórios de mensagens e provedores de catálogo de endereços. Usado por clientes.  <br/> |
|Serviço de mensagens  <br/> |Implementado por MAPI. Usado por clientes.  <br/> |
|Repositório de mensagens  <br/> |Implementado por MAPI. Usado por clientes.  <br/> |
|One-off  <br/> |Implementado por provedores de catálogo de endereços. Usado por MAPI.  <br/> |
|Fila de saída  <br/> |Implementado por provedores de repositório de mensagens. Usado pelo spooler MAPI.  <br/> |
|Perfil  <br/> |Implementado por MAPI. Usado por clientes.  <br/> |
|Provedor  <br/> |Implementado por MAPI. Usado por clientes.  <br/> |
|Pasta receber  <br/> |Implementado por provedores de repositório de mensagens. Usado por clientes.  <br/> |
|Destinatário  <br/> |Implementado por provedores de repositório de mensagens. Usado por clientes e provedores de transporte.  <br/> |
|Status  <br/> |Implementado por MAPI e provedores de serviço. Usado por clientes.  <br/> |
   
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

