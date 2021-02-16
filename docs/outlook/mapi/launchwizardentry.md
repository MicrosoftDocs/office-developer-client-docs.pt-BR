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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437382"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função que inicia o aplicativo Assistente de Perfil com a finalidade de adicionar um ou mais serviços de mensagem a um perfil. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiwz.h  <br/> |
|Função definida implementada por:  <br/> |MAPI  <br/> |
|Função definida chamada por:  <br/> |Aplicativos do cliente  <br/> |
   
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
  
> [in] Um alça para a janela pai do chamador. Se o chamador não tiver uma janela pai, o  _parâmetro hParentWnd_ deverá ser NULL. 
    
 _ulFlags_
  
> [in] Máscara de bits de sinalizadores indicando opções para o Assistente de Perfil. Os sinalizadores a seguir podem ser definidos:
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> O Assistente de Perfil é para adicionar apenas os serviços de mensagem listados por meio do parâmetro  _lppszServiceNameToAdd_ e não exibir sua página para selecionar serviços de mensagem. 
    
MAPI_PW_FIRST_PROFILE 
  
> O perfil a ser criado é o primeiro para esta estação de trabalho. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> A página do Assistente de Perfil para selecionar serviços de mensagem não deve ser exibida. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> O Assistente de Perfil foi lançado pelo aplicativo de configuração do Painel de Controle. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Somente as caixas de diálogo de configuração dos provedores de serviços devem ser exibidas e as páginas do Assistente de Perfil não devem aparecer. Esse sinalizador só poderá ser definido se o sinalizador MAPI_PW_ADD_SERVICE_ONLY estiver definido. 
    
 _lppszServiceNameToAdd_
  
> [in] Ponteiro para uma matriz de cadeias de caracteres que contém os nomes dos serviços de mensagem a serem adicionados ao perfil. A matriz deve terminar com um valor NULL. 
    
 _cbBufferMax_
  
> [in] Tamanho do buffer apontado pelo parâmetro _lpszNewProfileName._ 
    
 _lpszNewProfileName_
  
> [out] Ponteiro para um buffer de cadeia de caracteres em que a função baseada em **LAUNCHWIZARDENTRY** retorna o nome do perfil criado. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. 
    
MAPI_E_CALL_FAILED 
  
> Um erro de origem inesperada ou desconhecida impedia a conclusão da operação. As possibilidades incluem falha ao inicializar o subsistema MAPI para o Assistente de Perfil, a incapacidade de acessar o perfil padrão e um retorno de erro da caixa de diálogo.
    
## <a name="remarks"></a>Comentários

A implementação MAPI do protótipo **da função LAUNCHWIZARDENTRY** é o ponto de entrada no aplicativo assistente de perfil MAPI. MAPI nomes este ponto de entrada **LaunchWizard**. 
  
Quando o MAPI_PW_ADD_SERVICE_ONLY padrão é definido no  _parâmetro ulFlags,_ as seguintes regras se aplicam: 
  
- O MAPI_PW_LAUNCHED_BY_CONFIG sinalizador impede que a página de boas-vindas seja exibida. 
    
- Os MAPI_PW_HIDE_SERVICES_LIST e MAPI_PW_PROVIDER_UI_ONLY padrão são úteis somente quando não há um perfil padrão. Nesse caso, esses sinalizadores determinam qual página do Assistente de Perfil deve ser exibida. 
    
- Se existir um perfil padrão, nenhuma das páginas do Assistente de Perfil será exibida. 
    
- Se existir um perfil padrão, apenas um serviço de mensagem será listado por meio do parâmetro  _lppszServiceNameToAdd_ e esse serviço de mensagem já estiver no perfil padrão, o Assistente de Perfil retornará S_OK sem adicionar nada ao perfil. 
    
Para cada serviço de mensagem a ser adicionado ao perfil, o Assistente de Perfil chama a função de ponto de entrada do serviço com base no protótipo [MSGSERVICEENTRY.](msgserviceentry.md) Para cada provedor de serviços selecionado de um serviço de mensagem a ser adicionado ao perfil, o Assistente de Perfil chama a função de ponto de entrada do provedor com base no protótipo [WIZARDENTRY.](wizardentry.md) Durante a configuração interativa, cada evento de usuário nas páginas de propriedades faz com que o Assistente de Perfil chame a função de retorno de chamada do provedor com base no protótipo [SERVICEWIZARDDLGPROC.](servicewizarddlgproc.md) 
  
Se um provedor de serviços adicionado ao perfil suportar as páginas do Assistente de Perfil, ele deverá permitir a configuração programática do perfil.
  

