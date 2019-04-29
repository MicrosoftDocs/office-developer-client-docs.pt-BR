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
  
> no Um ponteiro para um identificador da janela pai da caixa de diálogo.
    
 _lpfnDismiss_
  
> no Um ponteiro para uma função com base no protótipo [DISMISSMODELESS](dismissmodeless.md) ou nulo. Este membro se aplica apenas à versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido. MAPI chama a função **DISMISSMODELESS** quando o usuário ignora a caixa de diálogo de endereço sem restrições, informando um cliente que está chamando os **detalhes** de que a caixa de diálogo não está mais ativa. 
    
 _lpvDismissContext_
  
> no Um ponteiro para informações de contexto a serem passadas para a função **DISMISSMODELESS** apontada pelo parâmetro _lpfnDismiss_ . Esse parâmetro se aplica apenas à versão sem janela restrita da caixa de diálogo, incluindo o sinalizador DIALOG_SDI no parâmetro _parâmetroulflags_ . 
    
 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada para a entrada para a qual os detalhes são exibidos.
    
 _lpfButtonCallback_
  
> no Um ponteiro para uma função com base no protótipo de função [LPFNBUTTON](lpfnbutton.md) . Uma função **LPFNBUTTON** adiciona um botão à caixa de diálogo detalhes. 
    
 _lpvButtonContext_
  
> no Um ponteiro para dados que foram usados como um parâmetro para a função especificada pelo parâmetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> no Um ponteiro para uma cadeia de caracteres que contém o texto a ser aplicado ao botão adicionado, se esse botão é extensível. O parâmetro _lpszButtonText_ deve ser NULL se você não precisar de um botão extensível. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo de texto para o parâmetro _lpszButtonText_ . Os seguintes sinalizadores podem ser definidos: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que os **detalhes** retornam S_OK se as alterações forem realmente feitas no endereço; caso contrário, os **detalhes** retornarão S_FALSE. 
    
DIALOG_MODAL
  
> Exibe a versão modal da caixa de diálogo endereço comum, que sempre é mostrada em clientes não-Outlook. Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.
    
DIALOG_SDI
  
>  Exibe a versão sem janela restrita da caixa de diálogo de endereço comum. Este sinalizador é ignorado para clientes que não são do Outlook. 
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A caixa de diálogo detalhes foi exibida com êxito para a entrada do catálogo de endereços.
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam o método **Details** para exibir uma caixa de diálogo que fornece detalhes sobre uma entrada específica no catálogo de endereços. Você pode usar os parâmetros _lpfButtonCallback_, _lpvButtonContext_e _lpszButtonText_ para adicionar um botão definido pelo cliente à caixa de diálogo. Quando o botão é clicado, MAPI chama a função de retorno de chamada indicada por _lpfButtonCallback_, passando o identificador de entrada do botão e os dados no _lpvButtonContext_. Se você não precisar de um botão extensível, _lpszButtonText_ deve ser nulo. 
  
 Os **detalhes** dão suporte a cadeias de caracteres Unicode; As cadeias de caracteres Unicode são convertidas no formato MBCS (cadeia de caracteres multibyte) antes de serem exibidas na caixa de diálogo detalhes. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CBaseDialog:: OnOpenEntryID  <br/> |MFCMAPI usa o método **Details** para exibir uma caixa de diálogo que mostra os detalhes de uma entrada do catálogo de endereços.  <br/> |
   
## <a name="see-also"></a>Confira também



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

