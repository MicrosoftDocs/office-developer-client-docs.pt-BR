---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3d78b4e6a4a0cc3363edefc84e7ae80dbe72c510
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590355"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de ponto de entrada de provedor de serviço que o Assistente de perfil chama para recuperar informações suficientes para exibir as folhas de propriedades de configuração do provedor. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiwz.h  <br/> |
|Função definido implementada por:  <br/> |Provedores de serviços  <br/> |
|Função definido chamada pelo:  <br/> |Assistente de perfil MAPI  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a>Parâmetros

 _hProviderDLLInstance_
  
> [in] Alça da instância da DLL do provedor de serviços. 
    
 _lpcsResourceName_
  
> [out] Ponteiro para uma cadeia de caracteres que contém o nome completo do recurso diálogo que deve ser exibido pelo Assistente de perfil durante a configuração. O tamanho máximo da cadeia de caracteres, incluindo o terminador NULL, é 32 caracteres. 
    
 _lppDlgProc_
  
> [out] Ponteiro para um procedimento de caixa de diálogo Windows padrão que será chamado pelo Assistente de perfil para notificar o provedor de vários eventos. 
    
 _lpMAPIProp_
  
> [in] Ponteiro para uma implementação de interface de propriedade que fornece acesso às propriedades de configuração. 
    
 _lpMapiSupportObject_
  
> [in] Ponteiro para o objeto de suporte MAPI aplicável a esta sessão.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Função **WIZARDENTRY** do provedor de serviços foi chamada com êxito. 
    
MAPI_E_CALL_FAILED 
  
> Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.
    
## <a name="remarks"></a>Comentários

O Assistente de perfil chama a função **WIZARDENTRY** com base em quando ele estiver pronto para exibir a interface do usuário de configuração do provedor de serviços. Quando o Assistente de perfil for terminar de configurar todos os provedores, ele grava as propriedades de configuração para o perfil chamando [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Deve ser colocado o nome da função **WIZARDENTRY** com base na entrada WIZARD_ENTRY_NAME Mapisvc. 
  
O nome do recurso é que o recurso de diálogo que serão renderizados no painel do Assistente de perfil. O recurso que é passado regressivo deve conter todas as páginas em um recurso de diálogo único. Quando o Assistente de perfil recebe este recurso, ele ignora o estilo de diálogo, mas não os estilos de controle e cria todos os controles como filhos da página do Assistente de perfil. Todos os controles inicialmente estão ocultas. Provedores Certifique-se de que as coordenadas para seus controles zero ou baseado em zero e que não exceder a largura máxima de 200 unidades de diálogo e uma altura de máxima de 150 unidades de diálogo. Identificadores de controle abaixo 400 são reservados para o Assistente de perfil. O Assistente de perfil exibe o título do provedor com texto em negrito acima da interface de usuário do provedor. 
  
O ponteiro de interface da propriedade fornecido no parâmetro _lpMAPIProp_ deve ser mantido pelo provedor para referência futura. O Assistente de perfil lida com apenas o conjunto de forma mais básico de propriedades e o provedor pode usar a implementação de interface de propriedade para incluir propriedades adicionais. Durante a configuração, provedores devem adicionar suas propriedades de configuração para o objeto implementando a interface de propriedade. Depois que todos os provedores que tiverem sido configurados, o Assistente de perfil adiciona essas propriedades para o perfil. 
  
Para obter mais informações sobre como usar esta função, consulte [Configuração do serviço de mensagem com suporte](supporting-message-service-configuration.md). 
  

