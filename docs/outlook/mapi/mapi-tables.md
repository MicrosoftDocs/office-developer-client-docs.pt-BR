---
title: Tabelas MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7974cae1-10f1-42e9-8be4-c02f2bd86714
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6393de45dbfd130e15a0678f2b6a7f18968dfa03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573212"
---
# <a name="mapi-tables"></a>Tabelas MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela MAPI é um objeto MAPI que é usado para exibir um conjunto de propriedades que pertencem a outros objetos MAPI de um determinado tipo. Tabelas MAPI são estruturadas em um formato de linha e coluna, com cada linha representa um objeto e cada coluna que representa uma propriedade do objeto. Uma das propriedades geralmente são incluídas em cada linha é a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), um identificador que pode ser usado para abrir e modificar o objeto. 
  
Como linhas contêm valores de propriedade, recuperando uma linha de uma tabela é semelhante a obtenção de um conjunto de propriedades diretamente do objeto que representa a linha. As duas operações resultam na recuperação de uma matriz de valores de propriedade. A principal diferença é no tratamento de tempo propriedades de cadeia de caracteres e binário. Para inclusão em uma tabela, alguns implementadores de tabela truncam essas propriedades para 255 bytes. Quando for recuperada diretamente do objeto, o valor completo está sempre disponível.
  
Tabelas são implementadas por provedores de armazenamento de mensagens e o catálogo de endereços e MAPI, dependendo do tipo de tabela e os objetos dentro dela. Um provedor de armazenamento de mensagem implementa pastas e uma tabela de conteúdo para cada pasta que inclui informações sobre as mensagens na pasta. Um provedor de catálogo de endereços implementa contêineres do catálogo de endereços e uma tabela de hierarquia que mostra a sua organização. MAPI implementa várias tabelas diferentes, algumas para uso por aplicativos do cliente, alguns para uso por provedores de serviços e alguns para uso por ambos. A tabela de status é exclusiva MAPI basicamente fornece a tabela, mas as linhas são compostas de contribuições de todos os tipos de provedores de serviço, além de MAPI. 
  
A ilustração a seguir mostra um dos usos frequentes de uma tabela no MAPI: para exibir o conteúdo de uma pasta. No lado direito é uma exibição de duas mensagens podem aparecer em um aplicativo cliente de mensagens típico. A exibição contém quatro partes de informações sobre cada mensagem: o remetente, destinatário, o assunto e o texto da mensagem. Cada informação corresponde a uma propriedade da mensagem.
  
No lado esquerdo é uma exibição da tabela conteúdo que inclui estas duas mensagens. Enquanto a tabela de conteúdo pode ter dez linhas porque a pasta tem dez mensagens, com cada linha que contém mais de três colunas de muitas, este modo de exibição específico é limitado apenas duas linhas e três colunas.
  
A tabela a seguir mostra as propriedades que compõem a coluna definido para o modo de exibição de tabela.
  
|**Propriedade**|**Descrição**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nome do remetente  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Data e hora em que a mensagem foi enviada  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Linha de assunto da mensagem  <br/> |
   
Observe que o conjunto de propriedades exibidas na mensagem não são o mesmo que o conjunto de colunas exibidas na tabela. O implementador da tabela, neste caso uma mensagem repositório provedor, um padrão de suprimentos definido de colunas em uma ordem padrão. O cliente pode modificar este conjunto de coluna, solicitando colunas adicionais ou rejeição padrão aqueles e pedir que eles ser solicitados de uma forma específica. O cliente também pode ordenar as linhas, classificando-os de acordo com o valor de uma ou mais colunas.
  
**Using a table to display folder contents**
  
![Usando uma tabela para exibir o conteúdo da pasta] (media/amapi_54.gif "Usando uma tabela para exibir o conteúdo da pasta")
  
Há duas interfaces para trabalhar com tabelas:
  
- [IMAPITable: IUnknown](imapitableiunknown.md) dá clientes e provedores de serviços de um modo de exibição somente leitura dos dados subjacentes da tabela, permitindo que eles exibir e alterar apenas a apresentação. Vários usuários podem acessar os mesmos dados depois **IMAPITable**. **IMAPITable** é implementada por MAPI e por provedores de serviços. 
    
- [ITableData: IUnknown](itabledataiunknown.md) dá aos clientes e provedores de serviços de leitura/gravação acesso aos dados subjacentes da tabela, permitindo que eles façam alterações permanentes. **IMAPITable** é implementada por MAPI e é usado principalmente pelos provedores de serviço que acessá-lo ao chamar a função [CreateTable](createtable.md) . A implementação de **ITableData** contém todos os dados da tabela e quaisquer associados restrições na memória, tornando-o inadequados para usam com tabelas muito grandes. Compostos restrições e operações complexas, como categorização não são suportados. 
    
## <a name="see-also"></a>Confira também

- [Conceitos MAPI](mapi-concepts.md)

