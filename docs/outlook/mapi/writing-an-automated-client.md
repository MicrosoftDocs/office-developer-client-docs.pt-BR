---
title: Escrevendo um cliente automatizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f9ce3452bbc2d3297cc67168835a9387235746a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439762"
---
# <a name="writing-an-automated-client"></a>Escrevendo um cliente automatizado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um aplicativo cliente automatizado é um aplicativo que é executado sem supervisão, não exibindo nenhuma interface do usuário.
  
 Por padrão, muitos métodos de interface MAPI mostram uma interface do usuário. Todos esses métodos têm sinalizadores que permitem que um cliente permita ou suprime essa exibição. Embora o MAPI espere que os provedores de serviços adcarem esses sinalizadores, há alguns provedores que nem sempre atendem a essas expectativas. Um motivo legítimo para não honrar os sinalizadores é a confiança do provedor de serviços em outro serviço que não permite a supressão da interface do usuário. Se você estiver desenvolvendo um cliente automatizado, preste atenção aos provedores de serviços que está usando e como eles são configurados. Não suponha que todas as suas chamadas para suprimir uma interface do usuário serão bem-sucedidas. 
  
Os clientes automatizados devem ter as informações necessárias disponíveis para a configuração adequada de cada um dos serviços de mensagens no perfil. Há duas maneiras de fornecer informações de configuração no momento do logon:
  
- O provedor de serviços pode recuperar informações do perfil.
    
- O provedor de serviços pode solicitar informações ao usuário. 
    
Como a segunda opção não está disponível para clientes automatizados, esses clientes devem usar a primeira opção. Os clientes devem configurar seus perfis com cuidado para garantir que essa opção sempre funcione.
  
Clientes automatizados sempre configuram o MAPI_NO_MAIL sinalizador na chamada de função [MAPILogonEx](mapilogonex.md) para iniciar uma sessão MAPI. 
  

