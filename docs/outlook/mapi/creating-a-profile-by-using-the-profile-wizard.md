---
title: Criar um perfil usando o assistente de perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a93cfb05d8abfffc9f55a7ea48efc3c3451dddbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332932"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>Criar um perfil usando o assistente de perfil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O assistente de perfil é um recurso MAPI que permite que um usuário crie um perfil da maneira mais fácil possível. O assistente de perfil exibe uma série de caixas de diálogo que solicitam que o usuário selecione serviços de mensagens e insira valores para algumas das propriedades de configuração mais essenciais. Para a maioria das outras propriedades obrigatórias, o assistente de perfil usa valores padrão fornecidos. Para invocar o assistente de perfil, chame **LaunchWizard**, uma função com base no protótipo [LAUNCHWIZARDENTRY](launchwizardentry.md) . 
  
O usuário pode adicionar apenas os serviços de mensagens e os provedores de serviços ao novo perfil que oferece suporte ao assistente de perfil. Como cada serviço de mensagens pode exigir que mais propriedades sejam definidas do que o assistente de perfil pode lidar, lembre-se de que se você usar essa abordagem, é possível que um ou mais serviços ou provedores selecionados sejam configurados de forma incompleta.
  

