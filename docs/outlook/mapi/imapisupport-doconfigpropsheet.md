---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cd8727104af694d456074614b5ea7c222c9b91b9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429009"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibe uma folha de propriedades de configuração.
  
```cpp
HRESULT DoConfigPropsheet(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszTitle,
  LPMAPITABLE lpDisplayTable,
  LPMAPIPROP lpConfigData,
  ULONG ulTopPage
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um alça para a janela pai da folha de propriedades.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpszTitle_
  
> [in] Um ponteiro para o título da folha de propriedades.
    
 _lpDisplayTable_
  
> [in] Um ponteiro para a tabela de exibição que descreve os controles para aparecer na folha de propriedades.
    
 _lpConfigData_
  
> [in] Um ponteiro para a [implementação de IMAPIProp](imapipropiunknown.md) a ser usado para acessar as propriedades de configuração a serem exibidas na folha de propriedades. 
    
 _ulTopPage_
  
> [in] Um índice baseado em zero para a página superior padrão da folha de propriedades.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A folha de propriedades de configuração foi exibida.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::D oConfigPropsheet** é implementado para todos os objetos de suporte. **O DoConfigPropSheet** fornece uma interface de usuário padrão para exibir as propriedades de provedores de serviços e serviços de mensagens. Você deve usar essa caixa de diálogo padrão para todas as exibições de propriedade de configuração para que os usuários se beneficiem de uma interface consistente do Windows. 
  
Os provedores de serviços chamam **DoConfigPropSheet** como parte de sua implementação do método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) ou de um botão usado para exibir detalhes sobre propriedades. Os serviços de mensagens **chamam DoConfigPropSheet a** partir da função de ponto de entrada do serviço de mensagens. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode criar a tabela de exibição apontada pelo parâmetro  _lpDisplayTable_ chamando a [função BuildDisplayTable](builddisplaytable.md) ou com código personalizado. 
  
## <a name="see-also"></a>Confira também



[BuildDisplayTable](builddisplaytable.md)
  
[CreateIProp](createiprop.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

