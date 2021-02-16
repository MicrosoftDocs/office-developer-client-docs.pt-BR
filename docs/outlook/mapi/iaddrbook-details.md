---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424676"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
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
  
> [in] Um ponteiro para uma alça da janela pai da caixa de diálogo.
    
 _lpfnDismiss_
  
> [in] Um ponteiro para uma função baseada no protótipo [DISMISSMODELESS](dismissmodeless.md) ou NULL. Este membro aplica-se somente à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido. MAPI calls the **DISMISSMODELESS function** when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active. 
    
 _lpvDismissContext_
  
> [in] Um ponteiro para informações de contexto a ser passado para a **função DISMISSMODELESS** apontado pelo _parâmetro lpfnDismiss._ Esse parâmetro se aplica somente à versão sem modo da caixa de diálogo, incluindo o sinalizador DIALOG_SDI no _parâmetro ulFlags._ 
    
 _cbEntryID_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada para a entrada para a qual os detalhes são exibidos.
    
 _lpfButtonCallback_
  
> [in] Um ponteiro para uma função baseada no protótipo da função [LPFNBUTTON.](lpfnbutton.md) Uma **função LPFNBUTTON** adiciona um botão à caixa de diálogo de detalhes. 
    
 _lpvButtonContext_
  
> [in] Um ponteiro para dados que foi usado como um parâmetro para a função especificada pelo _parâmetro lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém texto a ser aplicado ao botão adicionado, se esse botão for extensível. O  _parâmetro lpszButtonText_ deve ser NULL se você não precisar de um botão extensível. 
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla o tipo de texto para o _parâmetro lpszButtonText._ Os sinalizadores a seguir podem ser definidos: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que **Details retornará** S_OK se realmente foram feitas alterações no endereço; caso contrário, **Details** retornará S_FALSE. 
    
DIALOG_MODAL
  
> Exibe a versão modal da caixa de diálogo de endereço comum, que é sempre mostrada em clientes que não são do Outlook. Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.
    
DIALOG_SDI
  
>  Exibe a versão sem modo da caixa de diálogo de endereço comum. Esse sinalizador é ignorado para clientes que não são do Outlook. 
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A caixa de diálogo de detalhes foi exibida com êxito para a entrada do livro de endereços.
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam **o método Details** para exibir uma caixa de diálogo que fornece detalhes sobre uma entrada específica no livro de endereços. Você pode usar os parâmetros  _lpfButtonCallback_,  _lpvButtonContext_ e  _lpszButtonText_ para adicionar um botão definido pelo cliente à caixa de diálogo. Quando o botão é clicado, MAPI chama a função de retorno de chamada apontada por  _lpfButtonCallback_, passando o identificador de entrada do botão e os dados em  _lpvButtonContext_. Se você não precisar de um botão extensível,  _lpszButtonText_ deverá ser NULL. 
  
 **Os detalhes** suportam cadeias de caracteres Unicode; As cadeias de caracteres Unicode são convertidas para o formato de cadeia de caracteres multibyte (MBCS) antes de serem exibidas na caixa de diálogo de detalhes. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI usa o **método Details** para exibir uma caixa de diálogo que mostra os detalhes de uma entrada do livro de endereços.  <br/> |
   
## <a name="see-also"></a>Confira também



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

