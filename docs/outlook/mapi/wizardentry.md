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
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430676"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de ponto de entrada do provedor de serviços que o Assistente de Perfil chama para recuperar informações suficientes para exibir as folhas de propriedades de configuração do provedor. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiwz.h  <br/> |
|Função definida implementada por:  <br/> |Provedores de serviços  <br/> |
|Função definida chamada por:  <br/> |Assistente de Perfil MAPI  <br/> |
   
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
  
> [in] Alça de instância da DLL do provedor de serviços. 
    
 _lpcsResourceName_
  
> [out] Ponteiro para uma cadeia de caracteres que contém o nome completo do recurso de caixa de diálogo que deve ser exibido pelo Assistente de Perfil durante a configuração. O tamanho máximo da cadeia de caracteres, incluindo o terminador NULL, é de 32 caracteres. 
    
 _lppDlgProc_
  
> [out] Ponteiro para um procedimento de caixa de diálogo padrão do Windows que será chamado pelo Assistente de Perfil para notificar o provedor de vários eventos. 
    
 _lpMAPIProp_
  
> [in] Ponteiro para uma implementação de interface de propriedade que fornece acesso às propriedades de configuração. 
    
 _lpMapiSupportObject_
  
> [in] Ponteiro para o objeto de suporte MAPI aplicável a esta sessão.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A função **WIZARDENTRY** do provedor de serviços foi chamada com êxito. 
    
MAPI_E_CALL_FAILED 
  
> Um erro de origem inesperada ou desconhecida impedia a conclusão da operação.
    
## <a name="remarks"></a>Comentários

O Assistente de Perfil chama a função baseada em **WIZARDENTRY** quando ela está pronta para exibir a interface do usuário de configuração do provedor de serviços. Quando o Assistente de Perfil terminar de configurar todos os provedores, ele grava as propriedades de configuração no perfil chamando [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

O nome da função **com base EM WIZARDENTRY** deve ser colocado na WIZARD_ENTRY_NAME entrada MAPISVC.INF. 
  
O nome do recurso é o do recurso de caixa de diálogo que será renderizado no painel do Assistente de Perfil. O recurso que é passado para trás precisa conter todas as páginas em um único recurso de caixa de diálogo. Quando o Assistente de Perfil recebe esse recurso, ele ignora o estilo da caixa de diálogo, mas não os estilos de controle, e cria todos os controles como filhos da página do Assistente de Perfil. Todos os controles são inicialmente ocultos. Os provedores devem garantir que as coordenadas para seus controles sejam baseadas em zero ou zero e que não excedam uma largura máxima de 200 unidades de diálogo e uma altura máxima de 150 unidades de diálogo. Os identificadores de controle abaixo de 400 são reservados para o Assistente de Perfil. O Assistente de Perfil exibe o título do provedor em negrito acima da interface do usuário do provedor. 
  
O ponteiro da interface de propriedade fornecido no  _parâmetro lpMAPIProp_ deve ser mantido pelo provedor para referência futura. O Assistente de Perfil lida apenas com o conjunto mais básico de propriedades, e o provedor pode usar a implementação da interface de propriedade para incluir propriedades adicionais. Durante a configuração, os provedores devem adicionar suas propriedades de configuração ao objeto que está implementando a interface de propriedade. Depois que todos os provedores foram configurados, o Assistente de Perfil adiciona essas propriedades ao perfil. 
  
Para obter mais informações sobre como usar essa função, consulte Suporte à configuração [do serviço de mensagens.](supporting-message-service-configuration.md) 
  

