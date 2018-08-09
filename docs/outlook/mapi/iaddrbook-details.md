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
ms.openlocfilehash: fbe7f02555f76532896c951f50648c528c250a58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766882"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**Aplica-se a**: Outlook 
  
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
  
> [in] Um ponteiro para um identificador da janela pai para a caixa de diálogo.
    
 _lpfnDismiss_
  
> [in] Um ponteiro para uma função com base no [DISMISSMODELESS](dismissmodeless.md) protótipo ou nulo. Este membro só se aplica a versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI sendo definido. MAPI chama a função **DISMISSMODELESS** quando o usuário descarte a caixa de diálogo sem janela restrita endereço informando um cliente que está chamando **detalhes** que a caixa de diálogo não está mais ativa. 
    
 _lpvDismissContext_
  
> [in] Um ponteiro para informações de contexto para passar para a função **DISMISSMODELESS** apontado pelo parâmetro _lpfnDismiss_ . Esse parâmetro se aplica somente à versão da caixa de diálogo sem janela restrita, incluindo o sinalizador DIALOG_SDI no parâmetro _ulFlags_ . 
    
 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada para a entrada para o qual os detalhes são exibidos.
    
 _lpfButtonCallback_
  
> [in] Um ponteiro para uma função com base no protótipo de função [LPFNBUTTON](lpfnbutton.md) . Uma função **LPFNBUTTON** adiciona um botão para a caixa de diálogo detalhes. 
    
 _lpvButtonContext_
  
> [in] Um ponteiro para os dados que foi usados como um parâmetro para a função especificada pelo parâmetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém o texto a ser aplicado ao botão adicionado, se esse botão é extensível. O parâmetro _lpszButtonText_ deve ser NULL se não é necessário um botão extensível. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo do texto para o parâmetro _lpszButtonText_ . Sinalizadores a seguir podem ser definidos: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que os **detalhes** Retorna S_OK se alterações forem feitas realmente o endereço; Caso contrário, **detalhes** retorna S_FALSE. 
    
DIALOG_MODAL
  
> Exiba a versão modal da caixa de diálogo endereço comuns, que sempre é mostrada nos clientes não do Outlook. Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.
    
DIALOG_SDI
  
>  Exiba a versão sem janela restrita da caixa de diálogo endereço comum. Esse sinalizador é ignorada para clientes não do Outlook. 
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A caixa de diálogo detalhes foi exibida com êxito para a entrada do catálogo de endereços.
    
## <a name="remarks"></a>Comentários

Aplicativos cliente chamam o método de **detalhes** para exibir uma caixa de diálogo que fornece detalhes sobre uma determinada entrada no catálogo de endereços. Você pode usar os parâmetros _lpfButtonCallback_, _lpvButtonContext_e _lpszButtonText_ para adicionar um botão de cliente definido para a caixa de diálogo. Quando o botão é clicado, o MAPI chama a função de retorno de chamada apontada pela _lpfButtonCallback_, passando o identificador de entrada do botão e os dados em _lpvButtonContext_. Se você não é necessário um botão extensível, _lpszButtonText_ deve ser NULL. 
  
 **Detalhes** oferece suporte a cadeias de caracteres Unicode; Cadeias de caracteres Unicode são convertidas para o formato de cadeia de caracteres (MBCS) caracteres multibyte antes que eles sejam exibidos na caixa de diálogo detalhes. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI usa o método **Details** para exibir uma caixa de diálogo que mostra os detalhes de uma entrada do catálogo de endereços.  <br/> |
   
## <a name="see-also"></a>Confira também



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

