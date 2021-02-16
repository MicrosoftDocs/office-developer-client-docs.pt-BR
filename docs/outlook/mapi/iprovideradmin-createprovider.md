---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430802"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona um provedor de serviços ao serviço de mensagens. 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a>Parâmetros

 _lpszProvider_
  
> [in] Um ponteiro para o nome do provedor a ser acrescentado.
    
 _cValues_
  
> [in] A contagem de valores de propriedade apontados pelo _parâmetro lpProps._ 
    
 _lpProps_
  
> [in] Um ponteiro para uma matriz de valores de propriedade que descreve as propriedades do provedor a adicionar.
    
 _ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. O _parâmetro ulUIParam_ será usado se o sinalizador MAPI_DIALOG for definido no _parâmetro ulFlags._ 
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla a adição do provedor. Os sinalizadores a seguir podem ser definidos:
    
  - MAPI_DIALOG: exibe uma caixa de diálogo para solicitar informações de configuração.
      
  - MAPI_UNICODE: o nome do provedor e as propriedades de cadeia de caracteres estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.
    
 _lpUID_
  
> [out] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo que representa o provedor a ser acrescentado. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O provedor foi adicionado com êxito ao serviço de mensagens.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O **método IProviderAdmin::CreateProvider** adiciona um provedor de serviços ao serviço de mensagens. O  _parâmetro lpszProvider_ deve apontar para o nome de um provedor que pertence ao serviço de mensagens. **CreateProvider** não verifica se o nome corresponde ao nome de um provedor no serviço; se o nome passado não corresponder ao nome de um serviço, a chamada será bem-sucedida, mas os resultados serão imprevisíveis. A maioria dos serviços de mensagens não permite que provedores sejam adicionados ou excluídos enquanto o perfil estiver em uso. 
  
Depois que todas as informações disponíveis sobre o provedor de serviços são adicionadas ao perfil do arquivo Mapisvc.inf, **CreateProvider** chama a função de ponto de entrada do serviço de mensagens com o parâmetro  _ulContext_ definido como MSG_SERVICE_PROVIDER_CREATE. Se MAPI_DIALOG for definido no parâmetro _ulFlags_ do método **CreateProvider,** os valores nos parâmetros _ulUIParam_ e _ulFlags_ também serão passados para a função de ponto de entrada. Esses parâmetros adicionais permitem que o provedor de serviços exibir sua folha de propriedades para que o usuário possa inserir definições de configuração. 
  
## <a name="see-also"></a>Confira também

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

