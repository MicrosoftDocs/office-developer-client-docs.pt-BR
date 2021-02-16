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
ms.openlocfilehash: f1d1895cc6f9e65929781cb0e966873d2bce197c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423374"
---
# <a name="mapi-messages"></a>Mensagens MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As mensagens são objetos MAPI transmitidos de um aplicativo cliente para outro por meio do spooler MAPI e provedores de serviços por meio de um sistema de mensagens. Quase todos os componentes de MAPI funcionam com mensagens. Os clientes permitem que os usuários criem, salvem, enviem e excluam mensagens, além de copiá-las e movê-las de uma pasta para outra. Os provedores de armazenamento de mensagens são responsáveis pelo gerenciamento de mensagens e pela entrega de mensagens ao spooler MAPI ou a um provedor de transporte. O spooler MAPI move mensagens para um provedor de transporte apropriado, enquanto os provedores de transporte lidam com a entrega e o recebimento de mensagens de e para um sistema de mensagens e definir propriedades de opção de destinatário e mensagem. Os provedores de agendas trabalham indiretamente com mensagens, dando suporte a propriedades que descrevem destinatários de mensagens.
  
As mensagens são armazenadas em pastas ao longo de um armazenamento de mensagens, normalmente pastas criadas na pasta raiz da mensagem interpersonal (IPM). Normalmente, as mensagens são armazenadas no mesmo nível da Caixa de Entrada do IPM padrão, itens enviados, itens excluídos e pastas de caixa de saída ou em níveis inferiores na hierarquia. No entanto, as mensagens também podem ser armazenadas fora da subárvore do IPM.
  
As mensagens criadas na subárvore IPM padrão têm conteúdo padrão (ou seja, conteúdo visível para o usuário de um aplicativo cliente). Notas e relatórios são exemplos de mensagens com conteúdo padrão. As mensagens também podem ser criadas com conteúdo associado ou conteúdo que não está visível no cliente típico. As pastas suportam dois diferentes índices de conteúdo para conter os diferentes tipos de mensagens: uma tabela de conteúdo padrão para mensagens padrão e uma tabela de conteúdo associada para mensagens associadas. Como o MAPI não configura padrões para o conteúdo de mensagens associadas, eles podem conter informações arbitrárias. 
  
Uma mensagem pode ter dados adicionais — na forma de um arquivo, outra mensagem ou um objeto OLE — associados a ela. Esses dados adicionais, que são chamados de anexo, são exibidos como um ícone ou, para uma mensagem RTF, como um metadado no texto da mensagem. Uma mensagem pode ter zero, um ou muitos anexos. Os anexos são sempre transmitidos com a mensagem.
  
Uma mensagem transmitida tem um ou mais destinatários (endereços associados a um sistema de mensagens específico). Alguns destinatários são entradas em um contêiner que pertence a um provedor de agendas no perfil atual; outros destinatários são criados apenas para transmitir a mensagem. Como os destinatários e anexos devem ser acessados por meio da mensagem à qual estão associados, os destinatários e anexos de uma mensagem são conhecidos como seus subobjetos. 
  
Provedores de armazenamento de mensagens suportam mensagens, anexos e destinatários por meio de métodos em três interfaces: 
  
|**Interface**|**Descrição**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Gerencia anexos e destinatários, envia mensagens, define o status de leitura.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Cria, copia e move mensagens e subpastas e gerencia o status da mensagem.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Gerencia propriedades de anexo.  <br/> |
   
## <a name="see-also"></a>Confira também



[Desenvolvimento de aplicativos MAPI](mapi-application-development.md)

