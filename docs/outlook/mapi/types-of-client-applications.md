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
  
Há principalmente dois tipos de clientes de mensagens: aqueles que lidam com mensagens interpersonalas (IPM) e aqueles que lidam com mensagens de comunicação entre processos (IPC). Dentro desses tipos, os aplicativos cliente de mensagens podem ser categorizados da seguinte forma:
  
- Pessoa para pessoa
    
- Pessoa para computador
    
- Computador para pessoa
    
- Máquina para computador
    
- Combinação de pessoas e máquinas
    
Aplicativos de pessoa para pessoa envolvem uma pessoa que inicia a troca de mensagens e outra pessoa responde. Essa categoria de aplicativos inclui aplicativos de email tradicionais, bem como trocas mais estruturadas, como roteamento de documentos ou aprovação de despesas.
  
Aplicativos de pessoa para máquina envolvem uma pessoa iniciando a troca de mensagens e um computador respondendo. Essa categoria inclui aplicativos que usam email para, por exemplo, enviar uma consulta de banco de dados ou assinar uma lista de correspondência.
  
Os aplicativos de computador para pessoa envolvem um computador que inicia a troca de mensagens e uma pessoa responde. Essa categoria inclui aplicativos que distribuem documentos como feeds de notícias e pesquisas de opinião.
  
Aplicativos de máquina para máquina envolvem um computador que inicia a troca de mensagens e uma máquina responde. Essa categoria inclui aplicativos como monitoramento de pulsação de link e replicação de diretório e banco de dados.
  
A categoria final, uma mistura de pessoas e máquinas, envolve um cenário mais complexo. Essa categoria inclui aplicativos que não transmitem necessariamente mensagens entre os destinatários e os destinatários. Em vez disso, eles podem postá-los diretamente em uma pasta pública ou em um fórum de site com suporte em um armazenamento de mensagens. As mensagens podem ser consumidas sob demanda por outros leitores, um administrador ou um agente de software.
  
Se você estiver escrevendo um aplicativo de pessoa para pessoa, um aplicativo de computador para pessoa ou um aplicativo que posta mensagens em fóruns públicos, projete seu aplicativo para enviar e receber mensagens IPM. Se você estiver escrevendo um aplicativo de pessoa para máquina ou máquina para máquina, ele poderá ser projetado para enviar e receber mensagens IPC. Qualquer aplicativo que exija a interação de um usuário humano deve suportar mensagens IPM. Aplicativos que envolvem pessoas e máquinas em uma variedade de cenários geralmente devem dar suporte a mensagens IPM e IPC. A única diferença real entre as duas classes é que as mensagens IPM em um armazenamento de mensagens ficam visíveis para os usuários de clientes de mensagens, enquanto as mensagens IPC geralmente não são visíveis para os usuários do aplicativo cliente. 
  
Em vez de limitar suas mensagens aos recursos fornecidos pelas superclasses MAPI, IPM e IPC, você pode personalizar e aprimorar essas classes criando novas subclasses IPM ou IPC. Criar subclasses de mensagem envolve a criação de novas classes de mensagens que herdam das superclasses. Por exemplo, se seu aplicativo de pessoa para pessoa for especializado no gerenciamento de relacionamento com o cliente, você poderá subclasse a superclasse do IPM definindo um IPM. Classe Contact.Customer e criar propriedades que descrevem um cliente. Além de dar suporte a essas propriedades personalizadas, seu IPM. As mensagens Contact.Customer herdarão as propriedades suportadas por todas as mensagens IPM.
  

