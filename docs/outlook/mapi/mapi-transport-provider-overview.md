---
title: Visão geral do provedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404572"
---
# <a name="mapi-transport-provider-overview"></a>Visão geral do provedor de transporte MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de transporte lidam com a transmissão e recepção de mensagens e implementam a segurança, se necessário. Eles também cuidam de todas as tarefas de pré-processamento e de pré-processamento necessárias. Normalmente, há um provedor de transporte para cada sistema de mensagens ativas.
  
Os aplicativos cliente se comunicam com o provedor de transporte por meio de um provedor de repositório de mensagens. 
  
Os provedores de transporte se registram com MAPI para lidar com um ou mais tipos específicos de entradas de destinatário. Quando uma mensagem está pronta para ser enviada, o MAPI deve determinar qual provedor de transporte deve lidar com a transmissão. Dependendo do tipo de destinatário, o MAPI pode até chamar mais de um provedor de transporte. Se um provedor de transporte não disponível for o único que pode lidar com o destinatário, a transmissão da mensagem será adiada até que uma conexão com esse provedor possa ser restabelecida.
  
Alguns sistemas de mensagens são sistemas seguros; todos os usuários em potencial precisam inserir um conjunto de credenciais válidas antes que o acesso seja permitido. O MAPI impede o acesso não autorizado a esses sistemas de mensagens seguras, fazendo com que o provedor de transporte valide credenciais no momento do logon. 
  

