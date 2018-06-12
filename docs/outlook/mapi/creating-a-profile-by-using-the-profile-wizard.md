---
title: Criação de um perfil usando o Assistente de perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 29a135264772847a624e1a4558b68bcf822b18df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766349"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>Criação de um perfil usando o Assistente de perfil

  
  
**Aplica-se a**: Outlook 
  
O Assistente de perfil é um recurso MAPI que permite que o usuário crie um perfil da maneira mais fácil de possíveis. O Assistente de perfil exibe uma série de caixas de diálogo que solicita ao usuário selecionar serviços de mensagem e insira valores para algumas das propriedades de configuração mais essenciais. Para a maioria das outras propriedades necessárias, o Assistente de perfil usa valores padrão fornecidos. Para invocar o Assistente de perfil, chame **LaunchWizard**, uma função com base em protótipo [LAUNCHWIZARDENTRY](launchwizardentry.md) . 
  
O usuário pode adicionar apenas os serviços de mensagem e os provedores de serviço para o novo perfil que suportam o Assistente de perfil. Como cada serviço de mensagem pode exigir mais de propriedades a ser definido do Assistente de perfil pode manipular, lembre-se de que se você usar essa abordagem, é possível para uma ou mais dos serviços selecionados ou provedores parcialmente ser configurado.
  

