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
  
> no Um ponteiro para o nome do provedor a ser adicionado.
    
 _cValues_
  
> no A contagem de valores de propriedade apontados pelo parâmetro _lpProps_ . 
    
 _lpProps_
  
> no Um ponteiro para uma matriz de valor de propriedade que descreve as propriedades do provedor a ser adicionado.
    
 _ulUIParam_
  
> no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido. O parâmetro _ulUIParam_ é usado se o sinalizador MAPI_DIALOG estiver definido no parâmetro _parâmetroulflags_ . 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam a adição de provedor. Os seguintes sinalizadores podem ser definidos:
    
  - MAPI_DIALOG: exibe uma caixa de diálogo para solicitar informações de configuração.
      
  - MAPI_UNICODE: o nome do provedor e as propriedades de cadeia de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estarão no formato ANSI.
    
 _lpUID_
  
> bota Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo que representa o provedor a ser adicionado. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O provedor foi adicionado com êxito ao serviço de mensagens.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O método **IProviderAdmin:: CreateProvider** adiciona um provedor de serviços ao serviço de mensagens. O parâmetro _lpszProvider_ deve apontar para o nome de um provedor que pertença ao serviço de mensagens. O **CreateProvider** não verifica se o nome corresponde ao nome de um provedor no serviço; Se o nome passado não corresponder a um nome de serviço, a chamada será bem-sucedida, mas os resultados serão imprevisíveis. A maioria dos serviços de mensagem não permite que os provedores sejam adicionados ou excluídos enquanto o perfil está em uso. 
  
Depois que todas as informações disponíveis sobre o provedor de serviços forem adicionadas ao perfil do arquivo MAPISVC. inf, **CreateProvider** chamará a função de ponto de entrada do serviço de mensagens com o parâmetro _ULCONTEXT_ definido como MSG_SERVICE_ PROVIDER_CREATE. Se MAPI_DIALOG for definido no parâmetro _parâmetroulflags_ do método **CreateProvider** , os valores nos parâmetros _ulUIParam_ e _parâmetroulflags_ também serão passados para a função de ponto de entrada. Esses parâmetros adicionais permitem que o provedor de serviços exiba sua folha de propriedades para que o usuário possa inserir definições de configuração. 
  
## <a name="see-also"></a>Confira também

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

