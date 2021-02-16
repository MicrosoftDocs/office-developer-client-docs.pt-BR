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
  
Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada específica do livro de endereços.
  
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
  
> [out] Um ponteiro para a alça para a janela pai da caixa de diálogo retornada.
    
 _lpfnDismiss_
  
> [in] Um ponteiro para uma função baseada no protótipo [DISMISSMODELESS](dismissmodeless.md) ou NULL. Este membro aplica-se somente à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido. MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::D etails** that the dialog box is no longer active. 
    
 _lpvDismissContext_
  
> [in] Um ponteiro para informações de contexto a ser passado para a **função DISMISSMODELESS** apontado pelo _parâmetro lpfnDismiss._ Esse parâmetro se aplica somente à versão sem modo da caixa de diálogo, incluindo o sinalizador DIALOG_SDI no _parâmetro ulFlags._ 
    
 _cbEntryID_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada para o qual os detalhes são exibidos.
    
 _lpfButtonCallback_
  
> [in] Um ponteiro para uma função baseada no protótipo da função [LPFNBUTTON.](lpfnbutton.md) Uma **função LPFNBUTTON** adiciona um botão à caixa de diálogo de detalhes. 
    
 _lpvButtonContext_
  
> [in] Um ponteiro para os dados usados como um parâmetro para a função especificada pelo _parâmetro lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém texto a ser aplicado ao botão adicionado se esse botão for extensível. O  _parâmetro lpszButtonText_ deve ser NULL se um botão extensível não for necessário. 
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla o tipo de texto para o _parâmetro lpszButtonText._ O sinalizador a seguir pode ser definido: 
    
DIALOG_MODAL
  
> Exibe a versão modal da caixa de diálogo de endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.
    
DIALOG_SDI
  
>  Exibe a versão sem modo da caixa de diálogo de endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A caixa de diálogo de detalhes foi exibida com êxito para a entrada do livro de endereços.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::D etails** é implementado para objetos de suporte do provedor de agendamento de endereços. Os provedores de agendamento de endereços chamam **Detalhes** para exibir uma caixa de diálogo que fornece detalhes sobre uma entrada específica no livro de endereços. Os  _parâmetros lpfButtonCallback_,  _lpvButtonContext_ e  _lpszButtonText_ podem ser usados para adicionar um botão definido pelo cliente à caixa de diálogo. Quando o botão é clicado, MAPI chama a função de retorno de chamada apontada por  _lpfButtonCallback_, passando o identificador de entrada do botão e os dados em  _lpvButtonContext_. Se um botão extensível não for necessário,  _lpszButtonText_ deverá ser NULL. 
  
## <a name="see-also"></a>Confira também



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

