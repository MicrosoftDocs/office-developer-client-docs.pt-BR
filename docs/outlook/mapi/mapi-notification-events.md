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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427952"
---
# <a name="mapi-notification-events"></a>Eventos de notificação MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando os aplicativos cliente se registram para notificação de evento, eles devem especificar um ou mais eventos. Os eventos que eles podem especificar dependem do conjunto de eventos que a fonte de consultoria pretendido suporta. Há dez tipos de notificações nas quais os clientes e provedores de serviços podem se registrar, cada um representado por uma constante. A notificação de objeto de status é uma exceção. Notificação de objeto de status é uma notificação MAPI interna; os clientes não podem se registrar para ele e os provedores de serviços não podem gerá-lo. A tabela a seguir descreve os tipos de eventos e os objetos de origem de consultoria que podem dar suporte a eles. A constante de evento é incluída no tipo de evento.
  
|**Tipo de evento**|**Descrição**|**Avisar objetos de origem**|
|:-----|:-----|:-----|
|Erro crítico ( _fnevCriticalError_)  <br/> |Ocorreu um erro ou evento global, como o desligamento de uma sessão em andamento.  <br/> |Sessão, todos os tipos de objetos de armazenamento de mensagens e de address book, tabela, status  <br/> |
|Objeto modificado ( _fnevObjectModified_)  <br/> |Um objeto MAPI foi alterado.  <br/> |Pastas, mensagens, todos os tipos de objetos do address book  <br/> |
|Objeto criado ( _fnevObjectCreated_)  <br/> |Um objeto MAPI foi criado.  <br/> |Pastas, mensagens, todos os tipos de objetos do address book  <br/> |
|Objeto movido ( _fnevObjectMoved_)  <br/> |Um objeto MAPI foi movido.  <br/> |Pastas, mensagens, todos os tipos de objetos do address book  <br/> |
|Objeto excluído ( _fnevObjectDeleted_)  <br/> |Um objeto MAPI foi excluído.  <br/> |Pastas, mensagens, todos os tipos de objetos do address book  <br/> |
|Objeto copiado ( _fnevObjectCopied_)  <br/> |Um objeto MAPI foi copiado.  <br/> |Pastas, mensagens, todos os tipos de objetos do address book  <br/> |
|Evento estendido ( _fnevExtended_)  <br/> |Ocorreu um evento interno definido por um provedor de serviços específico.  <br/> |Qualquer objeto de origem de consultoria  <br/> |
|Pesquisa concluída ( _fnevSearchComplete_)  <br/> |Uma operação de pesquisa foi concluída e os resultados da pesquisa estão disponíveis.  <br/> |Folders  <br/> |
|Tabela modificada ( _fnevTableModified_)  <br/> |As informações em um objeto de tabela MAPI foram alteradas.  <br/> |Tabelas  <br/> |
|Novo email ( _fnevNewMail_)  <br/> |Uma mensagem foi entregue e está aguardando para ser processada.  <br/> |Armazenamento de mensagens, pastas  <br/> |
   
O evento estendido é definido por um provedor de serviços para representar um evento que não pode ser coberto por nenhum dos outros eventos predefinidos. Somente clientes que sabem antes de registrar que um provedor de serviços oferece suporte a um evento estendido podem se registrar para esse evento. Não é possível para os clientes determinar sem conhecimento prévio se um provedor de serviços oferece suporte a um evento estendido e, em caso afirmativos, como manipular esse evento quando ele é recebido.
  

