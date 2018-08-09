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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 06341f897a7865c09a565db67bb409fc9f49f8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767236"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**Aplica-se a**: Outlook 
  
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
  
> [in] Uma alça para a janela pai da folha de propriedades.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpszTitle_
  
> [in] Um ponteiro para o título da folha de propriedades.
    
 _lpDisplayTable_
  
> [in] Um ponteiro para a tabela de exibição que descreve os controles para que ele apareça na folha de propriedades.
    
 _lpConfigData_
  
> [in] Um ponteiro para a implementação de [IMAPIProp](imapipropiunknown.md) a ser usado para acessar as propriedades de configuração a ser exibida na folha de propriedades. 
    
 _ulTopPage_
  
> [in] Um índice baseado em zero à página padrão superior da folha de propriedades.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A folha de propriedades de configuração foi exibida.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::DoConfigPropsheet** é implementado para todos os objetos de suporte. **DoConfigPropSheet** fornece uma interface de usuário padrão para exibir as propriedades de provedores de serviço e serviços de mensagem. Você deve usar essa caixa de diálogo padrão para todas as exibições da propriedade de configuração para que os usuários se beneficiam de uma interface consistente do Windows. 
  
Provedores de serviços de chamarem **DoConfigPropSheet** como parte de sua implementação do método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) ou com um botão usado para exibir detalhes em Propriedades. Serviços de mensagem chamar **DoConfigPropSheet** de seu função de ponto de entrada de serviço de mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode criar a tabela de exibição apontada pelo parâmetro _lpDisplayTable_ chamando a função [BuildDisplayTable](builddisplaytable.md) ou com código personalizado. 
  
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

