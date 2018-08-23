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
ms.openlocfilehash: f55902190aa22694d89abd4d118a04d62a3c0d5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581913"
---
# <a name="types-of-tables"></a>Tipos de tabelas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há muitos tipos diferentes de tabelas, cada tipo diferenciada pelas informações que ele apresenta. Tabelas permitem que aplicativos cliente e provedores de serviços para prontamente acessar e manipular as propriedades importantes de muitos tipos de objetos. 
  
Algumas tabelas, como tabelas de conteúdo fornecem uma maneira alternativa de acessar propriedades. Por exemplo, um cliente pode recuperar o assunto de uma mensagem — sua propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) — seja diretamente da mensagem chamando seu método [IMAPIProp::GetProps](imapiprop-getprops.md) ou por meio de tabela de conteúdo da mensagem. Outras tabelas fornecem a única maneira de propriedades de objeto do access. Por exemplo, um cliente não pode acessar a propriedade de **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) de um anexo chamando **IMAPIProp::GetProps**; ela sempre deve recuperar a tabela de anexos da mensagem à qual ele está conectado. **PR_ATTACH_METHOD** é uma coluna necessária em todas as tabelas de anexo. 
  
Um modo de exibição de tabela pode ser estáticos ou dinâmicos. Com um modo de exibição de tabela estática, as alterações nos dados subjacentes fazem com que o modo de exibição a ser atualizado. Assim que o modo de exibição tiver sido instanciado, não é alterado. Usuários de tabelas estáticas podem ser informados sobre as alterações de dados por meio de notificações de tabela. Um modo de exibição de tabela dinâmica é atualizado quando são feitas alterações nos dados. Existem dois tipos de tabelas dinâmicas: que atualiza as colunas de cada linha, mas as linhas permaneçam estático e um que atualiza tanto as colunas e linhas. Este último tipo da tabela sempre reflete exatamente os dados subjacentes.
  
As tabelas têm uma coluna padrão definido, o conjunto mínimo de colunas que um provedor de cliente ou serviço pode esperar ao recuperar linhas de uma tabela que ainda não foram afetados por uma [IMAPITable::SetColumns](imapitable-setcolumns.md) chamada. Clientes e provedores de serviços podem adicionar colunas a serem ou remover colunas de definir chamando o método **SetColumns** esse padrão. Alterações podem ser feitas estática ou dinamicamente, após uma solicitação de cliente. Nem todas as tabelas oferecem suporte a modificação do conjunto de coluna dinâmica. 
  
As tabelas MAPI e seus usuários e implementadores são:
  
|**Table**|**Implementadores**|
|:-----|:-----|
|Anexo  <br/> |Implementado por provedores de armazenamento de mensagem. Usado por clientes e provedores de transporte.  <br/> |
|Conteúdo  <br/> |Implementado por mensagem armazenar e provedores de catálogo de endereços. Usado pelos clientes.  <br/> |
|Exibição  <br/> |Implementadas pelo MAPI e provedores de serviços. Usado pelo MAPI e provedores de serviços.  <br/> |
|Hierarquia  <br/> |Implementado por mensagem armazenar e provedores de catálogo de endereços. Usado pelos clientes.  <br/> |
|Serviço de mensagem  <br/> |Implementada por MAPI. Usado pelos clientes.  <br/> |
|Armazenamento de mensagens  <br/> |Implementada por MAPI. Usado pelos clientes.  <br/> |
|One-off  <br/> |Implementado por provedores de catálogo de endereços. Usada pelo MAPI.  <br/> |
|Fila de saída  <br/> |Implementado por provedores de armazenamento de mensagem. Usado pelo spooler MAPI.  <br/> |
|Perfil  <br/> |Implementada por MAPI. Usado pelos clientes.  <br/> |
|Provider  <br/> |Implementada por MAPI. Usado pelos clientes.  <br/> |
|Pasta de recebimento  <br/> |Implementado por provedores de armazenamento de mensagem. Usado pelos clientes.  <br/> |
|Recipient  <br/> |Implementado por provedores de armazenamento de mensagem. Usado por clientes e provedores de transporte.  <br/> |
|Status  <br/> |Implementadas pelo MAPI e provedores de serviços. Usado pelos clientes.  <br/> |
   
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

