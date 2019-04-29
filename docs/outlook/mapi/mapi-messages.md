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
  
As mensagens são objetos MAPI que são transmitidos de um aplicativo cliente para outro através do spooler MAPI e dos provedores de serviço por meio de um sistema de mensagens. Quase todos os componentes em MAPI funcionam com mensagens. Os clientes permitem que os usuários criem, salvem, enviem e excluam mensagens, além de copiá-los e movê-los de uma pasta para outra. Os provedores de repositório de mensagens são responsáveis pelo gerenciamento de mensagens e pelo envio de mensagens para o spooler MAPI ou um provedor de transporte. O spooler MAPI move mensagens para um provedor de transporte apropriado, enquanto os provedores de transporte lidam com a entrega e o recebimento de mensagens de e para um sistema de mensagens e definem as propriedades de opção de destinatário e de mensagem. Os provedores de catálogo de endereços trabalham indiretamente com mensagens, oferecendo suporte a propriedades que descrevem destinatários de mensagens.
  
As mensagens são armazenadas em pastas em um repositório de mensagens, normalmente pastas criadas na pasta raiz da mensagem interpessoal (IPM). As mensagens geralmente são armazenadas no mesmo nível das pastas de caixa de entrada, itens enviados, itens excluídos e caixa de saída padrão ou em níveis mais baixos na hierarquia. No enTanto, as mensagens também podem ser armazenadas fora da sub-árvore IPM.
  
As mensagens criadas na subárvore IPM padrão têm conteúdo padrão (ou seja, conteúdo que é visível para o usuário de um aplicativo cliente). Observações e relatórios são exemplos de mensagens com conteúdo padrão. As mensagens também podem ser criadas com o conteúdo associado, ou conteúdo que não estão visíveis no cliente típico. As pastas dão suporte a duas tabelas de conteúdo diferentes para armazenar os diferentes tipos de mensagens: uma tabela de conteúdo padrão para mensagens padrão e uma tabela de conteúdo associada para mensagens associadas. Como o MAPI não define padrões para o conteúdo de mensagens associadas, eles podem conter informações arbitrárias. 
  
Uma mensagem pode ter dados adicionais — na forma de um arquivo, de outra mensagem ou de um objeto OLE associado a ele. Esses dados adicionais, que são chamados de anexo, aparecem como um ícone ou, para uma mensagem RTF, como um metarquivo no texto da mensagem. Uma mensagem pode ter zero, um ou muitos anexos. Os anexos são sempre transmitidos com a mensagem.
  
Uma mensagem transmitida tem um ou mais destinatários (endereços associados a um sistema de mensagens específico). Alguns destinatários são entradas em um contêiner que pertence a um provedor de catálogo de endereços no perfil atual; outros destinatários são criados somente para transmitir a mensagem. Como destinatários e anexos devem ser acessados por meio da mensagem à qual estão associados, os destinatários de uma mensagem e os anexos são conhecidos como seus subobjetos. 
  
Os provedores de repositórios de mensagens dão suporte a mensagens, anexos e destinatários por meio de métodos em três interfaces: 
  
|**Interface**|**Descrição**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Gerencia anexos e destinatários, envia mensagens, define o status de leitura.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Cria, copia e move mensagens e subpastas e gerencia o status da mensagem.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Gerencia as propriedades do anexo.  <br/> |
   
## <a name="see-also"></a>Confira também



[Desenvolvimento de aplicativos MAPI](mapi-application-development.md)

