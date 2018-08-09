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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 01cc8a8a54137b72091abab3671c08b526ef9e31
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767664"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**Aplica-se a**: Outlook 
  
Adiciona um provedor de serviço para o serviço de mensagem. 
  
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
  
> [in] Um ponteiro para o nome do provedor para adicionar.
    
 _cValues_
  
> [in] A contagem dos valores de propriedade apontado pelo parâmetro _lpProps_ . 
    
 _lpProps_
  
> [in] Um ponteiro para uma matriz de valor de propriedade que descreve as propriedades do provedor para adicionar.
    
 _ulUIParam_
  
> [in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe. O parâmetro _ulUIParam_ é usado se o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a adição do provedor. Sinalizadores a seguir podem ser definidos:
    
  - MAPI_DIALOG: Exibe uma caixa de diálogo para solicitar informações de configuração.
      
  - MAPI_UNICODE: As propriedades de nome e a cadeia de caracteres do provedor estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.
    
 _lpUID_
  
> [out] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo que representa o provedor para adicionar. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O provedor foi adicionado com êxito ao serviço de mensagem.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O método **IProviderAdmin::CreateProvider** adiciona um provedor de serviço para o serviço de mensagem. O parâmetro _lpszProvider_ deve apontar para o nome de um provedor que pertence ao serviço de mensagem. **CreateProvider** não verifica se o nome corresponde ao nome de um provedor de serviço; Se o nome passado não corresponder a um nome de serviço, a chamada é bem-sucedida, mas os resultados serão imprevisíveis. A maioria dos serviços de mensagem não permita provedores a ser adicionado ou excluído enquanto o perfil estiver em uso. 
  
Afinal das informações disponíveis sobre o serviço provedor foi adicionada ao perfil do arquivo Mapisvc, **CreateProvider** chama a função de ponto de entrada do serviço de mensagem com o parâmetro _ulContext_ definido como MSG_SERVICE_ PROVIDER_CREATE. Se MAPI_DIALOG é definida no parâmetro de _ulFlags_ do método **CreateProvider** , os valores nos parâmetros _ulUIParam_ e _ulFlags_ também são passados para a função do ponto de entrada. Esses parâmetros adicionais habilitar o provedor de serviços para exibir sua folha de propriedades, de modo que o usuário pode digitar as definições de configuração. 
  
## <a name="see-also"></a>Confira também

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

