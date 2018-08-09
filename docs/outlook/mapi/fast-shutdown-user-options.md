---
title: Opções de desligamento rápido do usuário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Modificado pela última vez: 26 de junho de 2012'
ms.openlocfilehash: a58f8b98ab2f5a5c1028440676a561427272d028
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766523"
---
# <a name="fast-shutdown-user-options"></a>Opções de desligamento rápido do usuário

**Aplica-se a**: Outlook 
  
Este tópico descreve as três Windows configurações do registro que estão disponíveis, iniciando no Microsoft Outlook 2010 e agora, incluindo Microsoft Outlook 2013, para desligamento rápido de clientes MAPI do usuário. Os administradores podem usar essas configurações do registro para especificar o comportamento de desligamento do cliente preferencial dependendo suporte dos provedores de MAPI para desligamento rápido do cliente. Configuração do administrador, por sua vez, determina como o subsistema de MAPI responde a chamada do cliente MAPI para [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) em termos de suporte de desligamento rápido disponíveis. 
  
Embora uma configuração de registro reflete a preferência do administrador no nível do usuário para o desligamento rápido para todos os clientes MAPI, um desenvolvedor de cliente MAPI pode decidir se o cliente suporta desligamento rápido independentemente de outros clientes MAPI e o configuração de registro do administrador. No entanto, para o desligamento rápido ocorrência com êxito, o usuário deve ter a configuração de registro necessárias, um cliente MAPI deve iniciar o desligamento rápido usando o [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) interface e os provedores MAPI que funcionam com o cliente deverá implementar o [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) interface para suportar o desligamento rápido do cliente. 
  
A lista a seguir descreve as três opções de nível do usuário.
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>Opção 1: O subsistema de MAPI habilita o desligamento rápido, a menos que provedores MAPI explicitamente rejeitar 
    
No Outlook 2010, isso é iniciar o comportamento padrão quando o Outlook é o cliente MAPI; não é necessariamente o comportamento padrão de outros clientes MAPI. Para especificar explicitamente essa opção para o Outlook, os administradores podem optar definir a seguinte chave do registro e o valor.
    
Chave do registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000000`
    
Quando um cliente MAPI inicia um desligamento rápido e chama **IMAPIClientShutdown::QueryFastShutdown** a consulta para suporte de desligamento rápido, o subsistema de MAPI responde à consulta retornando S\_Okey contanto que nenhum provedor MAPI que tenha um ativo MAPI sessão com o cliente MAPI tem explicitamente aceitos sem suporte de desligamento rápido. 

Um provedor MAPI recusa sem desligamento rápido Implementando o método [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para retornar um erro (MAPI\_f\_não\_suporte). Se um ou mais provedores MAPI retornam um erro em **IMAPIProviderShutdown::QueryFastShutdown**, o subsistema de MAPI retorna MAPI_\E_\NO\_suporte para **IMAPIClientShutdown::QueryFastShutdown**. 

A menos que um provedor MAPI recusa, o retorna do subsistema MAPI S\_Okey, mesmo se um ou mais provedores não implementou o **IMAPIProviderShutdown: IUnknown** interface. 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>Opção 2: O subsistema de MAPI habilita o desligamento rápido somente se cada provedor MAPI recusa explicitamente em 
    
Os administradores devem definir explicitamente a seguinte chave do registro e o valor para especificar essa preferência para desligamento rápido do cliente.
    
Chave do registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000001`
    
Quando um cliente MAPI inicia um desligamento rápido e chama **IMAPIClientShutdown::QueryFastShutdown** a consulta para suporte de desligamento rápido, o subsistema de MAPI responde à consulta retornando S\_Okey se todos os provedores MAPI que tiver sessões ativas com desligamento rápido do suporte de cliente MAPI. Um provedor MAPI demonstra seu suporte por meio da implementação **IMAPIProviderShutdown::QueryFastShutdown** para retornar um código de erro não (S\_Okey). 

Se um ou mais desses provedores MAPI retornarem MAPI\_f\_não\_suporte, ou não implementar **IMAPIProviderShutdown::QueryFastShutdown**, o subsistema de MAPI retorna um código de erro ao **IMAPIClientShutdown::QueryFastShutdown** .
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>Opção 3: Administrador desabilita o suporte para desligamento rápido do cliente
    
Os administradores devem definir explicitamente a seguinte chave do registro e o valor para desabilitar o suporte para desligamento rápido do cliente.
    
Chave do registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000002`
    
Quando um cliente MAPI inicia um desligamento rápido e chama **IMAPIClientShutdown::QueryFastShutdown** a consulta para suporte de desligamento rápido, o subsistema de MAPI responde à consulta, retornando MAPI_E_NO_SUPPORT, independentemente se qualquer provedor MAPI suporta rápida desligamento. Sob esta configuração do registro, o subsistema de MAPI nunca chama o método **IMAPIProviderShutdown::QueryFastShutdown** ou [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) de qualquer um dos provedores. 
    
## <a name="see-also"></a>Confira também

- [Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)
- [Visão geral do desligamento rápido](fast-shutdown-overview.md)
- [Práticas recomendadas para o desligamento rápido](best-practices-for-fast-shutdown.md)

