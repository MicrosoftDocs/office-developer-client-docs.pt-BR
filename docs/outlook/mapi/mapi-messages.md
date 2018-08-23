---
title: Mensagens MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cf7876dacac40420fdedb8b6f55c99efcf56c4f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579932"
---
# <a name="mapi-messages"></a>Mensagens MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As mensagens são objetos MAPI que são transmitidos de aplicativo de um cliente para outro por meio do spooler MAPI e os provedores de serviços por meio de um sistema de mensagens. Quase todos os componentes nas MAPI funciona com mensagens. Clientes permitem aos usuários criar, salvar, enviar e excluir mensagens Além disso, para copiar e movê-los de uma pasta para outro. Provedores de armazenamento de mensagem são responsáveis para gerenciamento de mensagem e de entrega de mensagens para o spooler MAPI ou um provedor de transporte. O MAPI spooler move as mensagens para um provedor de transporte apropriado, enquanto os provedores de transporte lidar com a entrega e o recebimento de mensagens de e para um sistema de mensagens e definir a mensagem e destinatário propriedades de opção. Provedores de catálogo de endereços funcionam indiretamente com mensagens, com suporte para propriedades que descrevem os destinatários da mensagem.
  
As mensagens são armazenadas em pastas ao longo de um armazenamento de mensagens, normalmente pastas criadas na pasta raiz interpessoais mensagens (IPM). Mensagens geralmente são armazenadas no mesmo nível de caixa de entrada IPM standard, itens enviados, itens excluídos e pastas de caixa de saída ou em níveis inferiores na hierarquia. No entanto, as mensagens também podem ser armazenadas fora a subárvore IPM.
  
Mensagens criadas na subárvore IPM standard têm conteúdo padrão (ou seja, conteúdo que estão visível para o usuário de um aplicativo cliente). Anotações e relatórios são exemplos de mensagens que têm o conteúdo padrão. Mensagens também podem ser criadas com conteúdo associado ou conteúdo que não é visível no cliente típico. Pastas dão suporte a duas tabelas diferentes de conteúdo para armazenar os diferentes tipos de mensagens: um padrão de conteúdo da tabela de mensagens padrão e uma tabela de conteúdo associado para mensagens associadas. Porque o MAPI não definir padrões para o conteúdo das mensagens associadas, eles podem conter informações arbitrárias. 
  
Uma mensagem pode ter dados adicionais — na forma de um arquivo, outra mensagem ou um objeto OLE — associado a ela. Esses dados adicionais, que são chamados um anexo, aparecem como um ícone ou, para uma mensagem RTF, como um metarquivo no texto da mensagem. Uma mensagem pode ter zero, um ou muitos anexos. Anexos sempre são transmitidos com a mensagem.
  
Uma mensagem que é transmitida tem um ou mais destinatários (endereços que estão associados um determinado sistema de mensagens). Alguns destinatários são entradas em um recipiente que pertence a um provedor de catálogo de endereços no perfil atual; outros destinatários são criados apenas para transmitir a mensagem. Porque os destinatários e anexos precisam ser acessados por meio da mensagem com a qual estão associadas, os destinatários de uma mensagem e anexos são conhecidos como seus subobjetos. 
  
Provedores de armazenamento de mensagem oferecem suporte a mensagens, anexos e destinatários por meio dos métodos em três interfaces: 
  
|**Interface**|**Descrição**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Gerencia a destinatários e anexos, envia mensagens, define o status de leitura.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Cria, copia, move as mensagens e subpastas e gerencia o status da mensagem.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Gerencia as propriedades de anexo.  <br/> |
   
## <a name="see-also"></a>Confira também



[Desenvolvimento de aplicativos MAPI](mapi-application-development.md)

