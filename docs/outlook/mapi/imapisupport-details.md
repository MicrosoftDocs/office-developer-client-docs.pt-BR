---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426776"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada de catálogo de endereços específica.
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulUIParam_
  
> bota Um ponteiro para a alça da janela pai da caixa de diálogo retornada.
    
 _lpfnDismiss_
  
> no Um ponteiro para uma função com base no protótipo [DISMISSMODELESS](dismissmodeless.md) ou nulo. Este membro se aplica apenas à versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido. MAPI chama a função **DISMISSMODELESS** quando o usuário ignora a caixa de diálogo de endereço sem restrições, informando um cliente que está chamando **IMAPISupport::D etails** que a caixa de diálogo não está mais ativa. 
    
 _lpvDismissContext_
  
> no Um ponteiro para informações de contexto a serem passadas para a função **DISMISSMODELESS** apontada pelo parâmetro _lpfnDismiss_ . Esse parâmetro se aplica apenas à versão sem janela restrita da caixa de diálogo, incluindo o sinalizador DIALOG_SDI no parâmetro _parâmetroulflags_ . 
    
 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada para o qual os detalhes são exibidos.
    
 _lpfButtonCallback_
  
> no Um ponteiro para uma função com base no protótipo de função [LPFNBUTTON](lpfnbutton.md) . Uma função **LPFNBUTTON** adiciona um botão à caixa de diálogo detalhes. 
    
 _lpvButtonContext_
  
> no Um ponteiro para dados usados como um parâmetro para a função especificada pelo parâmetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> no Um ponteiro para uma cadeia de caracteres que contém o texto a ser aplicado ao botão adicionado se esse botão é extensível. O parâmetro _lpszButtonText_ deve ser NULL se um botão extensível não for necessário. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo de texto para o parâmetro _lpszButtonText_ . O seguinte sinalizador pode ser definido: 
    
DIALOG_MODAL
  
> Exibe a versão modal da caixa de diálogo endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.
    
DIALOG_SDI
  
>  Exibe a versão sem janela restrita da caixa de diálogo de endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A caixa de diálogo detalhes foi exibida com êxito para a entrada do catálogo de endereços.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::D etails** é implementado para objetos de suporte do provedor de catálogo de endereços. Os provedores de catálogo de endereços chamam **detalhes** para exibir uma caixa de diálogo que fornece detalhes sobre uma entrada específica no catálogo de endereços. Os parâmetros _lpfButtonCallback_, _lpvButtonContext_e _lpszButtonText_ podem ser usados para adicionar um botão definido pelo cliente à caixa de diálogo. Quando o botão é clicado, MAPI chama a função de retorno de chamada indicada por _lpfButtonCallback_, passando o identificador de entrada do botão e os dados no _lpvButtonContext_. Se um botão extensível não for necessário, _lpszButtonText_ deverá ser nulo. 
  
## <a name="see-also"></a>Confira também



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

