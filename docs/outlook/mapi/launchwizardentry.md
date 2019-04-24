---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270186"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função que inicia o aplicativo assistente de perfil com o objetivo de adicionar um ou mais serviços de mensagem a um perfil. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiwz. h  <br/> |
|Função definida implementada por:  <br/> |MAPI  <br/> |
|Função definida chamada por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a>Parâmetros

 _hParentWnd_
  
> no Uma alça para a janela pai do chamador. Se o chamador não tiver uma janela pai, o parâmetro _hParentWnd_ deverá ser nulo. 
    
 _ulFlags_
  
> no Bitmask de sinalizadores que indicam opções para o assistente de perfil. Os seguintes sinalizadores podem ser definidos:
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> O assistente de perfil é adicionar somente os serviços de mensagens listados por meio do parâmetro _lppszServiceNameToAdd_ , e não exibir sua página para selecionar serviços de mensagens. 
    
MAPI_PW_FIRST_PROFILE 
  
> O perfil a ser criado é o primeiro para esta estação de trabalho. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> A página do assistente de perfil para selecionar serviços de mensagens não deve ser exibida. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> O assistente de perfil foi iniciado pelo aplicativo de configuração do painel de controle. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Somente as caixas de diálogo de configuração dos provedores de serviços devem ser exibidas e as páginas do assistente de perfil não devem ser exibidas. Este sinalizador só poderá ser definido se o sinalizador MAPI_PW_ADD_SERVICE_ONLY estiver definido. 
    
 _lppszServiceNameToAdd_
  
> no Ponteiro para uma matriz de cadeias de caracteres que contém os nomes dos serviços de mensagens a serem adicionados ao perfil. A matriz deve terminar com um valor nulo. 
    
 _cbBufferMax_
  
> no Tamanho do buffer apontado pelo parâmetro _lpszNewProfileName_ . 
    
 _lpszNewProfileName_
  
> bota Ponteiro para um buffer de cadeia de caracteres em que a função baseada no **LAUNCHWIZARDENTRY** retorna o nome do perfil criado. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados. 
    
MAPI_E_CALL_FAILED 
  
> Um erro de origem inesperada ou desconhecida impediu a conclusão da operação. As possibilidades incluem falha ao inicializar o subsistema MAPI para o assistente de perfil, incapacidade de acessar o perfil padrão e um erro retornado da caixa de diálogo.
    
## <a name="remarks"></a>Comentários

A implementação de MAPI do protótipo da função **LAUNCHWIZARDENTRY** é o ponto de entrada no aplicativo assistente de perfil MAPI. Nomes de MAPI este ponto de entrada **LaunchWizard**. 
  
Quando o sinalizador MAPI_PW_ADD_SERVICE_ONLY é definido no parâmetro _parâmetroulflags_ , as seguintes regras são aplicadas: 
  
- O sinalizador MAPI_PW_LAUNCHED_BY_CONFIG inibe a exibição da página de boas-vindas. 
    
- Os sinalizadores MAPI_PW_HIDE_SERVICES_LIST e MAPI_PW_PROVIDER_UI_ONLY são úteis somente quando não há um perfil padrão. Nesse caso, esses sinalizadores determinam qual página do assistente de perfil deve ser exibida. 
    
- Se houver um perfil padrão, nenhuma das páginas do assistente de perfil será exibida. 
    
- Se houver um perfil padrão, apenas um serviço de mensagens será listado através do parâmetro _lppszServiceNameToAdd_ e esse serviço de mensagens já estiver no perfil padrão, o assistente de perfil retornará S_OK sem adicionar nada ao perfil. 
    
Para cada serviço de mensagens a ser adicionado ao perfil, o assistente de perfil chama a função de ponto de entrada do serviço com base no protótipo [MSGSERVICEENTRY](msgserviceentry.md) . Para cada provedor de serviços selecionado de um serviço de mensagens a ser adicionado ao perfil, o assistente de perfil chama a função de ponto de entrada do provedor com base no protótipo [WIZARDENTRY](wizardentry.md) . Durante a configuração interativa, todos os eventos de usuário nas páginas de propriedades fazem com que o assistente de perfil chame a função de retorno de chamada do provedor com base no protótipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) . 
  
Se um provedor de serviços adicionado ao perfil oferecer suporte às páginas do assistente de perfil, ele deverá permitir a configuração programática do perfil.
  

