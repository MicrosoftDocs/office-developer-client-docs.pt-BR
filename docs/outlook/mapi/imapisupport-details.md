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
ms.openlocfilehash: 3c1bfccf635b96dd0744d888e69b4af5b8df0fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587864"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada de catálogo de endereço específica.
  
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
  
> [out] Um ponteiro para a alça para a janela pai da caixa de diálogo retornado.
    
 _lpfnDismiss_
  
> [in] Um ponteiro para uma função com base no [DISMISSMODELESS](dismissmodeless.md) protótipo ou nulo. Este membro só se aplica a versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI sendo definido. MAPI chama a função **DISMISSMODELESS** quando o usuário descarte a caixa de diálogo sem janela restrita endereço informando um cliente que está chamando **IMAPISupport::Details** que a caixa de diálogo não está mais ativa. 
    
 _lpvDismissContext_
  
> [in] Um ponteiro para informações de contexto para passar para a função **DISMISSMODELESS** apontado pelo parâmetro _lpfnDismiss_ . Esse parâmetro se aplica somente à versão da caixa de diálogo sem janela restrita, incluindo o sinalizador DIALOG_SDI no parâmetro _ulFlags_ . 
    
 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada para o qual os detalhes são exibidos.
    
 _lpfButtonCallback_
  
> [in] Um ponteiro para uma função com base no protótipo de função [LPFNBUTTON](lpfnbutton.md) . Uma função **LPFNBUTTON** adiciona um botão para a caixa de diálogo detalhes. 
    
 _lpvButtonContext_
  
> [in] Um ponteiro para dados usados como um parâmetro para a função especificada pelo parâmetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém o texto a ser aplicado ao botão adicionado se esse botão é extensível. O parâmetro _lpszButtonText_ deve ser NULL se um botão extensível não é necessária. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo do texto para o parâmetro _lpszButtonText_ . O seguinte sinalizador pode ser definido: 
    
DIALOG_MODAL
  
> Exiba a versão modal da caixa de diálogo endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.
    
DIALOG_SDI
  
>  Exiba a versão sem janela restrita da caixa de diálogo endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A caixa de diálogo detalhes foi exibida com êxito para a entrada do catálogo de endereços.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::Details** é implementado para objetos de suporte do provedor de catálogo de endereços. Provedores de catálogo de endereço chamarem **detalhes** para exibir uma caixa de diálogo que fornece detalhes sobre uma determinada entrada no catálogo de endereços. Os parâmetros _lpfButtonCallback_, _lpvButtonContext_e _lpszButtonText_ podem ser usados para adicionar um botão de cliente definido para a caixa de diálogo. Quando o botão é clicado, o MAPI chama a função de retorno de chamada apontada pela _lpfButtonCallback_, passando o identificador de entrada do botão e os dados em _lpvButtonContext_. Se um botão extensível não for necessário, _lpszButtonText_ deve ser NULL. 
  
## <a name="see-also"></a>Confira também



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

