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
ms.openlocfilehash: 840c34a64cd0478be8f208799653b9916f50079d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437081"
---
# <a name="mapi-tables"></a>Tabelas MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela MAPI é um objeto MAPI usado para exibir uma coleção de propriedades pertencentes a outros objetos MAPI de um tipo específico. As tabelas MAPI são estruturadas em um formato de linha e coluna com cada linha representando um objeto e cada coluna representando uma propriedade do objeto. Uma das propriedades geralmente incluídas em cada linha é a **propriedade PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), um identificador que pode ser usado para abrir e modificar o objeto. 
  
Como as linhas contêm valores de propriedade, recuperar uma linha de uma tabela é semelhante a obter um conjunto de propriedades diretamente do objeto que a linha representa. Ambas as operações resultam na recuperação de uma matriz de valores de propriedade. A principal diferença está no tratamento de propriedades binárias e de cadeia de caracteres longas. Para inclusão em uma tabela, alguns implementadores de tabela truncam essas propriedades para 255 bytes. Quando recuperado diretamente do objeto, o valor completo está sempre disponível.
  
As tabelas são implementadas por provedores de armazenamento de endereços e por MAPI, dependendo do tipo de tabela e dos objetos dentro dela. Um provedor de armazenamento de mensagens implementa pastas e uma tabela de conteúdo para cada pasta que inclui informações sobre as mensagens na pasta. Um provedor de agenda implementa contêineres de agendas e uma tabela de hierarquia que mostra sua organização. O MAPI implementa várias tabelas diferentes, algumas para uso por aplicativos cliente, algumas para uso por provedores de serviços e outras para uso por ambos. A tabela de status é exclusiva porque o MAPI fornece a tabela, mas as linhas são compostas por contribuições de todos os tipos de provedores de serviços além de MAPI. 
  
A ilustração a seguir mostra um dos usos frequentes de uma tabela em MAPI: para exibir o conteúdo de uma pasta. À direita há uma exibição de duas mensagens, como pode aparecer em um aplicativo cliente de mensagens típico. A exibição contém quatro partes de informações sobre cada mensagem: o remetente, o destinatário, o assunto e o texto da mensagem. Cada informação corresponde a uma propriedade da mensagem.
  
À esquerda há uma exibição do índice que inclui essas duas mensagens. Enquanto a tabela de conteúdo pode ter dez linhas porque a pasta tem dez mensagens, com cada linha contendo muito mais de três colunas, esse ponto de exibição específico é limitado a apenas duas linhas e três colunas.
  
A tabela a seguir mostra as propriedades que com o conjunto de colunas para o exibição de tabela.
  
|**Propriedade**|**Descrição**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nome do remetente  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Data e hora em que a mensagem foi enviada  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Linha de assunto da mensagem  <br/> |
   
Observe que o conjunto de propriedades exibido na mensagem não é o mesmo que o conjunto de colunas exibido na tabela. O implementador da tabela, neste caso, um provedor de armazenamento de mensagens, fornece um conjunto padrão de colunas em uma ordem padrão. O cliente pode modificar esse conjunto de colunas, solicitar colunas adicionais ou rejeitar as padrão e solicitar que elas sejam ordenadas de uma maneira específica. O cliente também pode ordenar as linhas, ordenando-as de acordo com o valor de uma ou mais colunas.
  
**Using a table to display folder contents**
  
![Usando uma tabela para exibir o conteúdo da pasta]Usando uma tabela para exibir o conteúdo da(media/amapi_54.gif "pasta")
  
Há duas interfaces para trabalhar com tabelas:
  
- [IMAPITable : IUnknown](imapitableiunknown.md) oferece aos clientes e provedores de serviços uma exibição somente leitura dos dados subjacentes da tabela, permitindo que eles vejam e alterem somente a apresentação. Vários usuários podem acessar os mesmos dados simultaneamente com **IMAPITable**. **IMAPITable é** implementado por MAPI e por provedores de serviços. 
    
- [ITableData : IUnknown](itabledataiunknown.md) oferece aos clientes e aos provedores de serviços acesso de leitura/gravação aos dados subjacentes da tabela, permitindo que eles façam alterações permanentes. **IMAPITable** é implementado por MAPI e usado principalmente por provedores de serviços que o acessam chamando a [função CreateTable.](createtable.md) A **implementação ITableData** contém todos os dados da tabela e quaisquer restrições associadas na memória, tornando-a inadequada para uso com tabelas muito grandes. Restrições compostas e operações complexas, como categorização, não são compatíveis. 
    
## <a name="see-also"></a>Confira também

- [Conceitos de MAPI](mapi-concepts.md)

