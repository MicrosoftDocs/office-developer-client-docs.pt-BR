---
title: Eventos de notificação MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0d05672a0b136520216357cc85a6b7a125415759
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345847"
---
# <a name="mapi-notification-events"></a>Eventos de notificação MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando os aplicativos cliente se registram para notificação de eventos, eles devem especificar um ou mais eventos. Os eventos que eles podem especificar dependem do conjunto de eventos que a fonte de aviso pretendida oferece suporte. Há dez tipos de notificações que os clientes e provedores de serviço podem registrar, cada um representado por uma constante. Status o objeto Notification é uma exceção. Status o objeto Notification é uma notificação de MAPI interno; Os clientes não podem se registrar para os provedores de serviços e de ti não podem gerá-lo. A tabela a seguir descreve os tipos de eventos e os objetos de origem de aviso que podem oferecer suporte a eles. A constante do evento é incluída com o tipo de evento.
  
|**Tipo de evento**|**Descrição**|**Informar objetos de origem**|
|:-----|:-----|:-----|
|Erro crítico ( _fnevCriticalError_)  <br/> |Ocorreu um erro ou evento global, como um desligamento de sessão em andamento.  <br/> |Sessão, todos os tipos de repositório de mensagens e objetos do catálogo de endereços, tabela, status  <br/> |
|Objeto modificado ( _fnevObjectModified_)  <br/> |Um objeto MAPI foi alterado.  <br/> |Pastas, mensagens, todos os tipos de objetos do catálogo de endereços  <br/> |
|Objeto criado ( _fnevObjectCreated_)  <br/> |Um objeto MAPI foi criado.  <br/> |Pastas, mensagens, todos os tipos de objetos do catálogo de endereços  <br/> |
|Objeto movido ( _fnevObjectMoved_)  <br/> |Um objeto MAPI foi movido.  <br/> |Pastas, mensagens, todos os tipos de objetos do catálogo de endereços  <br/> |
|Objeto excluído ( _fnevObjectDeleted_)  <br/> |Um objeto MAPI foi excluído.  <br/> |Pastas, mensagens, todos os tipos de objetos do catálogo de endereços  <br/> |
|Objeto copiado ( _fnevObjectCopied_)  <br/> |Um objeto MAPI foi copiado.  <br/> |Pastas, mensagens, todos os tipos de objetos do catálogo de endereços  <br/> |
|Evento estendido ( _fnevExtended_)  <br/> |Um evento interno definido por um determinado provedor de serviços ocorreu.  <br/> |Qualquer objeto de origem de aviso  <br/> |
|Pesquisa concluída ( _fnevSearchComplete_)  <br/> |Uma operação de pesquisa foi concluída e os resultados da pesquisa estão disponíveis.  <br/> |Pastas  <br/> |
|Tabela modificada ( _fnevTableModified_)  <br/> |As informações em um objeto de tabela MAPI foram alteradas.  <br/> |Tabelas  <br/> |
|Nova mensagem de email ( _fnevNewMail_)  <br/> |Uma mensagem foi entregue e está aguardando para ser processada.  <br/> |Repositório de mensagens, pastas  <br/> |
   
O evento estendido é definido por um provedor de serviços para representar um evento que não pode ser coberto por nenhum dos outros eventos predefinidos. Somente os clientes que conhecem antes eles se registram que um provedor de serviços suporta um evento estendido pode se registrar para esse evento. Não é possível que os clientes determinem sem conhecimento avançado se um provedor de serviços oferecer suporte a um evento estendido e, em caso afirmativo, como lidar com esse evento quando ele for recebido.
  

