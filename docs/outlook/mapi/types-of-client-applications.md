---
title: Tipos de aplicativos cliente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 167710243c61a7226375b88977c94ff4a517c1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417053"
---
# <a name="types-of-client-applications"></a>Tipos de aplicativos cliente

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há principalmente dois tipos de clientes de mensagens: aqueles que tratam de mensagens interpessoais (IPM) e aqueles que lidam com mensagens de comunicação entre processos (IPC). Nesses tipos, os aplicativos clientes de mensagens podem ser categorizados da seguinte maneira:
  
- Pessoa para pessoa
    
- Pessoa para máquina
    
- Máquina para pessoa
    
- Máquina para máquina
    
- Mistura de pessoas e máquinas
    
Os aplicativos de pessoa para pessoa envolvem uma pessoa que inicia a troca de mensagens e outra pessoa respondendo. Essa categoria de aplicativos inclui aplicativos de email tradicionais, bem como trocas mais estruturadas, como roteamento de documentos ou aprovação de despesas.
  
Os aplicativos de pessoa para máquina envolvem uma pessoa que inicia a troca de mensagens e uma máquina respondendo. Esta categoria inclui aplicativos que usam email para, por exemplo, enviar uma consulta de banco de dados ou inscrever-se em uma lista de endereçamento.
  
Os aplicativos de máquina a pessoa envolvem uma máquina que inicia a troca de mensagens e uma pessoa respondendo. Esta categoria inclui aplicativos que distribuem documentos, como News feeds e pesquisas de opinião.
  
Os aplicativos de máquina para máquina envolvem uma máquina que inicia o Exchange de mensagens e uma máquina respondendo. Esta categoria inclui aplicativos como monitoramento de pulsação de link e replicação de diretório e banco de dados.
  
A categoria final, uma mistura de pessoas e máquinas, envolve um cenário mais complexo. Esta categoria inclui aplicativos que não necessariamente transmitem mensagens entre remetentes e destinatários. Em vez disso, eles podem lançá-los diretamente em uma pasta pública ou em um fórum de site da Web suportado por um repositório de mensagens. As mensagens podem ser consumidas por demanda por outros leitores, um administrador ou um agente de software.
  
Se você estiver escrevendo um aplicativo de pessoa para pessoa, um aplicativo de máquina para pessoa ou um aplicativo que publica mensagens em fóruns públicos, projete seu aplicativo para enviar e receber mensagens IPM. Se você estiver escrevendo um aplicativo de pessoa para máquina ou máquina para máquina, ele pode ser projetado para enviar e receber mensagens de IPC. Qualquer aplicativo que exija a interação de um usuário humano deve suportar mensagens IPM. Os aplicativos que envolvem pessoas e máquinas em uma variedade de cenários freqüentemente devem oferecer suporte a mensagens IPM e IPC. A única diferença real entre as duas classes é que as mensagens IPM em um repositório de mensagens são visíveis para os usuários de clientes de mensagens, enquanto as mensagens de IPC geralmente não são visíveis para os usuários do aplicativo cliente. 
  
Em vez de limitar suas mensagens aos recursos fornecidos pelas superclasses MAPI, IPM e IPC, você pode personalizar e aprimorar essas classes criando novas subclasses IPM ou IPC. Criar subclasses de mensagens envolve o inventting novas classes de mensagens que herdam das superclasses. Por exemplo, se o seu aplicativo de pessoa a pessoa é especializado no gerenciamento de relacionamento com o cliente, você pode subclassar a superclasse IPM definindo uma IPM. Classe Contact. Customer e criar propriedades que descrevem um cliente. Além de oferecer suporte a essas propriedades personalizadas, sua IPM. Contact. Customer messages herdará as propriedades suportadas por todas as mensagens IPM.
  

