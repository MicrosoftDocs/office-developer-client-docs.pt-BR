---
title: Opções do usuário para desligamento rápido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Última modificação: 26 de junho de 2012'
localization_priority: Priority
ms.openlocfilehash: 3c60862733c6b38e60650ae9daba9bba578fcd58
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716366"
---
# <a name="fast-shutdown-user-options"></a>Opções do usuário para desligamento rápido

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico descreve as três configurações de registro do Windows disponíveis, iniciando com o Microsoft Outlook 2010 e agora incluindo o Microsoft Outlook 2013, para o desligamento rápido de clientes de MAPI de um usuário. Os administradores podem usar essas configurações de registro para especificar o comportamento de desligamento preferencial do cliente, dependendo do suporte dos provedores de MAPI para o desligamento rápido do cliente. A configuração do administrador, por sua vez, determina como o subsistema de MAPI responde à chamada do cliente de MAPI para [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) em termos de suporte de desligamento rápido disponível. 
  
Mesmo que uma configuração do registro reflita a preferência do administrador no nível do usuário pelo desligamento rápido de todos os clientes de MAPI, um desenvolvedor de cliente de MAPI poderá decidir se o cliente dará suporte ao desligamento rápido independentemente de outros clientes de MAPI e da configuração do registro do administrador. No entanto, para que o desligamento rápido ocorra com êxito, o usuário deverá ter a configuração do registro necessária, um cliente de MAPI deverá iniciar o desligamento rápido usando a interface [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md), e os provedores de MAPI que trabalham com o cliente deverão implementar a interface [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) para dar suporte ao desligamento rápido do cliente. 
  
A lista a seguir descreve as três opções de nível do usuário.
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>Opção 1: o subsistema de MAPI permite o desligamento rápido, a menos que os provedores de MAPI recusem explicitamente 
    
Começando com o Outlook 2010, esse é o comportamento padrão quando o Outlook é o cliente de MAPI; não é necessariamente o comportamento padrão para outros clientes de MAPI. Para especificar explicitamente essa opção para o Outlook, os administradores podem optar por definir o seguinte valor e chave do Registro.
    
Chave do Registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000000`
    
Quando um cliente de MAPI inicia um desligamento rápido e chama **IMAPIClientShutdown::QueryFastShutdown** para consultar o suporte do desligamento rápido, o subsistema de MAPI responde à consulta retornando S\_OK, desde que nenhum provedor de MAPI que tenha uma sessão de MAPI ativa com o cliente de MAPI tenha recusado explicitamente o suporte do desligamento rápido. 

Um provedor de MAPI recusa o desligamento rápido implementando o método [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para retornar um erro (MAPI\_E\_NO\_SUPPORT). Se um ou mais provedores de MAPI retornarem um erro em **IMAPIProviderShutdown::QueryFastShutdown**, o subsistema de MAPI retorná MAPI_\E_\NO\_SUPPORT para **IMAPIClientShutdown::QueryFastShutdown**. 

Se um provedor de MAPI recusar, o subsistema de MAPI retornará S\_OK, mesmo que um ou mais provedores não tenham implementado a interface **IMAPIProviderShutdown: IUnknown**. 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>Opção 2: o subsistema de MAPI habilita o desligamento rápido somente se cada provedor de MAPI aceitar explicitamente 
    
Os administradores devem definir explicitamente o seguinte valor e chave do Registro para especificar essa preferência para o desligamento rápido do cliente.
    
Chave do Registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000001`
    
Quando um cliente de MAPI inicia um desligamento rápido e chama **IMAPIClientShutdown::QueryFastShutdown ** para consultar o suporte do desligamento rápido, o subsistema de MAPI responde à consulta retornando S\_OK se todos os provedores de MAPI que possuem sessões ativas com o cliente de MAPI derem suporte ao desligamento rápido. Um provedor de MAPI demonstra o suporte implementando **IMAPIProviderShutdown::QueryFastShutdown** para retornar um código de não erro (S\_OK). 

Se um ou mais desses provedores de MAPI retornarem MAPI\_E\_NO\_SUPPORT ou não implementarem **IMAPIProviderShutdown::QueryFastShutdown**, o subsistema de MAPI retornará um código de erro para **IMAPIClientShutdown::QueryFastShutdown**.
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>Opção 3: um administrador desabilita o suporte para o desligamento rápido do cliente
    
Os administradores devem definir explicitamente o seguinte valor e a chave do Registro para desabilitar o suporte para o desligamento rápido do cliente.
    
Chave do Registro:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valor:
  
>  `"FastShutdownBehavior"=dword:00000002`
    
Quando um cliente de MAPI inicia um desligamento rápido e chama **IMAPIClientShutdown::QueryFastShutdown** para consultar o suporte do desligamento rápido, o subsistema de MAPI responde à consulta retornando MAPI_E_NO_SUPPORT, independentemente de se algum provedor de MAPI oferece suporte ao desligamento rápido. Nesta configuração de registro, o subsistema de MAPI nunca chama o método **IMAPIProviderShutdown::QueryFastShutdown** ou [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) de qualquer dos provedores. 
    
## <a name="see-also"></a>Confira também

- [Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)
- [Visão geral do desligamento rápido](fast-shutdown-overview.md)
- [Práticas recomendadas para o desligamento rápido](best-practices-for-fast-shutdown.md)

