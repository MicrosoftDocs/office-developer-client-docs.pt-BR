---
title: Tipos de aplicativos cliente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 783b8972c29b80e1005f0d55e00487dd0e2757b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572057"
---
# <a name="types-of-client-applications"></a>Tipos de aplicativos cliente

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Existem basicamente dois tipos de clientes de mensagens: aqueles que lidam com interpessoais mensagens (IPM) e aqueles que trata as mensagens de comunicação entre processos (CPI). Dentre os tipos, aplicativos de cliente de mensagens podem ser categorizados da seguinte maneira:
  
- Entre duas pessoas
    
- Pessoa-para-machine
    
- Máquina-para-pessoa
    
- Máquina para
    
- Mistura de pessoas e máquinas
    
Aplicativos entre duas pessoas envolve uma pessoa iniciando a troca de mensagens e responder de outra pessoa. Esta categoria de aplicativos inclui aplicativos de email tradicional, bem como mais estruturadas trocas como aprovação de roteamento ou despesa do documento.
  
Aplicativos de pessoa-para-machine envolve uma pessoa iniciando a troca de mensagens e uma máquina que estão respondendo. Esta categoria inclui aplicativos que usam o email para, por exemplo, enviar uma consulta de banco de dados ou inscrever-se em uma lista de endereçamento.
  
Aplicativos de máquina-para-pessoa envolve uma máquina iniciando a troca de mensagens e uma pessoa respondendo. Esta categoria inclui aplicativos que distribuem documentos como feeds de notícias e pesquisas de opinião.
  
Aplicativos de máquina para envolve uma máquina iniciando a troca de mensagens e uma máquina que estão respondendo. Esta categoria inclui aplicativos como replicação de diretório e monitoramento e banco de dados de link pulsação.
  
A categoria final, uma mistura de pessoas e máquinas, envolve um cenário mais complexo. Esta categoria inclui aplicativos que não necessariamente transmitir mensagens entre os remetentes e destinatários. Em vez disso, eles podem publicá-los diretamente em uma pasta pública ou para um fórum do site da web compatíveis com um armazenamento de mensagens. As mensagens podem ser consumidas por demanda por outros leitores, um administrador ou um agente de software.
  
Se você estiver escrevendo um aplicativo entre duas pessoas, aplicativos de máquina-para-pessoa ou um aplicativo que envia mensagens para fóruns públicos, projete seu aplicativo para enviar e receber mensagens IPM. Se você estiver escrevendo um pessoa-para-machine ou máquina para o aplicativo, ele pode ser projetado para enviar e receber mensagens de CPI. Qualquer aplicativo que requer a interação de um usuário humano deve oferecer suporte a mensagens IPM. Aplicativos que envolvem pessoas e máquinas em uma variedade de cenários com frequência devem oferecer suporte a mensagens CPI e de IPM. A única diferença entre as duas classes é que mensagens IPM em um repositório de mensagem são visíveis para usuários de clientes de mensagens, enquanto mensagens CPI geralmente não estão visíveis para os usuários do aplicativo cliente. 
  
Em vez de limitando suas mensagens para os recursos fornecidos pelo superclasse MAPI, IPM e CPI, você pode personalizar e aprimorar essas classes criando novas subclasses IPM ou CPI. Criar subclasses mensagem envolve a criação de novas classes de mensagem que herde a superclasse. Por exemplo, se seu aplicativo entre duas pessoas especializada em gerenciamento de relacionamento do cliente, você pode subclasse superclasse IPM definindo uma IPM. Denota de classe e crie propriedades que descrevem um cliente. Além de oferecer suporte a essas propriedades personalizadas, sua IPM. Mensagens de denota herdará as propriedades suportadas por todas as mensagens IPM.
  

