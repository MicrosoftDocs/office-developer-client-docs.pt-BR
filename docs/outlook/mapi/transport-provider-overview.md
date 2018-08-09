---
title: Visão geral do provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 22b9da0cfe70cf499cc6f3a699eabe4aaee25b0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770635"
---
# <a name="transport-provider-overview"></a>Visão geral do provedor de transporte

  
  
**Aplica-se a**: Outlook 
  
Um provedor de transporte é uma biblioteca de vínculo dinâmico (DLL) que atua como um intermediário entre um ou mais sistemas de mensagens subjacentes e o subsistema de MAPI. Um sistema de mensagens é algum mecanismo específico pelo qual as mensagens são enviadas e recebidas. Alguns exemplos de sistemas de mensagens são:
  
- Um sistema de arquivos de rede compartilhado que o provedor de transporte grava as mensagens diretamente.
    
- Uma interface de rede TCP/IP que o provedor de transporte usa para se conectar a um servidor de mensagens.
    
- Um serviço online que os usuários se conectam ao.
    
- Um baseado em host mensagens ou office automation sistema.
    
- Um conjunto de chamadas de procedimento remoto para um servidor de mensagens.
    
- Qualquer coisa que pode ser usado para transferir dados de um computador para outro.
    
Um provedor de transporte DLL deve estar de acordo com a interface especificada por MAPI. Como um desenvolvedor de provedor de transporte, você implementará essa interface em termos de funcionalidade presente no sistema de mensagens.
  

