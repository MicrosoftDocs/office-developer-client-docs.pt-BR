---
title: Visão geral do provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433154"
---
# <a name="transport-provider-overview"></a>Visão geral do provedor de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de transporte é uma biblioteca de vínculo dinâmico (DLL) que atua como um intermediário entre o subsistema MAPI e um ou mais sistemas de mensagens subjacentes. Um sistema de mensagens é um mecanismo específico pelo qual as mensagens são enviadas e recebidas. Alguns exemplos de sistemas de mensagens são:
  
- Um sistema de arquivos de rede compartilhado no qual o provedor de transporte grava mensagens diretamente.
    
- Uma interface de rede TCP/IP que o provedor de transporte usa para se conectar a um servidor de mensagens.
    
- Um serviço online ao qual os usuários se conectam.
    
- Um sistema de mensagens ou de automação do Office baseado em host.
    
- Um conjunto de chamadas de procedimento remoto para um servidor de mensagens.
    
- Qualquer coisa que possa ser usada para transferir dados de um computador para outro.
    
Uma DLL do provedor de transporte deve estar em conformidade com a interface especificada por MAPI. Como desenvolvedor de provedor de transporte, você implementará essa interface em termos da funcionalidade presente no sistema de mensagens.
  

