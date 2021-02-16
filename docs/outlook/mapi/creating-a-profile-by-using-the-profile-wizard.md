---
title: Criando um perfil usando o Assistente de Perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a93cfb05d8abfffc9f55a7ea48efc3c3451dddbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411733"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>Criando um perfil usando o Assistente de Perfil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O Assistente de Perfil é um recurso MAPI que permite que um usuário crie um perfil da maneira mais fácil possível. O Assistente de Perfil exibe uma série de caixas de diálogo que solicitam que o usuário selecione serviços de mensagem e insira valores para algumas das propriedades de configuração mais essenciais. Para a maioria das outras propriedades necessárias, o Assistente de Perfil usa valores padrão fornecidos. Para invocar o Assistente de Perfil, chame **LaunchWizard**, uma função baseada no [protótipo LAUNCHWIZARDENTRY.](launchwizardentry.md) 
  
O usuário pode adicionar apenas esses serviços de mensagem e provedores de serviços ao novo perfil que dá suporte ao Assistente de Perfil. Como cada serviço de mensagens pode exigir que mais propriedades sejam definidas do que o Assistente de Perfil pode manipular, esteja ciente de que, se você usar essa abordagem, é possível que um ou mais dos serviços ou provedores selecionados sejam configurados de forma incompleta.
  

