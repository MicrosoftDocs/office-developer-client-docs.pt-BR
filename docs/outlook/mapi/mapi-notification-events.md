---
title: Eventos de notificação de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 76974c29f1d1efef376e6d23bb0d1f8b3b0d54c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767900"
---
# <a name="mapi-notification-events"></a>Eventos de notificação de MAPI

  
  
**Aplica-se a**: Outlook 
  
Quando os aplicativos cliente se registrar para fins de notificação de evento, eles devem especificar um ou mais eventos. Os eventos que eles podem especificar dependem do conjunto de eventos que suporta a fonte advise pretendido. Existem dez tipos de notificações de provedores de serviços e os clientes podem se inscrever para cada um representado por uma constante. Notificação de status de objeto é uma exceção. Notificação de status de objeto é uma notificação de MAPI interna; clientes não podem registrar para ele e provedores de serviços não é possível gerar a ele. A tabela a seguir descreve os tipos de eventos e os objetos de fonte de advise que ofereça suporte a eles. A constante de evento é incluída com o tipo de evento.
  
|**Tipo de evento**|**Descrição**|**Aviso de objetos source**|
|:-----|:-----|:-----|
|Erro crítico ( _fnevCriticalError_)  <br/> |Um erro global ou evento ocorreu, como um desligamento de sessão em andamento.  <br/> |Sessão, todos os tipos de armazenamento de mensagens e objetos de catálogo de endereços, tabela, status  <br/> |
|Objeto modificado ( _fnevObjectModified_)  <br/> |Um objeto MAPI foi alterado.  <br/> |Pastas, mensagens, todos os tipos de objetos do catálogo de endereços  <br/> |
|Objeto criado ( _fnevObjectCreated_)  <br/> |Um objeto MAPI foi criado.  <br/> |Pastas, mensagens, todos os tipos de objetos do catálogo de endereços  <br/> |
|Objeto movido ( _fnevObjectMoved_)  <br/> |Um objeto MAPI foi movido.  <br/> |Pastas, mensagens, todos os tipos de objetos do catálogo de endereços  <br/> |
|Objeto excluído ( _fnevObjectDeleted_)  <br/> |Um objeto MAPI foi excluído.  <br/> |Pastas, mensagens, todos os tipos de objetos do catálogo de endereços  <br/> |
|Objeto copiado ( _fnevObjectCopied_)  <br/> |Um objeto MAPI foi copiado.  <br/> |Pastas, mensagens, todos os tipos de objetos do catálogo de endereços  <br/> |
|Evento estendido ( _fnevExtended_)  <br/> |Ocorreu um evento interno definido por um provedor de serviço específico.  <br/> |Qualquer objeto de origem advise  <br/> |
|Pesquisa concluída ( _fnevSearchComplete_)  <br/> |Uma operação de pesquisa foi concluída e os resultados da pesquisa estão disponíveis.  <br/> |Folders  <br/> |
|Tabela modificada ( _fnevTableModified_)  <br/> |Informações em um objeto table MAPI foi alterada.  <br/> |Tabelas  <br/> |
|Novo email ( _fnevNewMail_)  <br/> |Uma mensagem foi entregue e está aguardando para serem processados.  <br/> |Armazenamento de mensagens, pastas  <br/> |
   
O evento estendido é definido por um provedor de serviços para representar um evento que não pode ser coberto por qualquer um dos outros eventos predefinidos. Somente os clientes que saber antes de se registram que um provedor de serviços oferece suporte a um evento estendido podem se inscrever para o evento. Não é possível para os clientes determinar sem o conhecimento avançado, se um evento estendido oferece suporte a um provedor de serviços e, em caso afirmativo, como lidar com esse evento quando ele for recebido.
  

