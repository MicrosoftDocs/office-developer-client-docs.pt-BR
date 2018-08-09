---
title: Visão geral do provedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 11cd1040bb228d789248a89184572b87cd1688ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767974"
---
# <a name="mapi-transport-provider-overview"></a>Visão geral do provedor de transporte MAPI

  
  
**Aplica-se a**: Outlook 
  
Provedores de transporte tratar recepção e transmissão de mensagens e implementam a segurança, se necessário. Eles também cuidam de qualquer pré-processamento necessário e tarefas de pós-processamento. Não há provedor de transporte normalmente uma para cada sistema de mensagens ativas.
  
Aplicativos cliente se comunicar com o provedor de transporte por meio de um provedor de armazenamento de mensagem. 
  
Provedores de transporte registram com MAPI para lidar com um ou mais tipos de entradas de destinatário específicos. Quando uma mensagem está pronta para ser enviada, MAPI deve determinar qual provedor de transporte deve lidar com a transmissão. Dependendo do tipo de destinatário, MAPI, até mesmo, pode chamar após a mais de um provedor de transporte. Se um provedor de transporte indisponível for a única pessoa que pode lidar com o destinatário, a transmissão de mensagens será adiada até que uma conexão com esse provedor pode ser restabelecida.
  
Alguns sistemas de mensagens são sistemas seguros; todos os usuários possíveis precisarão inserir um conjunto de credenciais válidas antes de acesso é permitido. MAPI impede o acesso não autorizado a tais sistemas de mensagens seguros fazendo com que o provedor de transporte validar as credenciais no momento do logon. 
  

