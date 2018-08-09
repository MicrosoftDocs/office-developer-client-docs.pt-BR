---
title: Gravar um cliente automatizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e5357c1e822dda35d3f38e00f91b58adbaf0ff9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770717"
---
# <a name="writing-an-automated-client"></a>Gravar um cliente automatizado

  
  
**Aplica-se a**: Outlook 
  
Um aplicativo cliente automatizado é um aplicativo que executa autônomo, não exibindo nenhuma interface de usuário.
  
 Por padrão, muitos métodos de interface MAPI mostram uma interface do usuário. Todos esses métodos têm os sinalizadores que permitem que um cliente permitir ou suprimir essa exibição. Embora o MAPI espera provedores de serviços para honram esses sinalizadores, existem alguns provedores que sempre não atendem a essas expectativas. Um motivo legítimo não respeitar os sinalizadores é a dependência do provedor de serviços em um outro serviço que não permita a supressão de interface do usuário. Se você estiver desenvolvendo um cliente automatizado, preste bastante atenção para os provedores de serviços que você está usando e como eles são configurados. Não presuma que todas as suas chamadas a fim de suprimir uma interface de usuário poderão ser bem-sucedidas. 
  
Clientes automatizados devem ter as informações necessárias para a configuração correta de cada um dos serviços de mensagem disponíveis no perfil. Há duas maneiras de fornecer informações de configuração no momento do logon:
  
- O provedor de serviços pode recuperar informações do perfil.
    
- O provedor de serviços pode solicitar informações do usuário. 
    
Desde que a segunda opção não estiver disponível para os clientes automatizados, esses clientes devem usar a primeira opção. Clientes devem configurar seus perfis cuidadosamente para garantir que esta opção sempre funciona.
  
Clientes automatizados sempre defina o sinalizador MAPI_NO_MAIL na chamada da função [MAPILogonEx](mapilogonex.md) para iniciar uma sessão MAPI. 
  

