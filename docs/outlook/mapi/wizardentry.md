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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329551"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de ponto de entrada do provedor de serviços que o assistente de perfil chama para recuperar informações suficientes para exibir as folhas de propriedades de configuração do provedor. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiwz. h  <br/> |
|Função definida implementada por:  <br/> |Provedores de serviços  <br/> |
|Função definida chamada por:  <br/> |Assistente de perfil MAPI  <br/> |
   
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
  
> no Identificador de instância da DLL do provedor de serviços. 
    
 _lpcsResourceName_
  
> bota Ponteiro para uma cadeia de caracteres que contém o nome completo do recurso de caixa de diálogo que deve ser exibido pelo assistente de perfil durante a configuração. O tamanho máximo da cadeia de caracteres, incluindo o terminador nulo, é de 32 caracteres. 
    
 _lppDlgProc_
  
> bota Ponteiro para um procedimento de caixa de diálogo padrão do Windows que será chamado pelo assistente de perfil para notificar o provedor de vários eventos. 
    
 _lpMAPIProp_
  
> no Ponteiro para uma implementação de interface de propriedade que fornece acesso às propriedades de configuração. 
    
 _lpMapiSupportObject_
  
> no Ponteiro para o objeto de suporte MAPI aplicável a esta sessão.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A função **WIZARDENTRY** do provedor de serviços foi chamada com êxito. 
    
MAPI_E_CALL_FAILED 
  
> Um erro de origem inesperada ou desconhecida impediu a conclusão da operação.
    
## <a name="remarks"></a>Comentários

O assistente de perfil chama a função baseada em **WIZARDENTRY** quando estiver pronto para exibir a interface do usuário de configuração do provedor de serviços. Quando o assistente de perfil tiver concluído a configuração de todos os provedores, ele gravará as propriedades de configuração no perfil chamando [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

O nome da função baseada em **WIZARDENTRY** deve ser colocado na entrada WIZARD_ENTRY_NAME no MAPISVC. inf. 
  
O nome do recurso é o do recurso de caixa de diálogo que será renderizado no painel do assistente de perfil. O recurso que é passado precisa conter todas as páginas em um único recurso de caixa de diálogo. Quando o assistente de perfil recebe esse recurso, ele ignora o estilo da caixa de diálogo, mas não os estilos de controle e cria todos os controles como filhos da página do assistente de perfil. Todos os controles estão inicialmente ocultos. Os provedores devem certificar-se de que as coordenadas de seus controles são zero ou com base em zero e que não excedem uma largura máxima de 200 unidades de diálogo e uma altura máxima de 150 de unidades de diálogo. Os identificadores de controle abaixo de 400 estão reservados para o assistente de perfil. O assistente de perfil exibe o título do provedor em negrito, acima da interface do usuário do provedor. 
  
O ponteiro de interface de propriedade fornecido no parâmetro _lpMAPIProp_ deve ser mantido pelo provedor para referência futura. O assistente de perfil lida apenas com o conjunto de propriedades mais básico e o provedor pode usar a implementação da interface de propriedade para incluir propriedades adicionais. Durante a configuração, os provedores devem adicionar suas propriedades de configuração ao objeto que está implementando a interface de propriedade. Após todos os provedores terem sido configurados, o assistente de perfil adiciona essas propriedades ao perfil. 
  
Para obter mais informações sobre como usar essa função, consulte [supportIng Message Service Configuration](supporting-message-service-configuration.md). 
  

