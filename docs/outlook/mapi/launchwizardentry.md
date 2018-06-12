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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: d80671331c2760c574ab32d79115a352ee4bcf25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767780"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**Aplica-se a**: Outlook 
  
Define uma função que inicia o aplicativo Assistente de perfil para fins de adição de um ou mais serviços de mensagem a um perfil. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiwz.h  <br/> |
|Função definido implementada por:  <br/> |MAPI  <br/> |
|Função definido chamada pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a>Par�metros

 _hParentWnd_
  
> [in] Um identificador para a janela do pai do chamador. Se o chamador não tiver uma janela pai, o parâmetro _hParentWnd_ deve ser NULL. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores indicando opções para o Assistente de perfil. Sinalizadores a seguir podem ser definidos:
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> O Assistente de perfil é adicionar apenas os serviços de mensagem listados através do parâmetro _lppszServiceNameToAdd_ e não exibir sua página para selecionar serviços de mensagens. 
    
MAPI_PW_FIRST_PROFILE 
  
> O perfil a ser criado é o primeiro para esta estação de trabalho. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> Página de perfil do Assistente para selecionar serviços de mensagem não deve ser exibida. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> O Assistente de perfil foi iniciado pelo aplicativo de configuração do painel de controle. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Somente dos provedores de serviços configuração caixas de diálogo devem ser exibidas e páginas de perfil do assistente não devem ser exibidos. Esse sinalizador só pode ser definida se o sinalizador MAPI_PW_ADD_SERVICE_ONLY está definido. 
    
 _lppszServiceNameToAdd_
  
> [in] Ponteiro para uma matriz de cadeias de caracteres que contém os nomes dos serviços de mensagem a ser adicionada ao perfil. A matriz deve terminar com um valor NULL. 
    
 _cbBufferMax_
  
> [in] Tamanho do buffer apontado pelo parâmetro _lpszNewProfileName_ . 
    
 _lpszNewProfileName_
  
> [out] Ponteiro para um buffer de sequência em que a função com base em **LAUNCHWIZARDENTRY** retorna o nome do perfil criado. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
MAPI_E_CALL_FAILED 
  
> Um erro de origem inesperado ou desconhecido impediu a conclusão da operação. Incapacidade de acessar o perfil padrão e um erro possibilidades incluem falha ao inicializar o subsistema MAPI para o Assistente de perfil, retornar da caixa de diálogo.
    
## <a name="remarks"></a>Coment�rios

A implementação de MAPI do protótipo de função **LAUNCHWIZARDENTRY** é o ponto de entrada para o aplicativo Assistente de perfil de MAPI. Esse ponto de entrada **LaunchWizard**os nomes de MAPI. 
  
Quando o sinalizador MAPI_PW_ADD_SERVICE_ONLY é definido no parâmetro _ulFlags_ , as seguintes regras se aplicam: 
  
- O sinalizador MAPI_PW_LAUNCHED_BY_CONFIG inibe a página de boas-vindas seja exibida. 
    
- Os sinalizadores MAPI_PW_HIDE_SERVICES_LIST e MAPI_PW_PROVIDER_UI_ONLY são úteis somente quando não houver nenhum perfil padrão. Nesse caso, esses sinalizadores determinam qual página deve ser exibida do Assistente de perfil. 
    
- Se existir um perfil padrão, nenhuma das páginas do Assistente de perfil devem ser exibidas. 
    
- Se existir um perfil padrão, o serviço de apenas uma mensagem está listado por meio do parâmetro _lppszServiceNameToAdd_ e que o serviço de mensagem já está no perfil padrão, o Assistente de perfil Retorna S_OK sem adicionar qualquer coisa ao perfil. 
    
Para cada serviço de mensagem a ser adicionada ao perfil, o Assistente de perfil chama a função de ponto de entrada do serviço com base em protótipo [MSGSERVICEENTRY](msgserviceentry.md) . Para cada provedor de serviço selecionado de um serviço de mensagem a ser adicionada ao perfil, o Assistente de perfil chama a função de ponto de entrada do provedor com base em protótipo [WIZARDENTRY](wizardentry.md) . Durante a configuração interativa, todos os eventos do usuário nas páginas de propriedade faz com que o Assistente de perfil chamar a função de retorno de chamada do provedor com base em protótipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) . 
  
Se um provedor de serviço que está sendo adicionado ao perfil do suporta as páginas do Assistente de perfil, ela deve permitir programática configuração do perfil.
  

