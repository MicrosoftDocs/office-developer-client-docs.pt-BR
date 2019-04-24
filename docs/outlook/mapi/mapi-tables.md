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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355830"
---
# <a name="mapi-tables"></a>Tabelas MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela MAPI é um objeto MAPI que é usado para exibir uma coleção de propriedades pertencentes a outros objetos MAPI de um tipo específico. As tabelas MAPI são estruturadas em um formato de linha e coluna com cada linha que representa um objeto e cada coluna representando uma propriedade do objeto. Uma das propriedades normalmente incluídas em cada linha é a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), um identificador que pode ser usado para abrir e modificar o objeto. 
  
Como as linhas contêm valores de propriedade, a recuperação de uma linha de uma tabela é semelhante à obtenção de um conjunto de propriedades diretamente do objeto que a linha representa. Ambas as operações resultam na recuperação de uma matriz de valor de propriedade. A principal diferença está no tratamento da cadeia de caracteres longa e propriedades binárias. Para inclusão em uma tabela, alguns implementadores de tabela truncam essas propriedades para 255 bytes. Quando recuperado diretamente do objeto, o valor completo estará sempre disponível.
  
As tabelas são implementadas por provedores de catálogo de endereços e de repositório de mensagens e por MAPI, dependendo do tipo de tabela e dos objetos dentro dela. Um provedor de repositório de mensagens implementa pastas e uma tabela de conteúdo para cada pasta que inclui informações sobre as mensagens na pasta. Um provedor de catálogo de endereços implementa contêineres de catálogo de endereços e uma tabela de hierarquia que mostra sua organização. O MAPI implementa várias tabelas diferentes, alguns para uso por aplicativos cliente, alguns para uso por provedores de serviços e alguns para uso por ambos. A tabela de status é exclusiva, por fim, o MAPI fornece a tabela, mas as linhas são compostas por contribuições de todos os tipos de provedores de serviço, além do MAPI. 
  
A ilustração a seguir mostra um dos usos frequentes de uma tabela em MAPI: para exibir o conteúdo de uma pasta. À direita está uma exibição de duas mensagens como pode aparecer em um aplicativo cliente de mensagens típico. A exibição contém quatro partes de informações sobre cada mensagem: o remetente, o destinatário, o assunto e o texto da mensagem. Cada informação corresponde a uma propriedade da mensagem.
  
À esquerda está um modo de exibição da tabela de conteúdo que inclui essas duas mensagens. Enquanto a tabela de conteúdo pode ter dez linhas porque a pasta possui dez mensagens, com cada linha contendo muito mais de três colunas, esse modo de exibição em particular é limitado a apenas duas linhas e três colunas.
  
A tabela a seguir mostra as propriedades que compõem o conjunto de colunas para o modo de exibição de tabela.
  
|**Property**|**Descrição**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nome do remetente  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Data e hora em que a mensagem foi enviada  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Linha de assunto da mensagem  <br/> |
   
Observe que o conjunto de propriedades exibidas na mensagem não é igual ao conjunto de colunas exibidas na tabela. O implementador da tabela, neste caso, um provedor de repositório de mensagens, fornece um conjunto padrão de colunas em uma ordem padrão. O cliente pode modificar esse conjunto de colunas, solicitar colunas adicionais ou rejeitar as padrões, e solicitar que eles sejam solicitados de forma específica. O cliente também pode ordenar as linhas classificadas de acordo com o valor de uma ou mais colunas.
  
**Using a table to display folder contents**
  
![Usando uma tabela para exibir o conteúdo da pasta] (media/amapi_54.gif "Usando uma tabela para exibir o conteúdo da pasta")
  
Há duas interfaces para trabalhar com tabelas:
  
- [IMAPITable: IUnknown](imapitableiunknown.md) fornece aos clientes e aos provedores de serviços um modo de exibição somente leitura dos dados subjacentes da tabela, permitindo que eles exibam e alterem apenas a apresentação. Vários usuários podem acessar os mesmos dados simultaneamente com imApitable. **** **** IMAPITable é implementado por MAPI e por provedores de serviço. 
    
- [ITableData: IUnknown](itabledataiunknown.md) fornece aos clientes e aos provedores de serviço acesso de leitura/gravação aos dados subjacentes da tabela, permitindo que eles façam alterações permanentes. **** IMAPITable é implementado por MAPI e usado principalmente por provedores de serviço que o acessam chamando a função [CreateTable](createtable.md) . A implementação do **ITableData** contém todos os dados da tabela e quaisquer restrições associadas na memória, tornando-a inadequada para uso com tabelas muito grandes. Não há suporte para restrições comPostas e operações complexas, como categorização. 
    
## <a name="see-also"></a>Confira também

- [Conceitos de MAPI](mapi-concepts.md)

